#yapi 安装

##环境要求

```markdown
- nodejs（7.6+)
- mongodb（2.6+）
- git
```

## 安装

### 本地安装

```bash
$ mkdir yapi
$ cd yapi
# 或者下载 zip 包解压到 vendors 目录（clone 整个仓库大概 140+ M，可以通过 `git clone --depth=1 https://github.com/YMFE/yapi.git vendors` 命令减少，大概 10+ M
$ git clone https://github.com/YMFE/yapi.git vendors 
# 复制完成后请修改相关配置
$ cp vendors/config_example.json ./config.json
$ cd vendors
$ npm install --production --registry https://registry.npm.taobao.org
# 安装程序会初始化数据库索引和管理员账号，管理员账号名可在 config.json 配置
$ npm run install-server
> yapi-vendor@1.7.0 install-server /Users/zhangkai/DevApps/yapi/vendors
>  node server/install.js

log: mongodb load success...
初始化管理员账号成功,账号名："425485346@qq.com"，密码："ymfe.org"
# 启动服务器后，请访问 127.0.0.1:{config.json配置的端口}，初次运行会有个编译的过程，请耐心等候
$ node server/app.js
log: -------------------------------------swaggerSyncUtils constructor-----------------------------------------------
log: 服务已启动，请打开下面链接访问: 
http://127.0.0.1:3000/
log: mongodb load success...
```

### docker 安装

## 相关配置文件

- yapi/config.json

  - ```json
    {
      "port": "3000",
      "adminAccount": "425485346@qq.com",
      "db": {
        "servername": "127.0.0.1",
        "DATABASE": "yapi",
        "port": 27017,
        "user": "",
        "pass": "",
        "authSource": ""
      },
      "mail": {
        "enable": true,
        "host": "smtp.qq.com", //邮箱服务器
        "port": 465, //端口
        "from": "425485346@qq.com", //发送人邮箱
        "auth": {
          "user": "425485346@qq.com", //邮箱服务器账号
          "pass": "nvzrcxfynxudbjid" //邮箱服务器密码
        }
      }
    }
    ```