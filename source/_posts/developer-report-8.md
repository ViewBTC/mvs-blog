---
title: Metaverse(元界)项目进展报告-2017年8月
date: August 31, 2017 11:50 AM
tags: upgrade
categories: metaverse developer report

---


# Web钱包开发进展
本月研发工作主要分为钱包系统优化和新特性开发两大部分
## 性能优化


- 崩溃修复（初始化数据库失败导致）
- 优化日志系统减少日志大小方便用户反馈问题
- 针对交易量庞大的账户优化了交易查询相关命令执行效率（提升约40倍
- 账户高级备份（导出到加密文件）
- 优化mongoose服务，提升web钱包相应速度
- Visual Studio 2015 开发环境搭建

![](http://bbs.viewfin.com/data/attachment/forum/201708/31/111554w9hd3zyqpc6peyv6.png)



## 新特性

- 钱包改为操作系统后台运行，启动后可以在任务栏进行钱包打开、退出等操作（目前支持windows和os x）
- 多重签名交易
- 交易地址订阅
- 资产增发
- ETP交易发送命令支持交易说明
- Mac系统安装包制作

![](http://bbs.viewfin.com/data/attachment/forum/201708/31/111748wljblir9riil7lrb.jpg)

注：部分特性功能目前仍处于内测中，后续版本中会陆续放出。

Web钱包0.7.0版本已进入内测阶段，将尽快发布。



# 手机钱包开发进展
## TokenMaster
本月正式推出TokenMaster 安卓版本，官网下载：[https://tokenmaster.info/](https://tokenmaster.info/)

![](http://bbs.viewfin.com/data/attachment/forum/201708/31/112014jvdg340uv46en666.png)

Token Master是一款安全易用、功能强大的手机端数字资产钱包，支持多链多币种，兼容各平台。

【主要功能】
1、	界面简洁、交互流畅，方便数字资产的管理；
2、	支持扫码收付，转账、收款快捷轻便，秒速到账；
3、	跨链跨平台支持多种主流的数字货币，无需在多应用中切换，便捷高效；
4、	自动获取数字货币的交易所实时价格，显示数字资产价值；

## 元界轻钱包
本月，元界轻钱包已完成了整体的功能定义和大部分页面设计工作，元界轻钱包数据将与Web端钱包兼容。

界面预览：
![](http://bbs.viewfin.com/data/attachment/forum/201708/31/112142pqwh8icxsggnhcsi.jpg)

# 其他研发进展

## 元界官网更新
元界官网全新改版上线，地址：[https://mvs.org/](https://mvs.org/)

## 元界数字身份白皮书
元界数字身份白皮书已进入第1.1版修订阶段，将尽快发布。

数字身份将基于元界的生态体系搭建，根据元界区块链提供的底层功能，围绕BaaS及钱包来开展数字身份的应用，以期为各行各业提供可验证、可授权的基础设施服务。

## 区块链即服务（BaaS)
元界CTO陈浩提出区块链即服务（BaaS）概念并对该概念做出了初步的探讨。

区块链即服务（BaaS）—— Blockchain as a Service，是指利用公有区块链产生的数据，提供基于区块链的搜索查询、交易提交，数据分析等一系列操作服务，该操作服务集合可能是中心化的，也可以是去中心化的。目前在区块链领域，区块浏览器、数字货币交易平台以及公链衍生应用：存证型-Factom， 数字身份型-uPort 等都可称之为区块链服务。

具体可见陈浩发布的文章[《从区块链即服务（BaaS）到价值互联网》](http://www.sohu.com/a/166354830_609518)

## MVShub
提交mvshub，旨在提供一个开放开源的基于BaaS的区块链项目的代码库，期待所有开发者的参与。

Github：[https://github.com/mvshub](https://github.com/mvshub)



