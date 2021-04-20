# 终端

## 简介

+ 对于开发者来说，你或多或少地都会接触到命令行，甚至很多程序员只在终端下就能完成大部分工作，所以一个易用又漂亮的终端配置教程来了。

[![终端之美](https://z3.ax1x.com/2021/04/20/c7gFC4.md.png)](https://imgtu.com/i/c7gFC4)

## iTerm2

### 安装

+ 官网：[《链接》](https://www.iterm2.com/downloads.html)。

```bash
brew install iterm2
```

### 配色

+ 官网：[《链接》](https://github.com/mbadolato/iTerm2-Color-Schemes)。
  + `https://github.com/mbadolato/iTerm2-Color-Schemes/blob/master/schemes/Solarized%20Dark%20Higher%20Contrast.itermcolors`。

+ 将配色方案内容复制并保存为本地文件(`SolarizedDarkHigherContrast.itermcolors`)，然后双击安装。
+ `iTerm2 ==> Preferences ==> Profiles ==> Colors ==> Colors Presets ==> SolarizedDarkHigherContrast`。

### 字体

+ 官网：[《链接》](https://www.nerdfonts.com/)。

```bash
brew install --cask font-hack-nerd-font
```

+ `iTerm2 ==> Preferences ==> Profiles ==> Text ==> Font ==> Hack Nerd Font Mono ==> Regular ==> 14`。


### 背景图片

+ `iTerm2 ==> Preferences ==> Profiles ==> Window ==> Background Image ==> Enabled`，选择自己喜欢的背景图即可。
+ 推荐背景图：[《地图》](https://imgtu.com/i/c72v7V)、[《鬼刀》](https://imgtu.com/i/c7RW34)。

### 回滚缓冲区

+ 无限缓冲区，防止执行命令的输出过多，导致无法查询执行结果。
+ `iTerm2 ==> Preferences ==> Profiles ==> Terminal ==> Scrollback Buffer ==> Unlimited scrollback`。

### 克隆会话

+ 避免重复输入登录堡垒机的口令：`iTerm2 ==> Preferences ==> General ==> Working Directory ==> Reuse previous sessions’s directory`。

+ 配置`SSH`：

```bash
vim ~/.ssh/config
```

```ini
Host *
  User root
  Port 22
  ControlMaster auto
  ControlPath ~/.ssh/master-%r@%h:%p
```

### 科学上网

+ 设置环境变量：

```bash
# 需要科学上网的客户端
export all_proxy="socks5://127.0.0.1:1080"
```

+ 测试：

```bash
curl https://api.myip.com
```

+ 撤销环境变量：

```bash
unset all_proxy
```

## OhMyZsh

### 安装

+ `Mac Book`一般自带了`Zsh`，无需额外安装，修改默认的`Shell`为`Zsh`。

```bash
chsh -s /bin/zsh
```

+ `OhMyZsh`：轻松配置`Zsh`，快速提高工作效率。

```bash
# GitHub
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Gitee 推荐国内用户使用
sh -c "$(curl -fsSL https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh)"
```

### 主题

+ 官网：[《链接》](https://github.com/ohmyzsh/ohmyzsh/wiki/themes)。

+ 克隆主题仓库到`OhMyZsh`的用户自定义主题目录中：

```bash
# GitHub
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k

# Gitee 推荐国内用户使用
git clone --depth=1 https://gitee.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

+ 设置`~/.zshrc`中的变量：

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

+ 配置主题：

```bash
# 在终端执行交互式命令进行配置
p10k configure

# Install Meslo Nerd Font?(下载字体)：No
# Does this look like a diamond (rotated square)?(钻石图标)：Yes
# Does this look like a lock?(锁图标)：Yes
# Does this look like a Debian logo (swirl/spiral)?(Debian Logo)：Yes
# Do all these icons fit between the crosses?：Yes
# Prompt Style(提示样式)：Rainbow
# Character Set(字符集)：Unicode
# Show current time?(显示当前时间)：24-hour format
# Prompt Separators(提示分隔符)：Angled
# Prompt Heads(提示头部)：Sharp
# Prompt Tails(提示尾部): Blurred
# Prompt Height(提示高度)：One line
# Prompt Spacing(提示间距)：Compact
# Icons(图标)：Many icons
# Prompt Flow(提示流): Fluent
# Enable Transient Prompt(瞬时提示): No
# Instant Prompt Mode(即时提醒)：Verbose
# 是否覆盖已存在的配置文件：Yes
# 是否应用配置文件：Yes
```

### 插件

+ 设置`~/.zshrc`中的变量：

```bash
plugins=(
    git
    colored-man-pages
    colorize
    github
    brew
    osx
    autojump
    zsh-autosuggestions
    zsh-syntax-highlighting
)
```

+ `autojump`：可以用于直达常用目录。

```bash
brew install autojump
```

+ `zsh-autosuggestions`：补全历史输入的命令，用方向键`->`即可补全。

```bash
# GitHub
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# Gitee 推荐国内用户使用
git clone https://gitee.com/pocmon/zsh-autosuggestions.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

+ `zsh-syntax-highlighting`：语法高亮显示。

```bash
# GitHub
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Gitee 推荐国内用户使用
git clone https://gitee.com/mo2/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

***
