---
title: 元界历史版本ReleaseNotes以及下载地址
date: 2017-04-01 00:00:00
tags: Metaverse
categories: ReleaseNotes
---

0.6.6 版本更新如下:
------------------
1. 增加gettransaction命令，命令输入为transaction hash，返回该hash所对应的transaction信息以及该transaction所在的块高。
2. 修改listtx命令，修改后该命令会默认返回account的100条交易记录而不是返回account的所有记录
3. 增加utxo限制，若一个地址的utxo中含有资产，则该utxo所包含的etp是不能参与etp->etp的交易，只能用于资产交易
4. 增加etp借用功能。转移资产时，若一个地址上的etp不足支付交易费，则从该account上的其他etp充足的地址上借取etp以完成资产转移交易。
5. 修改WebUI中的一些文字提示，让其更友好。
6. 增加WebUI的错误提示内容；

Linux 下载地址:[http://newmetaverse.org/mvs-download/mvs066-linux-x86_64.tar.gz](http://newmetaverse.org/mvs-download/mvs066-linux-x86_64.tar.gz)
OSX   下载地址:[http://newmetaverse.org/mvs-download/mvs066-OSX-x86_64.tar.gz](http://newmetaverse.org/mvs-download/mvs066-OSX-x86_64.tar.gz)

本次发布为补丁级别，针对程序BUG作修正和功能性增强，不涉及任何账户数据迁移。
最新版本请至官网 [http://mvs.live](http://mvs.live) 下载。


0.6.5 版本更新如下:
------------------
一些已知问题修正。
Linux 下载地址:[http://newmetaverse.org/mvs-download/mvs065-linux-x86_64.tar.gz](http://newmetaverse.org/mvs-download/mvs065-linux-x86_64.tar.gz)
OSX   下载地址:[http://newmetaverse.org/mvs-download/mvs065-OSX-x86_64.tar.gz](http://newmetaverse.org/mvs-download/mvs065-OSX-x86_64.tar.gz)

本次发布为补丁级别，针对程序BUG作修正和功能性增强，不涉及任何账户数据迁移。
最新版本请至官网 [http://mvs.live](http://mvs.live) 下载。


0.6.4 版本更新如下:
------------------
一些已知问题修正。

本次发布为补丁级别，针对程序BUG作修正和功能性增强，需要重新同步块数据。
最新版本请至官网 [http://mvs.live](http://mvs.live) 下载。

