---
title: 元界(Metaverse)安装与使用手册
date: 2017-04-08 13:44:21
tags: Metaverse
categories: Guide
---
[Go to English Version](http://blog.mvs.live/mvs-user-guide-en/)

开始
---------------
### 试用
元界提供测试网络的WEB在线测试页面
点击进入测试节点1: <http://test1.metaverse.live:8820>
点击进入测试节点4: <http://test4.metaverse.live:8820>

### 开始安装与使用
#### Windows 版本
1. 获取元界客户端
请至<http://mvs.live>下载最新版安装包
![download-zh](http://newmetaverse.org/guide/download-zh.png)

2. 解压缩
解压压缩包
![win-extract](http://newmetaverse.org/guide/win-extract.png)

3. 运行
打开'mvsd', 等待同步块完成, 最新块高可以从 <http://explorer.mvs.live> 查询
(第一次运行可能出现网络访问请求许可)
![win-run1](http://newmetaverse.org/guide/win-run1.png)
![win-run2](http://newmetaverse.org/guide/win-run2.png)

4. 开始使用
打开start-metaverse.html, 打开页面后请将该地址收藏
![win-start](http://newmetaverse.org/guide/win-start.png)
或直接在浏览器中打开输入  127.0.0.1:8820  并回车
![login-zh](http://newmetaverse.org/guide/login-zh.png)


#### MacOSX 版本
1. 获取元界客户端
请至<http://mvs.live>下载最新版安装包
![download-zh](http://newmetaverse.org/guide/download-zh.png)

2. 解压缩并安装WEB-UI
解压缩
![OSX-extract](http://newmetaverse.org/guide/OSX-extract.png)
打开'mvs-install', 等待提示'' 则表示WEB-UI安装结束，请关闭该窗口
![OSX-install](http://newmetaverse.org/guide/OSX-install.png)

3. 运行
打开'mvsd', 等待同步块完成, 最新块高可以从 <http://explorer.mvs.live> 查询
![OSX-run](http://newmetaverse.org/guide/OSX-run.png)

4. 开始使用
打开start-metaverse.html, 打开页面后请将该地址收藏
或直接在浏览器中输入  127.0.0.1:8820  并回车
![login-zh](http://newmetaverse.org/guide/login-zh.png)

#### Linux 版本
1. 获取元界客户端
请至<http://mvs.live>下载最新版安装包
![download-zh](http://newmetaverse.org/guide/download-zh.png)

2. 解压缩, 安装WEB-UI(可选)
```bash
#解压缩
tar -xzvf mvs067-linux-x86_64.tar.gz
#执行'mvs-isntall'安装WEB-UI，提示安装结束。(此步骤可选)
./mvs-install
```

3. 运行
```bash
# 执行'mvsd', 等待同步块完成, 最新块高可以从 <http://explorer.mvs.live> 查询
# -d 以守护进程形式启动, 没有-d则从会话终端启动
./mvsd -d

# 执行help查看启动参数
./mvsd help

#执行mvs-cli查看控制台命令
./mvs-cli help
```

4. 开始使用
a. 命令行请在终端使用
b. 浏览器端与其他平台操作相同:
请打开start-metaverse.html, 打开页面后请将该地址收藏
或直接在浏览器中输入  127.0.0.1:8820  并回车
![login-zh](http://newmetaverse.org/guide/login-zh.png)


(注:后续版本会制作一键安装包简化安装过程)

账户与登录
----------------------
### 账户
账户基于HD设计, 您所使用的帐号和密码属于该钱包本地的，非链上的数据，所以不可随主私钥助记符(主私钥助记符是为了方便用户记忆的24个单词或汉字,与主私钥是映射关系)导入。
如果切换新钱包，原账户名和密码不可使用，需要重新设置，即使忘记也没有关系，只需要备份好主私钥助记符即可。
#### a. 新建一个账户
点击'新建'后，新建账户
![addnew](http://newmetaverse.org/guide/usage/addnew.png)
备份主私钥助记符
![private-keys](http://newmetaverse.org/guide/usage/private-keys.png)

**在任何情况下，您都不能向任何人透露您的主私钥助记符，这是您在元界上的唯一凭证，丢失后无法找回！请务必保管好您的主私钥助记符。**
#### b. 从已有账户导入
![importaccount](http://newmetaverse.org/guide/usage/importaccount.png)

### 登录
输入您的本地账户名和密码（刚刚创建或导入的），点击登录
登录后的界面：
![main-page](http://newmetaverse.org/guide/usage/main-page.png)
ETP转账页面：
![transfer](http://newmetaverse.org/guide/usage/transfer.png)


熵(ETP)币转移和资产操作演示视频
---------------------
[点击在新tab页打开](http://newmetaverse.org/video/issue_asset_mvs_1280x720.MP4)
<video src="http://newmetaverse.org/video/issue_asset_mvs_1280x720.MP4" width="640" height="480" controls="controls">
Your browser does not support the video tag.
</video>
