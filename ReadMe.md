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

```bash
git clone https://ghproxy.com/https://github.com/stilleshan/ServerStatus
```

#### **wget & curl**

```bash
wget https://ghproxy.com/https://github.com/stilleshan/ServerStatus/archive/master.zip
wget https://ghproxy.com/https://raw.githubusercontent.com/stilleshan/ServerStatus/master/Dockerfile
curl -O https://ghproxy.com/https://github.com/stilleshan/ServerStatus/archive/master.zip
curl -O https://ghproxy.com/https://raw.githubusercontent.com/stilleshan/ServerStatus/master/Dockerfile
```

### 首页下载

在本页地址栏输入合规链接（参考以下链接）点击下载按钮

支持 raw.githubusercontent.com , gist.github.com , gist.githubusercontent.com 文件下载.

#### **Raw 文件**

```http
https://raw.githubusercontent.com/stilleshan/ServerStatus/master/Dockerfile
```

#### **分支源码**

```http
https://github.com/stilleshan/ServerStatus/archive/master.zip
```

#### **Releases 源码**

```http
https://github.com/stilleshan/ServerStatus/archive/v1.0.tar.gz
```

#### **Releases 文件**

```http
https://github.com/fatedier/frp/releases/download/v0.33.0/frp_0.33.0_linux_amd64.tar.gz
```

### 镜像站

```http
https://mirror.ghproxy.com/

https://gh.api.99988866.xyz/
```

## PiQi文库

### 项目发起者

```http
https://github.com/PeiQi0
```

### 项目地址

```http
https://github.com/PeiQi0/PeiQi-WIKI-Book
```

### 源码地址

```http
https://github.com/PeiQi0/PeiQi-WIKI-Book/archive/refs/heads/main.zip

https://ghproxy.com/https://github.com/PeiQi0/PeiQi-WIKI-Book/archive/refs/heads/main.zip
```

### [PeiQi-WIKI-Book-2022-03-20](https://github.com/PeiQi0/PeiQi-WIKI-Book/releases/tag/PeiQi-WIKI-Book-2022-03-20)

```http
https://github.com/PeiQi0/PeiQi-WIKI-Book/releases/download/PeiQi-WIKI-Book-2022-03-20/PeiQi-WIKI-Book-HTML.zip

https://ghproxy.com/https://github.com/PeiQi0/PeiQi-WIKI-Book/releases/download/PeiQi-WIKI-Book-2022-03-20/PeiQi-WIKI-Book-HTML.zip
```

### 本地搭建

文库支持多种快捷的方式在本地搭建随时查阅文库，项目图片均为本地化，推荐Docker或内网搭建，不推荐公网服务器部署

#### Yarn源码搭建 (个人二次扩展，需要编译环境)

```bash
git clone https://github.com/PeiQi0/PeiQi-WIKI-Book.git
cd PeiQi-WIKI-Book
yarn add vuepress-theme-antdocs -d
yarn install
yarn run dev
```

#### Html源码搭建 (无需编译环境，使用编译好的Html文件直接部署)

```bash
git clone https://github.com/PeiQi0/PeiQi-WIKI-Book.git
cd PeiQi-WIKI-Book/docs/.vuepress/dist
mv * 你的服务器Web目录
```

#### Docker搭建 (只需要Dokcer环境，快速搭建在各个环境中)

```bash
docker search peiqipeiqi
docker pull peiqipeiqi/peiqi_wiki:220320
docker run -t -d -p 65534:80 --name "PeiQi_Wiki" peiqipeiqi/peiqi_wiki:220320
User/Pass: peiqi:peiqi
```

### PeiQi文库在线版

```http
http://wiki.peiqi.tech/
```

![image-20220403170612630](https://cdn.jsdelivr.net/gh/Asura88/Mannix/img/202204031706714.png)

## Vulhub

### 项目发起者

```http
https://github.com/vulhub
```

### 项目地址

```http
 https://github.com/vulhub/vulhub
```

### 源码地址

```http
https://github.com/vulhub/vulhub/archive/refs/heads/master.zip

https://ghproxy.com/https://github.com/vulhub/vulhub/archive/refs/heads/master.zip
```

### 安装

在Ubuntu 20.04下安装docker/docker-compose:

```bash
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

```bash
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

```bash
docker-compose down -v
```

本项目每个漏洞环境均附带文档，建议你购买1G内存的vps搭建漏洞测试环境，文档中所说的`your-ip`均指你的vps的ip地址，如果你是用虚拟机搭建测试环境，是指你的虚拟机IP，而不是docker容器内部的IP，请不要混淆。

### 注意事项

1.  为防止出现权限错误，最好使用root用户执行docker和docker-compose命令
2.  docker部分镜像不支持在ARM等架构的机器上运行

## 反弹Shell命令一键生成

### 项目发起者

```http
https://github.com/0dayCTF
```

### 项目地址

```http
https://github.com/0dayCTF/reverse-shell-generator
```

### 项目源码

```http
https://github.com/0dayCTF/reverse-shell-generator/archive/refs/heads/main.zip

https://ghproxy.com/https://github.com/0dayCTF/reverse-shell-generator/archive/refs/heads/main.zip
```

### Reverse Shell Generator在线版

```http
https://www.revshells.com/

https://forum.ywhack.com/reverse-shell/
```

![image-20220403172326162](https://cdn.jsdelivr.net/gh/Asura88/Mannix/img/202204031723261.png)

![image-20220403172445935](https://cdn.jsdelivr.net/gh/Asura88/Mannix/img/202204031724026.png)

### Docker部署

```bash
Simply run the following commands within this repository to spin up the instance locally using a Docker container

docker build -t reverse_shell_generator .

docker run -d -p 80:80 reverse_shell_generator

Browse to http://localhost:80
```

```bash
Last login: Sun Apr  3 17:27:30 on ttys000
mannix@MannixdeMacBook-Pro-2 ~ % cd Desktop/reverse-shell-generator-main
mannix@MannixdeMacBook-Pro-2 reverse-shell-generator-main % ls
Dockerfile          index.html
LICENSE             js
README.md           netlify.toml
Thumbs.db           package.json
assets              parcel-transformer-obfuscation
css             server_functions
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

## Viper(炫彩蛇)

- Viper(炫彩蛇)是一款图形化内网渗透工具,将内网渗透过程中常用的战术及技术进行模块化及武器化.
- Viper(炫彩蛇)集成杀软绕过,内网隧道,文件管理,命令行等基础功能.
- Viper(炫彩蛇)当前已集成70+个模块,覆盖初始访问/持久化/权限提升/防御绕过/凭证访问/信息收集/横向移动等大类.
- Viper(炫彩蛇)目标是帮助红队工程师提高攻击效率,简化操作,降低技术门槛.
- Viper(炫彩蛇)支持在浏览器中运行原生msfconsole,且支持多人协作.

### 项目发起者

```http
https://github.com/FunnyWolf
```

### 项目地址

```http
https://github.com/FunnyWolf/Viper
```

### 源码地址

```http
https://github.com/FunnyWolf/Viper/archive/refs/heads/master.zip

https://ghproxy.com/https://github.com/FunnyWolf/Viper/archive/refs/heads/master.zip
```

### [v1.5.19 20220328](https://github.com/FunnyWolf/Viper/releases/tag/v1.5.19)

```
优化
Session文件管理增加缓存,优化首次打开速度
合并metasploit-framework 6.1.36版本
Bugfix
修复无法使用migrate命令问题
修复无法创建虚拟监听问题
修复Windows UAC绕过运行报错问题
```

```htt
https://github.com/FunnyWolf/Viper/archive/refs/tags/v1.5.19.zip

https://ghproxy.com/https://github.com/FunnyWolf/Viper/archive/refs/tags/v1.5.19.zip
```

### **首次安装**

#### 脚本安装

f8x工具支持在全新的linux环境一键安装viper,命令如下:

```bash
curl -o f8x https://f8x.io/   # wget -O f8x https://f8x.io/
bash f8x -viper
```

### **更新版本**

#### 小版本更新(例如1.2.1更新到1.2.2)

docker-compose所有命令在/root/VIPER目录执行

删除原有容器

```bash
cd /root/VIPER              # viper安装目录
docker-compose down         # 删除现有容器
```

更新 docker 镜像

```bash
docker-compose pull
```

新建并启动容器

```bash
docker-compose up -d
```

**访问**  [**https://vpsip:d**](http://vpsip:60000)**iyport 登录服务器.用户名:root 密码:****自定义密码**

密码可以通过 `cat /root/VIPER/docker-compose.yml` 查看

diyport可通过 `cat /root/VIPER/nginxconfig/viper.conf` 查看

#### 跨版本更新(例如1.2.6更新到1.3.0)

docker-compose所有命令在/root/VIPER目录执行

**Viper高版本不兼容低版本已有数据,跨版本更新需要清空已有数据**

删除原有容器

```bash
cd /root/VIPER # viper安装目录
docker-compose down
```

清空已有数据及自定义模块

```bash
rm -f ./db/*
rm -f ./module/*
```

更新 docker 镜像

```bash
docker-compose pull
```

新建并启动容器

```bash
docker-compose up -d
```

**访问**  [**https://vpsip:d**](http://vpsip:60000)**iyport 登录服务器.用户名:root 密码:****自定义密码**

密码可以通过 `cat /root/VIPER/docker-compose.yml` 查看

diyport可通过 `cat /root/VIPER/nginxconfig/viper.conf` 查看

![img](https://camo.githubusercontent.com/92106ea9b268f31573e7365b0a31642dfdd5d313cc0da46fa7531ebb3097e063/68747470733a2f2f63646e2e6e6c61726b2e636f6d2f79757175652f302f323032312f706e672f3135393235392f313632383537333037393031342d38373164303537332d656632612d343236372d393734622d3130323664366564323436362e706e673f782d6f73732d70726f636573733d696d616765253246726573697a65253243775f313530342532436c696d69745f30)

## alist

*一个支持多存储的文件列表程序，使用 Gin 和 React 。*

### 支持

- 多种存储
  -  本地存储
  -  [阿里云盘](https://www.aliyundrive.com/)
  -  OneDrive / Sharepoint（[国际版](https://www.office.com/), [世纪互联](https://portal.partner.microsoftonline.cn/),de,us）
  -  [天翼云盘](https://cloud.189.cn/) (个人云, 家庭云)
  -  [GoogleDrive](https://drive.google.com/)
  -  [123云盘](https://www.123pan.com/)
  -  [蓝奏云](https://pc.woozooo.com/)
  -  [Alist](https://github.com/Xhofe/alist)
  -  FTP
  -  [PikPak](https://www.mypikpak.com/)
  -  [闪电盘](https://shandianpan.com/)
  -  [S3](https://aws.amazon.com/cn/s3/)
  -  WebDav
  -  Teambition（[中国](https://www.teambition.com/)，[国际](https://us.teambition.com/)）
  -  [分秒帧](https://www.mediatrack.cn/)
  -  [和彩云](https://yun.139.com/) (个人云, 家庭云)
  -  [Yandex.Disk](https://disk.yandex.com/)
  -  [百度网盘](http://pan.baidu.com/)
  -  [夸克网盘](https://pan.quark.cn/)
  -  [迅雷云盘](https://pan.xunlei.com/)
-  部署方便，开箱即用
-  文件预览（PDF、markdown、代码、纯文本……）
-  画廊模式下的图像预览
-  视频和音频预览（mp4、mp3 等）
-  Office 文档预览（docx、pptx、xlsx、...）
-  `README.md` 预览渲染
-  文件永久链接复制和直接文件下载
-  黑暗模式
-  国际化
-  受保护的路由（密码保护和身份验证）
-  WebDav（具体见https://alist-doc.nn.ci/docs/webdav ）
-  [Docker 部署](https://hub.docker.com/r/xhofe/alist)
-  Cloudflare workers 中转
-  文件/文件夹打包下载
-  支持视频列表播放和字幕(ass,srt,vtt)
-  网页上传(可以允许访客上传)，删除，新建文件夹，重命名，移动，复制 

### 项目发起者

```http
https://github.com/Xhofe
```

### 项目地址

```http
https://github.com/Xhofe/alist
```

### 源码地址

```http
https://github.com/Xhofe/alist/archive/refs/heads/v2.zip

https://ghproxy.com/https://github.com/Xhofe/alist/archive/refs/heads/v2.zip
```

### [v2.3.2](https://github.com/Xhofe/alist/releases/tag/v2.3.2)

```http
https://github.com/Xhofe/alist/releases/download/v2.3.2/alist-darwin-10.12-amd64.tar.gz

https://ghproxy.com/https://github.com/Xhofe/alist/releases/download/v2.3.2/alist-darwin-10.12-amd64.tar.gz

https://github.com/Xhofe/alist/releases/download/v2.3.2/alist-linux-amd64.tar.gz

https://ghproxy.com/https://github.com/Xhofe/alist/releases/download/v2.3.2/alist-linux-amd64.tar.gz

https://github.com/Xhofe/alist/releases/download/v2.3.2/alist-windows-4.0-amd64.zip

https://ghproxy.com/https://github.com/Xhofe/alist/releases/download/v2.3.2/alist-windows-4.0-amd64.zip

https://github.com/Xhofe/alist/archive/refs/tags/v2.3.2.zip

https://ghproxy.com/https://github.com/Xhofe/alist/archive/refs/tags/v2.3.2.zip
```

### 一键脚本

仅支持Linux-x86_64/aarch64平台。

#### 安装

```bash
curl -fsSL "https://nn.ci/alist.sh" | bash -s install
```

已经安装过再次执行安装会删除之前的数据，更新请使用更新命令。

#### 更新

```bash
curl -fsSL "https://nn.ci/alist.sh" | bash -s update
```

#### 卸载

```bash
curl -fsSL "https://nn.ci/alist.sh" | bash -s uninstall
```

#### 自定义路径

默认安装在`/opt/alist`，要自定义安装路径，添加安装路径为第二个参数，必须是绝对路径（路径以alist结尾时直接安装到给定路径，否则会安装在给定路径alist目录下），如安装到`/root`：

```bash
# 安装
curl -fsSL "https://nn.ci/alist.sh" | bash -s install /root
# 更新
curl -fsSL "https://nn.ci/alist.sh" | bash -s update /root
# 卸载
curl -fsSL "https://nn.ci/alist.sh" | bash -s uninstall /root
```