# Setup My MacOS

在重装系统、环境同步等情况下。重新配置我的个性化MacOS开发环境 💻

## 📖 Table of Contents

## Basic Settings

1. 增强 MacOS 自带词典，支持朗文、牛津等英英词典、美式发音。参考这篇[文章](https://www.zhihu.com/question/20428599)

## Dev

修改 hosts 文件

```bash
sudo vi /etc/hosts
```

terminal or iterm 使用快捷键 `CMD +` 放大 🔍 窗口

### Editor

VSCode

### Python3 Environment

todo 

### ☕️ Java Environment

- jdk
- maven
- idea
...

[IntellIJ IDEA](https://www.jetbrains.com/idea/download/download-thanks.html?platform=macM1) support Apple Silicon!!!

1. Ultimate 版激活码
2. 把 `idea <path to the folder>` 添加到命令行启动 `Tools > Create Command-line Launcher`

## Reading

iPage

[MacOS高效的读书笔记方法](https://www.youtube.com/watch?v=4Jg10PAmd08&list=PLbkko9cqTctew4zvXeeyfWJffQ7omfW1D&index=24)

Markdown Editor
PDF Export

欧陆词典

## Work with iPad

...

## 基本快捷键

- 聚焦搜索：CMD + 空格


## todo

[MacOS Web Dev Setup](https://github.com/fabien-h/macos-web-dev-setup#-install-docker)
...

## dev-setup.sh

```bash
xcode-select --install
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
brew cask install iterm2
# update iterm2 settings -> colors, keep directory open new shell, keyboard shortcuts
brew install bash # latest version of bash
# set brew bash as default shell
brew install fortune
brew install cowsay 
brew install git
brew install vcprompt
# update bash_profile
brew cask install spectacle
brew cask install alfred
# set CMD+space to launch alfred
brew cask install firefox
# install nvm/node
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
nvm install stable
mkdir ~/workspace
npm install -g lite-server eslint
brew cask install visual-studio-code
# update vscode settings
# install vscode extensions 
```

1. 安装 xcode
2. 安装 [Homebrew](http://brew.sh)
3. 使用 `brew case` 安装 iTerm2
4. 配置 iTerm2 主题为 `Minimal`
5. 配置 iTerm2 默认 Profile 的窗口字体大小为 `24` 前景色为 `#5acd5a`. 第一个配置项位置  `Preferences-Profiles-Text-Font` 第二个配置项位置：`Preferences-Profiles-Colors-Foreground`
6. todo 配置 iTerm2 快捷键行为
7. todo 安装最新版本的 bash. 并将将 bash 切换为最新的 /usr/local/bin/bash // ❌ M1 Mac 无法更新成功

说明: MacOS 默认的 shell 是 `zsh`, 但是我更喜欢使用 `bash`. 可以使用 `bash --version` 查看 bash 的版本. 使用 `echo "$SHELL"` 查看当前使用的 shell 名称.

```zsh
which bash

sudo nano /etc/shells

chsh -s /usr/local/bin/bash
```

8. todo 安装 fortune 和 cowsay // ❌ M1 Mac 无法更新成功

```zsh
fortune | cowsay

# 企鹅
cowsay -f tux hello 
```

9. todo vcprompt 自定义 .bash_profile
10. todo 安装 spectacle // ❌ M1 Mac 无法更新成功 使用这个替代 https://rectangleapp.com/
11. 安装 alfred
12. todo 安装 hyperSwitch
13. some stuff ... 浏览器插件等

https://gist.github.com/w3cj/76cd9fb9f346e153b6f0dc46fd025620

os-x-setup-commands.sh

vs-code-extensions.txt

## vscode 

To make the transition from one computer to another seamless, VS Code has a sweet extension by the name of Settings Sync, which lets you upload your configurations to a GitHub Gist. Once they are up on GitHub, the extension takes care of keeping the following files in sync: settings file, keybindings, snippets, workspace folders, and extensions and their corresponding configurations.

The extension’s page has a thorough explanation on how to get it set up and should only take a couple of minutes to have your VS Code with your preferred settings.
