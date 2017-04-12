---
title: The Installation And Usage Of Metaverse
date: 2017-04-08 13:44:21
tags: Metaverse
categories: Guide
---

[简体中文版本 Simplified Chinese Documentation](http://blog.mvs.live/mvs-user-guide-zh/)


Get Started
---------------
### trial on metaverse test-net
There are two on-line test-net web page for Metaverse as below:
Click into node1: <http://test1.metaverse.live:8820>
Click into node4：<http://test4.metaverse.live:8820>

### Installations
#### Windows platform
1. Get latest release from mvs.live
download from <http://mvs.live>
![download-en](http://newmetaverse.org/guide/download-en.png)

2. Extract installation ball
![win-extract](http://newmetaverse.org/guide/win-extract.png)

3. Run metaverse
open 'mvsd', waiting for synchronizing blocks, the height you can exeplorer on <http://explorer.mvs.live>
(Allow network permission when startup at first time)
![win-run1](http://newmetaverse.org/guide/win-run1.png)
![win-run2](http://newmetaverse.org/guide/win-run2.png)

4. Usage
open 'start-metaverse.html'
![win-start](http://newmetaverse.org/guide/win-start.png)
Or you can type in 127.0.0.1:8820 with your brower
![login-en](http://newmetaverse.org/guide/login-en.png)


#### MacOSX 
1. Get latest release from mvs.live
download from <http://mvs.live>
![download-en](http://newmetaverse.org/guide/download-en.png)

2. Extract tar-ball and install WEB-UI files
Extract
![OSX-extract](http://newmetaverse.org/guide/OSX-extract.png)
open 'mvs-install', waiting for installation done , then close this windows
![OSX-install](http://newmetaverse.org/guide/OSX-install.png)

3. Run
open 'mvsd', waiting for synchronizing blocks, the height you can exeplorer on <http://explorer.mvs.live>
![OSX-run](http://newmetaverse.org/guide/OSX-run.png)

4. Usage
open 'start-metaverse.html'
Or you can type in 127.0.0.1:8820 with your brower
![login-en](http://newmetaverse.org/guide/login-en.png)

#### Linux 
1. Get latest release from mvs.live
download from <http://mvs.live>
![download-en](http://newmetaverse.org/guide/download-en.png)

2. Extract tar-ball and install WEB-UI files
```bash
# extract
tar -xzvf mvs067-linux-x86_64.tar.gz
# open 'mvs-install', waiting for installation done (terminal only, then skip)
./mvs-install
```

3. Run
```bash
open 'mvsd', waiting for synchronizing blocks, the height you can exeplorer on <http://explorer.mvs.live>
# -d run as daemon, otherwise running on your terminal.
./mvsd -d

# look up the help message from mvsd
./mvsd help

# look up the help message from mvs-cli
./mvs-cli help
```

4. Usage
a. Using on terminal normally.
b. Using on browser same as other platfroms.
open 'start-metaverse.html'
Or you can type in 127.0.0.1:8820 on your brower
![login-en](http://newmetaverse.org/guide/login-en.png)


Account and Login
----------------------
### Account Explanation
账户基于HD设计, 您所使用的帐号和密码属于该钱包本地的，非链上的数据，所以不可随主私钥助记符(主私钥助记符是为了方便用户记忆的24个单词或汉字,与主私钥是映射关系)导入。
如果切换新钱包，原账户名和密码不可使用，需要重新设置，即使忘记也没有关系，只需要备份好主私钥助记符即可。
#### a. Add your own new account
Click 'register'
![add-new-en](http://newmetaverse.org/guide/usage/add-new-en.png)
Backup your mnemonic words
![private-keys-en](http://newmetaverse.org/guide/usage/private-keys-en.png)

**Please save this key at a safe place. A good way can be to write it down on a piece of paper. It is very important to back up this key and it is not possible to retrieve this key later**
#### b. import account from other mnemonic words
![importaccount-en](http://newmetaverse.org/guide/usage/importaccount-en.png)

### Login
Type in your own account name and password(those created in last step), click 'Login'
The home-page as blow:
![main-page-en](http://newmetaverse.org/guide/usage/main-page-en.png)
Here is the ETP transfer page:
![transfer-en](http://newmetaverse.org/guide/usage/transfer-en.png)


How to Register/Transfer/IssueAsset on metaverse? (Video)
---------------------
[Open as new tab](http://newmetaverse.org/video/issue_asset_mvs_1280x720.MP4)
<video src="http://newmetaverse.org/video/issue_asset_mvs_1280x720.MP4" width="640" height="480" controls="controls">
Your browser does not support the video tag.
</video>
