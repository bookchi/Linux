# mac搭建hexo
hexo在mac上的安装十分简单，不过多废话，直接写命令。

1. 安装node.js
```shell
$ brew install node
```

2. 安装hexo
``` shell
$ npm install -g hexo

# 创建/切换hexo文件夹
$ mkdir hexo
$ cd hexo

# 初始化hexo
$ hexo init

# 运行
$ hexo g 
$ hexo s
```

## 配置主题
我喜欢`catus`这种极简的主题。还是在hexo目录下操作。
```shell
# 下载主题
$ git clone https://github.com/probberechts/hexo-theme-cactus.git themes/cactus

# 修改配置
$ vim _config.yml

# 修改themes为catus
theme: cactus
```
