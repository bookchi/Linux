## 安装oh my zsh
oh my zsh是Linux下很好用的一个终端，这里就介绍一些如何安装这个终端。

### 1 安装oh-my-zsh
``` sh
# 安装zsh
sudo apt-get install zsh
# 修改默认终端为zsh
chsh -s /bin/zsh 
# 安装oh-my-zsh
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```
### 2 安装插件
``` sh
# 下载自动补全插件
wget http://mimosa-pudica.net/src/incr-0.2.zsh
# 将插件放到相应目录下
sudo mkdir ~/.oh-my-zsh/plugins/incr/
sudo mv incr-0.2.zsh ~/.oh-my-zsh/plugins/incr/incr-0.2.zsh
sudo vim ~/.zshrc
# 末尾添加代码
source ~/.oh-my-zsh/plugins/incr/incr*.zsh
# 修改主题
ZSH_THEME = 'agnoster'
# 更新配置
source ~/.zshrc
```

### 3 安装字体
安装好后，字体可能是乱码，需要安装powerline字体才能正常显示。
``` sh
# 下载字体
git clone https://github.com/powerline/fonts.git
# 安装字体
cd fonts
sudo ./install.sh
```
最后再去终端修改字体及OK啦。
