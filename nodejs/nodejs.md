# 安装

## 环境准备

```markdown
- linux
```

## 安装

- Unzip the binary archive to any directory you wanna install Node, I use `/usr/local/lib/nodej`

```bash
$ wget https://nodejs.org/dist/v10.16.0/node-v10.16.0-linux-x64.tar.xz
$ sudo mkdir -p /usr/local/lib/nodejs
$ sudo tar -xJvf node-v10.16.0-linux-x64.tar.xz -C /usr/local/lib/nodejs 
```

- Set the environment variable `~/.profile`, add below to the end

```
# Nodejs
export PATH=/usr/local/lib/nodejs/node-v10.16.0-linux-x64/bin:$PATH
```

- Refresh profile

```bash
$ . ~/.profile
```

- Test installation using

```bash
$ node -v
v10.16.0
$ npm version
{ npm: '6.9.0',
  ares: '1.15.0',
  brotli: '1.0.7',
  cldr: '35.1',
  http_parser: '2.8.0',
  icu: '64.2',
  modules: '64',
  napi: '4',
  nghttp2: '1.34.0',
  node: '10.16.0',
  openssl: '1.1.1b',
  tz: '2019a',
  unicode: '12.1',
  uv: '1.28.0',
  v8: '6.8.275.32-node.52',
  zlib: '1.2.11' }
$ npx -v
6.9.0
```

- To create a **sudo** link:

```bash
$ sudo ln -s /usr/local/lib/nodejs/node-node-v10.16.0-linux-x64/bin/node /usr/bin/node

$ sudo ln -s /usr/local/lib/nodejs/node-node-v10.16.0-linux-x64/bin/npm /usr/bin/npm

$ sudo ln -s /usr/local/lib/nodejs/node-node-v10.16.0-linux-x64/bin/npx /usr/bin/npx
```



## 参考文档

- [install Node.js via binary archive on Linux](<https://github.com/nodejs/help/wiki/Installation>)