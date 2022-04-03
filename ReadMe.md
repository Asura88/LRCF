# GitHub 资源

---

## GitHub Proxy

GitHub 文件 , Releases , archive , gist , raw.githubusercontent.com 文件代理加速下载服务.

![image-20220403163704481](https://cdn.jsdelivr.net/gh/Asura88/Mannix/img/202204031637734.png)

### 终端命令行

支持终端命令行 git clone , wget , curl 等工具下载.

支持 raw.githubusercontent.com , gist.github.com , gist.githubusercontent.com 文件下载.

**注意：**不支持 SSH Key 方式 git clone 下载.

#### **git clone**

```
git clone https://ghproxy.com/https://github.com/stilleshan/ServerStatus
```

#### **wget & curl**

```
wget https://ghproxy.com/https://github.com/stilleshan/ServerStatus/archive/master.zip
wget https://ghproxy.com/https://raw.githubusercontent.com/stilleshan/ServerStatus/master/Dockerfile
curl -O https://ghproxy.com/https://github.com/stilleshan/ServerStatus/archive/master.zip
curl -O https://ghproxy.com/https://raw.githubusercontent.com/stilleshan/ServerStatus/master/Dockerfile
```

### 首页下载

在本页地址栏输入合规链接（参考以下链接）点击下载按钮

支持 raw.githubusercontent.com , gist.github.com , gist.githubusercontent.com 文件下载.

#### **Raw 文件**

```
https://raw.githubusercontent.com/stilleshan/ServerStatus/master/Dockerfile
```

#### **分支源码**

```
https://github.com/stilleshan/ServerStatus/archive/master.zip
```

#### **Releases 源码**

```
https://github.com/stilleshan/ServerStatus/archive/v1.0.tar.gz
```

#### **Releases 文件**

```
https://github.com/fatedier/frp/releases/download/v0.33.0/frp_0.33.0_linux_amd64.tar.gz
```

### 镜像站

```
https://mirror.ghproxy.com/

https://gh.api.99988866.xyz/
```

## PiQi文库

### 项目发起者

```
https://github.com/PeiQi0
```

### 项目地址

```
https://github.com/PeiQi0/PeiQi-WIKI-Book
```

### 源码地址

```
https://github.com/PeiQi0/PeiQi-WIKI-Book/archive/refs/heads/main.zip

https://ghproxy.com/https://github.com/PeiQi0/PeiQi-WIKI-Book/archive/refs/heads/main.zip
```

### [PeiQi-WIKI-Book-2022-03-20](https://github.com/PeiQi0/PeiQi-WIKI-Book/releases/tag/PeiQi-WIKI-Book-2022-03-20)

```
https://github.com/PeiQi0/PeiQi-WIKI-Book/releases/download/PeiQi-WIKI-Book-2022-03-20/PeiQi-WIKI-Book-HTML.zip

https://ghproxy.com/https://github.com/PeiQi0/PeiQi-WIKI-Book/releases/download/PeiQi-WIKI-Book-2022-03-20/PeiQi-WIKI-Book-HTML.zip
```

### 本地搭建

文库支持多种快捷的方式在本地搭建随时查阅文库，项目图片均为本地化，推荐Docker或内网搭建，不推荐公网服务器部署

#### Yarn源码搭建 (个人二次扩展，需要编译环境)

```
git clone https://github.com/PeiQi0/PeiQi-WIKI-Book.git
cd PeiQi-WIKI-Book
yarn add vuepress-theme-antdocs -d
yarn install
yarn run dev
```

#### Html源码搭建 (无需编译环境，使用编译好的Html文件直接部署)

```
git clone https://github.com/PeiQi0/PeiQi-WIKI-Book.git
cd PeiQi-WIKI-Book/docs/.vuepress/dist
mv * 你的服务器Web目录
```

#### Docker搭建 (只需要Dokcer环境，快速搭建在各个环境中)

```
docker search peiqipeiqi
docker pull peiqipeiqi/peiqi_wiki:220320
docker run -t -d -p 65534:80 --name "PeiQi_Wiki" peiqipeiqi/peiqi_wiki:220320
User/Pass: peiqi:peiqi
```

### PeiQi文库在线版

```
http://wiki.peiqi.tech/
```

![image-20220403170612630](https://cdn.jsdelivr.net/gh/Asura88/Mannix/img/202204031706714.png)

## Vulhub

### 项目发起者

```
https://github.com/vulhub
```

### 项目地址

```
 https://github.com/vulhub/vulhub
```

### 源码地址

```
https://github.com/vulhub/vulhub/archive/refs/heads/master.zip

https://ghproxy.com/https://github.com/vulhub/vulhub/archive/refs/heads/master.zip
```

### 安装

在Ubuntu 20.04下安装docker/docker-compose:

```
# 安装pip
curl -s https://bootstrap.pypa.io/get-pip.py | python3

# 安装最新版docker
curl -s https://get.docker.com/ | sh

# 启动docker服务
systemctl start docker

# 安装compose
pip install docker-compose 
```

### 使用

```
# 下载项目
wget https://github.com/vulhub/vulhub/archive/master.zip -O vulhub-master.zip
unzip vulhub-master.zip
cd vulhub-master

# 进入某一个漏洞/环境的目录
cd flask/ssti

# 自动化编译环境
docker-compose build

# 启动整个环境
docker-compose up -d
```

测试完成后，删除整个环境

```
docker-compose down -v
```

本项目每个漏洞环境均附带文档，建议你购买1G内存的vps搭建漏洞测试环境，文档中所说的`your-ip`均指你的vps的ip地址，如果你是用虚拟机搭建测试环境，是指你的虚拟机IP，而不是docker容器内部的IP，请不要混淆。

### 注意事项

1.  为防止出现权限错误，最好使用root用户执行docker和docker-compose命令
2.  docker部分镜像不支持在ARM等架构的机器上运行

## 反弹Shell命令一键生成

### 项目发起者

```
https://github.com/0dayCTF
```

### 项目地址

```
https://github.com/0dayCTF/reverse-shell-generator
```

### 项目源码

```
https://github.com/0dayCTF/reverse-shell-generator/archive/refs/heads/main.zip

https://ghproxy.com/https://github.com/0dayCTF/reverse-shell-generator/archive/refs/heads/main.zip
```

### Reverse Shell Generator在线版

```
https://www.revshells.com/

https://forum.ywhack.com/reverse-shell/
```

![image-20220403172326162](https://cdn.jsdelivr.net/gh/Asura88/Mannix/img/202204031723261.png)

![image-20220403172445935](https://cdn.jsdelivr.net/gh/Asura88/Mannix/img/202204031724026.png)

### Docker部署

```
Simply run the following commands within this repository to spin up the instance locally using a Docker container

docker build -t reverse_shell_generator .

docker run -d -p 80:80 reverse_shell_generator

Browse to http://localhost:80
```

```
Last login: Sun Apr  3 17:27:30 on ttys000
mannix@MannixdeMacBook-Pro-2 ~ % cd Desktop/reverse-shell-generator-main
mannix@MannixdeMacBook-Pro-2 reverse-shell-generator-main % ls
Dockerfile			index.html
LICENSE				js
README.md			netlify.toml
Thumbs.db			package.json
assets				parcel-transformer-obfuscation
css				server_functions
favicon.ico
mannix@MannixdeMacBook-Pro-2 reverse-shell-generator-main % docker build -t reverse_shell_generator .
[+] Building 4.2s (7/7) FINISHED
 => [internal] load build definition from Dockerfile                       0.1s
 => => transferring dockerfile: 74B                                        0.0s
 => [internal] load .dockerignore                                          0.0s
 => => transferring context: 2B                                            0.0s
 => [internal] load metadata for docker.io/fnichol/uhttpd:latest           3.5s
 => [internal] load build context                                          0.1s
 => => transferring context: 635.86kB                                      0.1s
 => CACHED [1/2] FROM docker.io/fnichol/uhttpd@sha256:28e6f95cf33ae133652  0.0s
 => => resolve docker.io/fnichol/uhttpd@sha256:28e6f95cf33ae1336525034e2b  0.3s
 => [2/2] COPY . /www                                                      0.1s
 => exporting to image                                                     0.1s
 => => exporting layers                                                    0.1s
 => => writing image sha256:701518d4cb9cb293317a6b4a696fef29b1b671317a27b  0.0s
 => => naming to docker.io/library/reverse_shell_generator                 0.0s

Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
mannix@MannixdeMacBook-Pro-2 reverse-shell-generator-main % docker run -d -p 80:80 reverse_shell_generator
ff1a094ed60aef1fe98ddd17c8989322d39f05b6aceb4e9965bc6cc92a840655
```

