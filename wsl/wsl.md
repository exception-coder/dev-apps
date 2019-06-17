# Windows Subsystem for Linux (WSL)

## 开启ssh

```bash
# 查看是否安装 ssh 服务
$ dpkg -l | grep ssh
ii  openssh-client                 1:7.6p1-4ubuntu0.3                 amd64        secure shell (SSH) client, for secure access to remote machines
ii  openssh-server                 1:7.6p1-4ubuntu0.3                 amd64        secure shell (SSH) server, for secure access from remote machines
ii  openssh-sftp-server            1:7.6p1-4ubuntu0.3                 amd64        secure shell (SSH) sftp server module, for SFTP access from remote machines
ii  ssh-import-id                  5.7-0ubuntu1.1                     all          securely retrieve an SSH public key and install it locally
# 如果没有 openssh-server 则安装 openssh-server 服务
$ sudo apt-get install openssh-server
```



-  编辑配置文件 `/etc/ssh/sshd_config`

```sshd_config
$ # To disable tunneled clear text passwords, change to no here!
PasswordAuthentication yes
```

```bash
$ sudo service ssh —-full-restart
$ ps -e | grep ssh
933 ?        00:00:00 sshd
```



## 参考文档

- [Windows Subsystem for Linux Installation Guide for Windows 10](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

