# mongo安装

## docker

```bash
$ cd /Users/zhangkai/DockerApps/mongo
# 拉取 mongo 镜像
$ docker pull mongo
$ docker images
REPOSITORY                 TAG                 IMAGE ID            CREATED             SIZE
mongo                      latest              0fb47b43df19        13 days ago         411MB
# centos7 临时关闭 SELinux
$ sudo setenforce 0 
# 启动 mongo 容器
$ docker run -p 27017:27017 -v $PWD/db:/data/db -d mongo:latest
```

