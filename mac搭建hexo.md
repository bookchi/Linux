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

## 关联GitHub
主要是生成ssh密钥，把公钥放在GitHub上。
```shell
# 生成公钥匙
$ ssh-keygen -t rsa -C "your_email@example.com"

# 查看公钥
$ cat ~/.ssh/id_rsa.pub

# 然后将公钥添加到GitHub上
```
之后在本地做一些配置(仍在hexo目录下
```shell
$ npm install hexo-deployer-git --save

# 修改config配置文件
$ vim _config.yml 

deploy:
type: git 
repo: git@github.com:[username]/[username].github.io.git // ssh  刚创建的Github仓库
branch: master
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

## 测试
最后看效果
```shell
$ hexo clean
$ hexo d -g
```
然后访问博客地址即可。
