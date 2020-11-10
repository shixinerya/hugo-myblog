docker run -d --name ariang --restart unless-stopped --log-opt max-size=1m -p 6880:6880 p3terx/ariang
docker run -d --name aria2-pro --restart unless-stopped --log-opt max-size=1m --network host -e PUID=$UID -e PGID=$GID -e RPC_SECRET=admin -e RPC_PORT=6800 -e LISTEN_PORT=6888 p3terx/aria2-pro

docker run -d     --name aria2-onedrive     --restart unless-stopped     --log-opt max-size=1m     --network host     -e PUID=$UID     -e PGID=$GID     -e RPC_SECRET=dana5haw     -e RPC_PORT=6803     -e LISTEN_PORT=33333     -v ~/aria2-onedrive-config:/config     -v ~/onedrive-downloads:/downloads     -e RCLONE=enable     p3terx/aria2-pro

docker run -d     --name aria2-onedrive     --restart unless-stopped     --log-opt max-size=1m     --network host     -e PUID=$UID     -e PGID=$GID     -e RPC_SECRET=dana5haw     -e RPC_PORT=6803     -e LISTEN_PORT=33333     -v ~/aria2-onedrive-config:/config     -v ~/onedrive-downloads:/downloads     -e RCLONE=enable     p3terx/aria2-pro


docker run -d --name aria2-onedrive --restart unless-stopped --log-opt max-size=1m --network host -e PGID=$UID -e PGID=$GID -e RPC_SECRET=dana5haw -e RPC_PORT=6803 -e LISTEN_PORT=33333 -e RCLONE=enable p3terx/aria2-pro

docker run -d --name aria2-pro --restart unless-stopped --log-opt max-size=1m --network host -e PUID=$UID -e PGID=$GID -e RPC_SECRET=P3TERX -e RPC_PORT=6800 -e LISTEN_PORT=6888 -v D:\Users\aria2-config:/config -v D:\Users\rclone-downloads:/downloads -v D:\Users\usr\bin\gclone:/usr/local/bin/rclone -v D:\Users\service-account:/service-account -e SPECIAL_MODE=rclone p3terx/aria2-pro

pyone的安装：
印象笔记

8888
username: quhmj0cf
password: c9563877

aria密匙：aria2
pyone后台密码：123456

PyOne安装完成！
请通过访问：http://39.103.135.32:34567 继续后面的安装
PyOne后台密码：123456
Aria2密匙：aria2
常用命令：
1. 暂停PyOne: systemctl stop pyone
2. 启动PyOne: systemctl start pyone
3. 重启PyOne: systemctl restart pyone
4. 手动运行PyOne: systemctl stop pyone && gunicorn -keventlet -b 0:34567 run:app
5. 暂停Aria2: systemctl stop aria2
6. 启动Aria2: systemctl start aria2
7. 重启Aria2: systemctl restart aria2




宝塔：
FTP账号资料

用户：ftp_39_103_135_32
密码：HfrzrC8Ftw8stp5s1
//宝塔界面的安装，直接到宝塔的官网上进行安装

- aria2的搭建
	1. 一行命令的搭建
	apt install wget curl ca-certificates//更新环境
	wget -N git.io/aria2.sh && chmod +x aria2.sh//下载脚本
	./aria2.sh//运行脚本
	配置自动上传脚本
Aria2 一键安装管理脚本 增强版 整合了 Aria2 完美配置 ，安装后会附带一些附加功能脚本功能脚本，RCLONE 自动上传脚本就是其中之一。由于默认不启用，所以需要手动启用。

TIPS: 本项目的上传脚本使用更稳定快速的原生命令上传方式，而非处在测试阶段的挂载方式，这点和一般的脚本不同。
输入nano /root/.aria2c/aria2.conf打开 Aria2 配置文件进行修改。或使用Aria2 一键安装管理脚本 增强版中的手动修改选项打开配置文件进行修改。找到“下载完成后执行的命令”，把clean.sh替换为upload.sh。
# 下载完成后执行的命令
on-download-complete=/root/.aria2c/upload.sh
nano 编辑器的操作方法参见《Linux 下适合新手的文本编辑器 nano 使用教程》
输入nano /root/.aria2c/script.conf打开附加功能脚本配置文件进行修改，有中文注释，按照自己的实际情况进行修改，第一次使用只建议修改网盘名称。
# 网盘名称(RCLONE 配置时填写的 name)
drive-name=OneDrive
重启 Aria2 。脚本选项重启或者执行以下命令：
service aria2 restart
检查是否配置成功
执行 upload.sh 脚本，提示 success 即配置成功。

/root/.aria2c/upload.sh
	2. 原始安装
	
	3. docker的安装
	
	
启动：/etc/init.d/aria2 start | service aria2 start

停止：/etc/init.d/aria2 stop | service aria2 stop

重启：/etc/init.d/aria2 restart | service aria2 restart

查看状态：/etc/init.d/aria2 status | service aria2 status

配置文件路径：/root/.aria2c/aria2.conf （配置文件有中文注释，若语言设置有问题会导致中文乱码）

默认下载目录：/root/downloads

RPC 密钥：随机生成，可使用选项7. 修改 配置文件自定义

//reclone
 一键安装脚本
 curl https://rclone.org/install.sh | sudo bash
//ariaNG的搭建
docker run -d \
    --name ariang \
    --restart unless-stopped \
    --log-opt max-size=1m \
    -p 6880:6880 \
    p3terx/ariang
	
	




