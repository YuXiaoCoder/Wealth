# Homebrew

## 简介

+ `Homebrew`是一款`Mac OS`平台下的软件包管理工具，拥有安装、卸载、更新、查看、搜索等很多实用的功能。

[![Homebrew](https://z3.ax1x.com/2021/04/19/co1nvq.png)](https://imgtu.com/i/co1nvq)

## 安装方法

+ 官方给出的安装方法，将如下命令粘贴到终端即可，详情请参考[《官网》](https://brew.sh/index_zh-cn)，但是这种方法不适合国内的用户，因为网络的原因，下载龟速，实在无法忍受。

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

+ 那我们如何解决呢？解决办法有两种：
  + 科学上网（不推荐）：通过全局代理来进行安装，存在喝茶风险。
  + 替换镜像源（推荐）：将镜像源改为国内镜像源即可。

+ 网上替换镜像源的博文有很多，若熟悉`Shell`脚本或者对此感兴趣值得一看，但是若是仅仅想要快速安装并使用，就略显繁琐了，有爱好者提供了一键换源安装的脚本，让我们来体验一下吧。

```bash
# 内置中科大的镜像源
/bin/bash -c "$(curl -fsSL https://cdn.jsdelivr.net/gh/ineo6/homebrew-install/install.sh)"
```

+ 脚本中内置中科大的镜像源，若需更换镜像源，请参考[《镜像助手》](https://brew.idayer.com/guide/change-source)，若为`M1`芯片的`Mac`，请参考[《M1芯片》](https://brew.idayer.com/guide/m1/)。

## 基本用法

+ 查找软件包：

```bash
brew search [OPTION] PACKAGE
```

+ 查看软件包信息：

```bash
brew info [OPTION] PACKAGE
```

+ 安装软件包：

```bash
brew install [OPTION] PACKAGE
```

+ 卸载软件包：

```bash
brew uninstall [OPTION] PACKAGE
```

+ 列出已安装的软件包：

```bash
brew list [OPTION]
```

+ 更新`Homebrew`自身：

```bash
brew update
```

+ 更新所有安装过的软件包：

```bash
brew upgrade
```

## 常用软件

+ 添加第三方仓库：

```bash
# 字体库
brew tap homebrew/cask-fonts
```

+ `Git`：

```bash
brew install git
```

+ `Mounty`：允许以读写模式在`Mac Book`上挂载`NTFS`盘，[官网](https://mounty.app/)。

```bash
brew install --cask mounty
```

+ `Docker`：开源的容器应用引擎。

```bash
brew install --cask docker
brew install docker-compose
```

+ `Postman`：`API`开发的协作平台，后端调试`API`利器。

```bash
brew install --cask postman
```

+ `Chrome`：谷歌浏览器。

```bash
brew install --cask google-chrome
```

+ 办公软件：

```bash
# 搜狗输入法
https://pinyin.sogou.com/mac/

# QQ
https://im.qq.com/macqq/

# QQ影音
https://player.qq.com/

# 微信
https://mac.weixin.qq.com/

# 迅雷
http://mac.xunlei.com/

# 百度网盘
http://pan.baidu.com/download

# Android File Transfer 用于安卓与 Mac Book 快速传输文件
https://www.android-file-transfer.com/

# TeamViewer 远程访问及支持
https://www.teamviewer.cn/cn/download/mac-os/

# 腾讯看图
https://kantu.qq.com/

# Shadowsocks
https://github.com/shadowsocks/ShadowsocksX-NG/releases

# VNC Viewer
https://www.realvnc.com/en/connect/download/viewer/
```

+ 常用命令：

```bash
brew install tree
brew install telnet
```

***
