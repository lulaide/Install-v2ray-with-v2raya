# Install-v2ray-with-v2raya-locally
> [官方自动安装脚本](https://github.com/v2fly/fhs-install-v2ray) 需要从GitHub下载，网络不通畅往往导致下载不下了
> 此仓库将会指导你如何在debian系统本地安装v2raya，避免网络问题

## 需要的文件
```
install-release.sh
v2ray-linux-64.zip
installer_debian_x64.deb
```
# 获取文件
## 1.获取官方安装脚本
```bash
wget https://raw.githubusercontent.com/v2fly/fhs-install-v2ray/master/install-release.sh
```
## 2.下载 v2ray-linux-64.zip 
* 这里以v5.16.1为例
* [获取最新Release](https://github.com/v2fly/v2ray-core/releases)
```bash
wget https://github.com/v2fly/v2ray-core/releases/download/v5.16.1/v2ray-linux-64.zip
```
## 3.下载 v2raya 的deb安装包
* 以2.2.5.8为例
* [获取最新Release](https://github.com/v2rayA/v2rayA/releases)
```bash
wget https://github.com/v2rayA/v2rayA/releases/download/v2.2.5.8/installer_debian_x64_2.2.5.8.deb
```
# 安装
* 更改脚本权限
```bash
sudo chmod 777 install-release.sh
```
* 使用本地文件安装v2ray
```bash
./install-release.sh -l v2ray-linux-64.zip
```
* 启动v2ray服务
```bash
sudo systemctl enable v2ray; sudo systemctl start v2ray
```
* 安装v2raya
```bash
dpkg -i installer_debian_x64_2.2.5.8.deb 
```
* 启动v2raya服务
```bash
 sudo systemctl start v2raya.service; sudo systemctl enable v2raya.service
```

