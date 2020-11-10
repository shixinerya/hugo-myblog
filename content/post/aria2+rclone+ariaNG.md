





~~~shell
docker run -d \
    --name aria2ProNG \
    --restart unless-stopped \
    --log-opt max-size=1m \
    -p 6881:6880 \
    p3terx/ariang
~~~



~~~shell
docker run -d \
    --name aria2-pro \
    --restart unless-stopped \
    --log-opt max-size=1m \
    -e PUID=$UID \
    -e PGID=$GID \
    -e RPC_SECRET=P3TERX \
    -e RPC_PORT=6800 \
    -e LISTEN_PORT=6888 \
    -v ~/aria2-config:/config # 从本地的aria2上面拷贝yi'fen\
    -v ~/rclone-downloads:/downloads \
    -e SPECIAL_MODE=rclone \
    p3terx/aria2-pro
~~~

​    --network host \

~~~
git clone https://github.com/P3TERX/Docker-Aria2-Pro.git

导一个配置文件
aria2


~~~



