

# 一个服务器可以干什么

docker 环境 

~~~shell

# 卸载旧版本
# 较旧的 Docker 版本称为 docker 或 docker-engine 。如果已安装这些程序，请卸载它们以及相关的依赖项。
yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
# 设置仓库
# 安装所需的软件包。yum-utils 提供了 yum-config-manager ，并且 device mapper 存储驱动程序需要 device-mapper-persistent-data 和 lvm2。
yum install -y yum-utils \
  device-mapper-persistent-data \
  lvm2
# 使用以下命令来设置稳定的仓库。
yum-config-manager \
    --add-repo \
    http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
# 安装 Docker Engine-Community
# 安装最新版本的 Docker Engine-Community 和 containerd，或者转到下一步安装特定版本：
yum install docker-ce docker-ce-cli containerd.io

$ yum list docker-ce --showduplicates | sort -r

docker-ce.x86_64  3:18.09.1-3.el7                     docker-ce-stable
docker-ce.x86_64  3:18.09.0-3.el7                     docker-ce-stable
docker-ce.x86_64  18.06.1.ce-3.el7                    docker-ce-stable
docker-ce.x86_64  18.06.0.ce-3.el7                    docker-ce-stable

$ sudo yum install docker-ce-<VERSION_STRING> docker-ce-cli-<VERSION_STRING> containerd.io
$ sudo systemctl start docker
sudo mkdir -p /etc/docker
sudo systemctl daemon-reload
 sudo systemctl restart docker
docker官网地址  https://www.docker.com/

docker启动命令,docker重启命令,docker关闭命令

启动        systemctl start docker

守护进程重启   sudo systemctl daemon-reload

重启docker服务   systemctl restart  docker

重启docker服务  sudo service docker restart

关闭docker service docker stop

关闭docker systemctl stop docker
    
~~~

### Docker安装（已安装的可省略此步骤）（快捷安装）

```shell
curl -sSL https://get.docker.com/ | sh
service docker restart 
systemctl enable docker  #设置开机自启
```







视频解析、aria2的安装（一个就够了）、onedrive分享盘 、



1. 宝塔面板

   - ```shell
     yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh
     ```

     mwhp6lpn
     
     123456

2. 分享盘 

   - oneindex（oneindex）

     - ~~~shell
       #创建临时容器：
       docker run -itd --name=tmp baiyuetribe/oneindex
       #拷贝容器内文件到宿主机目录：
       docker cp tmp:/var/www/html /opt/oneindex
       docker rm -f tmp
       #正式启动服务：
       docker run -d -p 8181:80 -v /opt/oneindex:/var/www/html --restart=always baiyuetribe/oneindex
       ~~~

     - 挂载windows本地盘: RaiDrive垃圾

     第二个分享盘：（把分享盘挂载本地）

     ~~~shell
     #创建临时容器：
     docker run -itd --name=tmp baiyuetribe/oneindex
     #拷贝容器内文件到宿主机目录：
     docker cp tmp:/var/www/html /opt/oneindexkel
     docker rm -f tmp
     #正式启动服务：
     docker run -d -p 8183:80 -v /opt/oneindexkel:/var/www/html --restart=always baiyuetribe/oneindex
     
     
     ~~~

     

     ​	把主题更换一下

   - 安装失败可能是谷歌浏览器的原因

   - 完了之后可以进行主题更换

3. 离线下载
   - aria2:一键安装

     ~~~shell
     wget -N git.io/aria2.sh && chmod +x aria2.sh && ./aria2.sh
     // 因为网络原因，如果没有安装好的话多试几次，
     ~~~

   - rclone：一键安装

     ~~~shell
     curl https://rclone.org/install.sh | sudo bash
     
     ~~~

     

   - ariaNG（docker）（aria2 GUI）：如果连接不上的话，就把6800的端口开放

   - ~~~shell
     
     
     docker run -d \    --name ariang \    --restart unless-stopped \    --log-opt max-size=1m \    -p 6880:6880 \    p3terx/ariang
     ~~~

   **之后待解决的问题**

   在服务器上只能装一个，我想要使用多个账号那就要docker安装aria2，rclone。

   图床

   - 七牛云

4. pyone 个人网盘:https://www.moerats.com/archives/806/

5. wordpress:

   ~~~shell
   docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=baiyue -d mysql:5.5   #安装数据库大小只有66MB
   docker run -p 80:80 --name some-wordpress --link some-mysql:mysql -d wordpress  #运行wordpress
   ~~~

   wordpress的doker搭建方法：要可以完整的保存数据，用卷连接起来。

   最好能自己build一个wordpress。最新版哦，可以自由的切换主题

   hugo博客的搭建，不行的话试试世纪网盘。

   先用免费版的wordpress试试手，然后本地搭建。

6. 开源博客：GRAV

   ~~~shell
   https://baiyue.one/archives/426.html
   ~~~

7. KODExplorer-可道云

   ~~~shell
   docker run -d -p 999:80 --name kodexplorer -v "$PWD":/code baiyuetribe/kodexplorer
   ~~~

   

   1. JPress:可以对接微信公众号和小程序的博客：

   ~~~
   wget https://gitee.com/fuhai/jpress/raw/master/docker-compose.yml
   docker-compose up -d
   ~~~

   

8. owcloud网盘

   ~~~
   docker run -it -d -p 8181:80 owncloud
   ~~~

   首次登陆是创建

   

10. office：

   ```shell
   docker run -itd -p 666:80 --restart=always onlyoffice/communityserver
   ```

11. nextcloud：

    ~~~shell
     docker run -d -p 8080:80 nextcloud 
    
    ~~~

    

12. docker桌面  Xfce是一个适用于类UNIX操作系统的轻量级桌面环境。它的目标是快速而低廉的系统资源，同时仍然具有视觉吸引力和用户友好性。

    ```shell
    docker run -d -p 6080:6080 -e VNC_RESOLUTION=1920x1080 wangguanzzz/xfce-desktop
    ```

    完成后访问：[http://ip:6080](http://ip:6080/) 默认的vnc密码是 `vncpassword`

13. vpn(v2ry的文件配置)

    ```shell
    docker run -d --name v2ray --restart always --network host jrohy/v2ray    #安装程序
    docker exec v2ray bash -c "v2ray info"  #查看配置信息
    
    ```

14. 视频解析

    docker run -d -p 9527:80 baiyuetribe/onekey:vipvideo

15. roboat

    ~~~
    {
      "aria2-server": "ws://39.103.135.32:6800/jsonrpc",
      "aria2-key": "31a1a5df917f426a1092",
      "proxy": "http://127.0.0.1:7890",
      "bot-key": "123456789:xyz",
      "user-id": "123456",
      "max-index": 10
    }
    ~~~

    ~~~
    docker run -d \
        --name tele-aria2 \
        --restart unless-stopped \
        --log-opt max-size=1m \
        -p  \
        -v root/.tele-aria2-conf.json:/config.json \
        p3terx/tele-aria2:0.2.2
    ~~~

    





OneDrive、centos

科学上网、博客、搭建个人网盘



发散是： 微软的office，pyone，

docker安装软件：docker是跨平台的，我会在docker里面安装所有就好了。







厉害的博主： 

https://blog.kieng.cn/    //给了一个网盘

软件在Windows上的使用，和软件在Linux上的使用，这就是跨平台的软件。



多个网盘的使用：先使用国际版的装上，国内的高速版等这些完了之后再看。

onedrive云盘的使用：一个做同步盘（同步盘里面的所有文件保持一致），一个做网盘可以存网上下载的东西。【所有重要的东西本地都有】

centos服务器：aria2（ariaNG）【一键脚本，docker未完成】，oneindex【完成】（后续的进阶，可以更改网页，使图像更人性化，可以直接在博客跳转到对应的页面），rclone【已完成】，

oneindex:直接抽取OneDrive上面的数据，流量是从OneDrive转接到服务器，再到我的本地网页。

reclone：可以登录onedrive与网盘挂载。可以从网盘抽取数据。

aria2：可以与reclone对接，用服务器做缓存和下载，转接到OneDrive上。



最后的效果就是，对于一些大的，下载慢的东西（比如Java的jdk就可以直接在离线下载上下载）下载到OneDrive网盘上，我用的时候直接从OneDrive网盘上拉取。【世纪云盘可以加速，我觉得国际版的OneDrive是不慢的，科学上网就可以解决所有的网络问题】、

科学上网：可以使我的搜索范围扩展到整个世界。

一件事情不能做完要备案。

临时邮箱，我还想再要onedrive几个账号。到时候没有了到淘宝店上买

windows上的应用： raidrive，onedrive，rclone，ariang客户端，

插件网盘助手 可以从百度网盘上拉取资源



实验的环境可以在实验盘上进行。{ 我需要一个实验的环境，一个稳定的，一个是测试用的，git就是管理数据的，github是同步用的，git主要是代码，onedrive云盘同步的是所有}

关于精力管理：不一定所有的事情都要用充沛的精力

大同社会不是最好的社会。

想着赚钱

人力有穷我很菜，我帮不到你。

我写的文章比较散乱想到哪里写哪里。我在一篇文章上写单一的内容很困难。

博客优化：用一个标签可以把我写的话抽出来组成一个文章

我能控制的只有那么一点点，其他的网盘就用来收藏吧。



看视频最快是：哔哩哔哩、腾讯。我自己的可以bilibili，onedrive（paper），超星。