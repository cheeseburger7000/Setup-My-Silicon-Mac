# Setup Apple Silicon Mac

✨💻 在重装系统、环境同步等情况下。重新配置我的个性化MacOS开发环境。

## 📚 词典

1. 开启 MacOS 内置单词、句子发音. 系统偏好设置 - 辅助功能 - 朗读内容 - ☑️ 朗读所选内容. 开启之后使用快捷键触发 <kbd>Opt</kbd> + <kbd>ESC</kbd>
2. 增强 MacOS 自带词典. [《柯林斯双解》for macOS](https://placeless.net/blog/macos-dictionaries). 也可参考[文章](https://www.zhihu.com/question/20428599)
3. 安装欧陆词典

> 强制唤醒内置词典 <kbd>Ctrl</kbd> + <kbd>CMD</kbd> + <kbd>D</kbd>

## 👨🏻‍💻 Dev环境

1. 执行脚本

```sh
xcode-select --install

# Homebrew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update

# iTerm2
brew cask install iterm2

# Git
brew install git
git config --global user.name "Luca" 
git config --global user.email "shaohsiung@163.com"
git config --global url."https://github.com.cnpmjs.org/".insteadOf "https://github.com/" # 配置国内 GitHub 镜像网站
git config --global credential.helper store # 保存用户名和密码
git config --global core.quotepath off
# git lfs install --skip-repo # 解决 GitHub 限制最大只能克隆 100M 的仓库
brew install vcprompt

# Oh my zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
# Plugins
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
# 解决使用agnoster主题导致终端乱码
git clone https://github.com/powerline/fonts.git
cd fonts/
./install.sh
# 解决使用agnoster主题导致VS Code控制台乱码
git clone https://github.com/abertsch/Menlo-for-Powerline.git
cd Menlo-for-Powerline
sudo mv "Menlo for Powerline.ttf" ~/Library/Fonts
# VS Code -> User Settings - Terminal Font Family 设置字体为 Menlo for Powerline

# NVM
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
nvm install stable

mkdir ~/dev
mkdir ~/bin

brew install --cask alfred
brew install --cask rectangle
brew install --cask firefox
brew install --cask visual-studio-code
```

2. 配置 `.zshrc` 相关配置参见 [dotfiles]() 这个仓库
3. 安装 Docker Desktop, 并配置国内 Docker 加速镜像 参加有道云笔记
3. 设置 SSH 会话不超时, 配置文件的位置`/etc/ssh/ssh_config`

```zsh
 Host *
   SendEnv LANG LC_*
+  # 每60秒给SSH服务器发送KeepAlive请求，保证终端不会因为超时空闲而自动断开连接
+  ServerAliveInterval 60
```

4. 搭建 Python3 环境
5. 搭建 Java 环境: JDK, MVN等
4. 搭建 GO环境

# 📘 VSCode

1. 安装 `code .`。 <kbd>CMD</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> 选择 install 'code' command in PATH.
2. 参考插件清单 [user:w3cj](https://gist.github.com/w3cj/520eb023dd3531d1b654794f65aa434b) 并使用脚本直接批量安装, 例如 `hile read line; do code --install-extension "$line";done < vscode-extensions.txt`, 安装插件 Settings Sync
3. 设置 [参考](https://github.com/CodingGarden/vscode-settings)

# 🔎 Alfred

1. 增强 alfred 支持快捷翻译 `tr concurrent`. 配置方式参考[这里](https://www.alfredapp.com/blog/tips-and-tricks/dont-get-lost-in-translation/)
2. 配置Google翻译, 发音等 `https://www.google.com/search?q=how%20to%20pronounce%20{query}`
3. 参考
    - [高效进阶](https://ihtcboy.com/2020/02/09/2020-02-09_%E7%A8%8B%E5%BA%8F%E5%91%98%E7%9A%84macOS%E7%B3%BB%E5%88%97%EF%BC%9A%E9%AB%98%E6%95%88Alfred%E8%BF%9B%E9%98%B6/)
    - [Search Web Like a Pro](https://www.makeuseof.com/tag/alfred-mac-search-tips/)
    - [Windows Wox](https://sspai.com/post/33460) Win平台类似产品

# ⌨️ Touch bar

TODO

# 📦 App

笔记、脑图

- [x] 印象笔记
- [x] 有道云笔记
- [ ] 幕布
- [x] XMind
- [x] GoodNotes 5
- [x] PDF Expert

网盘

- [ ] 阿里网盘
- [x] 百度网盘
- [x] 坚果云
- [x] OneDrive 
  
社交软件

- [ ] Spoitfy
- [ ] Twitter
- [ ] 微信
- [ ] Line 台湾地区
- [ ] 钉钉

代理

- [x] Brook
- [x] Lantern
- [ ] ShadowsocksX-NG

开发

- [ ] Postman
- [x] 微信开发者工具
- [ ] Sourcetree
- [x] VirtualBox
- [x] IntelliJ
- [x] GoLand
- [x] DataGrip
- [x] PyCharm
- [x] Navicat Premium 百度云DMG包
- [x] Redis Manager 百度云DMG包
- [x] Charles

通用

- [x] OmniPlayer 播放器
- [x] WPS
- [x] Unarchiver 压缩、解压工具
- [x] 欧陆词典
