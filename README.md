# Setup My Silicon Mac

✨💻 在重装系统、环境同步等情况下。重新配置我的个性化MacOS开发环境。

## 📖 Table of Contents

- [⚙️ Basic Settings](#-basic-settings)
  - [Dock](#dock)
  - [Finder](#finder)
- [📚 Dictionary](#-dictionary)
- [📦 App](#-app)
- [👨🏻‍💻 Dev](#-dev)
  - [os-x-setup-commands](#os-x-setup-commands)
  - [安装并配置 VSCode]
  - [配置 Java 开发环境]
  - [配置 Python3 开发环境]
  - [配置 Node 开发环境]
  - [Docker]
  - [Firefox]
  - [其它]
- [Work with iPad]
- [Mac OS Shortcuts]
- [其它]

## ⚙️ Basic Settings

### Dock

移除不常用的 APP

> 使用 <kbd>CMD</kbd> + <kbd>Space</kbd> 打开 Finder, Empty Trash 等其它 APP , 不要太依赖 Dock.

### Finder

1. 将常用的文件夹移动到个人收藏下. 例如 root根目录(前往-电脑)

> 在 Finder 中使用快捷键 <kbd>CMD</kbd> + <kbd>Shift</kbd> + <kbd>H</kbd> , 能够马上回到当前用户的家目录. 

2. 设置 Finder Preferences

> 大多数 MacOS 的 APP 都可以使用 <kbd>CMD</kbd> + <kbd>,</kbd> 打开偏好设置. 

3. 设置 Tags
4. 显示-显示状态栏
5. 显示-显示路径栏
6. 显示-显示标签页栏

## 📚 Dictionary

1. [hallelujahIM](https://github.com/dongyuwei/hallelujahIM/blob/master/README-En.md) 智能英文拼写补全, 拥有英文写作 ✏️
2. [Bob](https://github.com/ripperhe/Bob) 截图翻译
3. [grammarly](https://www.grammarly.com/native/mac) 英文写作语法纠正
4. 开启 MacOS 内置单词、句子发音. 系统偏好设置 - 辅助功能 - 朗读内容 - ☑️ 朗读所选内容. 开启之后使用快捷键触发 <kbd>Opt</kbd> + <kbd>ESC</kbd>
5. 强制唤醒内置词典 <kbd>Ctrl</kbd> + <kbd>CMD</kbd> + <kbd>D</kbd>
6. 增强 alfred 支持快捷翻译 `tr concurrent`. 配置方式参考[这里](https://www.alfredapp.com/blog/tips-and-tricks/dont-get-lost-in-translation/)
7. 增强 MacOS 自带词典. [《柯林斯双解》for macOS](https://placeless.net/blog/macos-dictionaries). 也可参考[文章](https://www.zhihu.com/question/20428599)
8. 安装欧陆词典

## 📦 App

1. Spoitfy
2. Twitter
3. 印象笔记
4. 微信
5. 百度网盘
6. todo VPN
7. 坚果云
8. todo 换掉 Typora
9. 有道云笔记
10. Xmind // 幕布
11. OneDrive
12. Omniplayer
13. todo 换掉 WPS
14. Unarchiver 压缩、解压工具
15. GoodNotes 5

<details>
<summary>一个待办</summary>
<code style="white-space:nowrap;">todo 设置 iPage</code>
</details>

## 👨🏻‍💻 Dev

### os-x-setup-commands

```bash dev-setup.sh
xcode-select --install

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update

brew cask install iterm2
# 配置 iTerm2 主题为 Minimal
# 配置 iTerm2 默认 Profile 的窗口字体大小为 24, 前景色为 #5acd5a. 
# 第一个配置项位置: Preferences-Profiles-Text-Font, 第二个配置项位置: Preferences-Profiles-Colors-Foreground.
# TODO 配置 iTerm2 快捷键行为 

# oh my zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

brew install git
brew install vcprompt
# TODO update bash_profile. 配置 history, alias 等

brew install --cask rectangle

brew cask install alfred
# set CMD+space to launch alfred
# CMD + L 放大关键词

brew install --cask firefox

# TODO 安装 hyperSwitch // Silicon Mac 暂不支持 
# https://isapplesiliconready.com/zh/app/HyperSwitch

# install nvm/node
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
nvm install stable

mkdir ~/dev

#npm install -g lite-server eslint

brew install --cask visual-studio-code
# update vscode settings
# install vscode extensions 
```

### 修改 hosts 文件

```bash
sudo vi /etc/hosts
```

### 安装并配置 VSCode

安装 `code .`。 <kbd>CMD</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> 选择 install 'code' command in PATH.

参考插件清单 [user:w3cj](https://gist.github.com/w3cj/520eb023dd3531d1b654794f65aa434b) 并使用脚本直接批量安装, 例如 `hile read line; do code --install-extension "$line";done < vscode-extensions.txt`

安装插件 Settings Sync

设置 [参考](https://github.com/CodingGarden/vscode-settings)

打开终端 <kbd>CMD</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> 输入 `>toggle int` 

### 配置 Java 开发环境

TODO JDK MAVEN

[IntellIJ IDEA](https://www.jetbrains.com/idea/download/download-thanks.html?platform=macM1)

1. Ultimate 版激活码
2. 把 `idea <path to the folder>` 添加到命令行启动 `Tools > Create Command-line Launcher`

### 配置 Python3 开发环境

MacOS 默认py为2.0

### 配置 Node 开发环境

安装 [nvm](https://github.com/nvm-sh/nvm#install--update-script)

```bash
nvm list
nvm install 14

node -v
npm -v
```

### Docker

todo

### Firefox

快捷键

<kbd>Control</kbd> + <kbd>Tab</kbd> 支持预览切换标签页

about:config 搜索 browser:ctrlTab:recentlyUsedOrder false 可关闭预览标签页

偏好设置

- [x] General - Restore previous session
- [x] General - Warn you when quitting the browser 
- [x] Home - Homepage and new windows - Google
- [x] Home - New tabs - Blank
- [x] Search - Default Search Engine - DuckDuckGo

> DuckDuckGo 支持快速搜索, 例如 !gh better google

- [ ] Search - Search Suggestions. uncheck that, only show my search history.

插件

- tabliss.io 标签页皮肤
- [uBlock Origin](https://github.com/gorhill/uBlock#firefox--firefox-for-android) 广告拦截
- Privacy Badger // EFF 
- [OneTab](https://addons.mozilla.org/en-US/firefox/addon/onetab/) 标签管理
- JSON Viewer 火狐浏览器默认支持, [点击](https://www.reddit.com/r/javascript.json)测试
- HTTPS Everywhere // EEF
- [Stylus](https://addons.mozilla.org/en-US/firefox/addon/styl-us/) 设置不同网站的自定义样式. 例如
  - [Github Dark](https://github.com/StylishThemes/GitHub-Dark)
  - [Wikipedia Dark](https://github.com/StylishThemes/Wikipedia-Dark)
- [Tamper Monkey](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/)
  - [greasyfork.org](https://greasyfork.org/en)
  - [Better Google](https://github.com/aligo/better-google)
  - 如何自己开发浏览器脚本 先挖个坑😄
- [Vue DevTools](https://github.com/vuejs/vue-devtools)
- [React DevTools](https://addons.mozilla.org/en-US/firefox/addon/react-devtools/)

审查元素

- Settings - Themes - Dark

### 其它

Postman

微信开发者工具

Sourcetree

## Work with iPad

todo [MacOS高效的读书笔记方法](https://www.youtube.com/watch?v=4Jg10PAmd08&list=PLbkko9cqTctew4zvXeeyfWJffQ7omfW1D&index=24)

## Mac OS Shortcuts

- 聚焦搜索：CMD + 空格

## 其它

todo

说明: MacOS 默认的 shell 是 `zsh`, 但是我更喜欢使用 `bash`. 可以使用 `bash --version` 查看 bash 的版本. 使用 `echo "$SHELL"` 查看当前使用的 shell 名称.

```zsh
which bash

sudo nano /etc/shells

chsh -s /usr/local/bin/bash
```

12. todo 安装 hyperSwitch
13. some stuff ... 浏览器插件等

https://gist.github.com/w3cj/76cd9fb9f346e153b6f0dc46fd025620

https://gist.github.com/w3cj?page=4

[MacOS Web Dev Setup](https://github.com/fabien-h/macos-web-dev-setup#-install-docker)

```bash
brew install fortune
brew install cowsay 
# 企鹅
# cowsay -f tux hello 
```

Airpods 和 Mac 交互

Jsonserver
