## 安装msf

很简单的一条命令，就可以直接安装

```shell
curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && chmod 755 msfinstall && ./msfinstall
```
大概效果如下
```shell
sudo curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && chmod 755 msfinstall && ./msfinstall
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  5495  100  5495    0     0   7889      0 --:--:-- --:--:-- --:--:--  7883
Switching to root user to update the package
Adding metasploit-framework to your repository list..OK
Updating package cache..OK
Checking for and installing update..
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following package was automatically installed and is no longer required:
  libopts25
Use 'sudo apt autoremove' to remove it.
```
## 安装docker

```shell
# ubuntu 官方仓库提供了Docker的稳定版本
sudo apt-get update
sudo apt-get install docker.io
```
或者使用官网的脚本安装
```shell
# 安装curl
sudo apt-get update
sudo apt-get install curl
# 使用官网脚本安装
curl -s https://get.docker.com/ | sudo sh
```
docker的启动停止
```shell
sudo service docker stop
sudo service docker start
sudo service docker restart

```
