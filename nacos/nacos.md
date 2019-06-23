# naocs安装

## macos 安装

```bash
$ cd /Users/zhangkai/DevApps/naocs
$ wget https://github.com/alibaba/nacos/releases/download/1.0.1/nacos-server-1.0.1.tar.gz
$ tar -xvf nacos-server-1.0.1.tar.gz
$ cd nacos/bin
$ sh startup.sh -m standalone
# ubuntu 使用 bash 启动
$ bash -f ./startup.sh -m standalone
$ sh shutdown.sh
```

