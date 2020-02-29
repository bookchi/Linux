## 安装Golang

### 1 下载Go
首先去官网下载Golang：[下载地址](https://golang.org/dl/)
```shell
# 下载linux版本的Go
$ wget https://dl.google.com/go/go1.14.linux-amd64.tar.gz
```
### 2 安装Go
安装很简单，不再赘述，按步骤操作即可。
```shell
# 解压到/usr/local
$ sudo tar -C /usr/local -zxvf go1.14.linux-amd64.tar.gz
 
# vim编辑配置文件；默认是/etc/profile, oh-my-zsh是~/.zshrc
# 没有的话vim可以用命令`sudo apt-get install vim`安装
$ vim /etc/profile

# 在profile最后一行添加
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin

# 保存退出后source
source /etc/profile
```
### 3 验证安装
最后查看安装是或成功。
```shell
# 输入go version命令
$ go version
go version go1.14 linux/amd64

```

