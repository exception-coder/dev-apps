# Git安装

## 环境

```bash
$ uname -a
Linux DESKTOP-NCB813A 4.4.0-17763-Microsoft #379-Microsoft Wed Mar 06 19:16:00 PST 2019 x86_64 x86_64 x86_64 GNU/Linux
```



## 本地安装

```bash
$ sudo mkdir /usr/local/lib/git
$ wget https://github.com/git/git/archive/v2.22.0.tar.gz
$ sudo tar -zxf v2.22.0.tar.gz
$ cd git-2.22.0
$ make configure
$ ./configure --prefix=/usr
$ make all doc info
$ sudo make install install-doc install-html install-info

```

