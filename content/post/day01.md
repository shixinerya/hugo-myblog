---
title: "Day01"
date: 2020-10-12T15:12:28+08:00
draft: false
---
# day01

## MySql配置
docker run -p 3306:3306 --name mysql -v /mydata/mysql/log:/var/log/mysql -v /mydata/mysql/data:/var/lib/mysql -v /mydata/mysql/conf:/etc/mysql -e MYSQL_ROOT_PASSWORD=root -d mysql:5.7
vi /mydata/mysql/conf/my.cnf

[client]
default-character-set=utf8

[mysql]
default-character-set=utf8

[mysqld]
init_connect='SET collation_connection = utf8_unicode_ci'
init_connect='SET NAMES utf8'
character-set-server=utf8
collation-server=utf8_unicode_ci
skip-character-set-client-handshake
skip-name-resolve

## redis 配置

![](D:\_Astudent\snipaste\Snipaste_2020-10-12_19-31-39.png)
mkdir -p /mydata/redis/conf
touch /mydata/redis/conf/redis.conf

docker run -p 6379:6379 --name redis -v /mydata/redis/data:/data -v /mydata/redis/conf/redis.conf:/etc/redis/redis.conf -d redis redis-server /etc/redis/redis.conf
docker exec -it redis redis-cli # 可以直接使用redis
exit
### redis 数据持久化

![image-20201012195020976](C:\Users\temperature0\AppData\Roaming\Typora\typora-user-images\image-20201012195020976.png)

redis-desktop



## maven 配置阿里云加速、配置jdk1.8运行环境

  <mirror>
      <id>alimaven</id>
	  <mirrorOf>central</mirrorOf>
      <name>aliyun maven</name>
      <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
      <mirrorOf>central</mirrorOf>        
    </mirror>
	
	<profile>
		<id>jdk-1.8</id>
		<activation>
			<activeByDefault>true</activeByDefault>
			<jdk>1.8</jdk>
		</activation>
		<properties>
			<maven.compiler.source>1.8</maven.compiler.source>
			<maven.compiler.target>1.8</maven.compiler.target>
			<maven.compiler.compilerVersion>1.8</maven.compiler.compilerVersion>
		</properties>
	</profile>

IDEA 的 maven 配置
IDEA安装插件 
	Plugins
	简化javabean的开发 lombok mybatisx
## vscode
	auto close tag
	auto rename tag
	eslint
	html css support
	html snippets
	javascript
	live server
	open in browser
	vetur

## git 配置

git config --global user.name ""
git config --global user.email ""	
使用ssh免密连接 ssh-keygen -t rsa -C "xxxxx@xxxxx.com"
cat ~/.ssh/id_rsa.pub
ssh-T git#gitee.com

## 搭建gitee仓库

在IDEA中使用版本控制

