+++
date = '2025-09-02T17:49:30+08:00'
draft = false
title = 'ZSH安装和配置'
+++
[TOC]

# 1 安装

# 1.1 安装zsh

```
安装zsh
sudo apt-get install zsh
看下zsh的位置
which zsh
将上述步骤中的zsh设置为默认的Shell
chsh -s /bin/zsh
```

## 1.2 安装 on my zsh

```bash
# 下载所需的构建工在这里插入代码片具和依赖项
apt-get -y install build-essential nghttp2 libnghttp2-dev libssl-dev

# 使用一行命令安装(第一行可以)
#方式1 curl
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
#方式2 wget
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
#方式3 fetch
sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 切换风格
vi ~/.zshrc
## 修改
#ZSH_THEME="robbyrussell"
ZSH_THEME="ys"

# 新风格ok 
```

# 2 FAQ 

## 2.1 问题1

```zsh
# 报错
zsh: corrupt history file /home/XXX/.zsh_history
# 解决方法
cp .zsh_history zsh_history
rm -f .zsh_history 
strings zsh_history .zsh_history
#OK了，修复成功。
```




