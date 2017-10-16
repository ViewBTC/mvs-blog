---
title: Windows下元界钱包区块文件移到其他盘符
date: 2017-09-29 13:44:21
tags: prameters
categories: blockchain metaverse
---

1. 在下述目录创建配置文件mvs.conf：
```
%HOMEPATH%\AppData\Roaming\Metaverse
```

2. mvs.conf 文件配置内容如下:
```
[database]
directory = D:\MVS\ChainData\Metaverse
```
![p1](http://dlmvs1.oss-cn-hangzhou.aliyuncs.com/conf/20170929181838.jpg)
**上述的路径可以填写你自己的路径;**
或者你可以下载该配置文件:
<http://newmetaverse.org/conf/mvs.conf>

如果是新用户，建议安装 blockdata-inside 版本后，
将 %HOMEPATH%\AppData\Roaming\Metaverse 目录整个拷贝到D盘的目标目录;
(文件夹名称必须是 Metaverse 。)
