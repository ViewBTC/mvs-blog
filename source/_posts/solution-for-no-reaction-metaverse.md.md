---
title: 元界钱包“已停止工作”或是闪退的解决方法
date: June 20, 2017 6:10 PM
tags: Metaverse
categories: Guide
---

***注意：如果你没有注册过元界钱包账号，可以直接操作；如果你曾经注册过元界钱包账号，在进行下列操作前，一定要先确认自己已保存好账户助记词（私钥）。***

元界钱包打开过程中，如果出现无法响应要求停止程序，或者打开同步程序就会闪退的情况，请按照以下步骤操作：

先关闭mvsd，然后打开“我的电脑”，在地址栏输入C:\Users\username\AppData\Roaming\Metaverse *（将username替换成本电脑的账户名）*，将此目录下的文件全部删除，然后重新打开mvsd同步程序。
![1](http://bbs.viewfin.com/data/attachment/forum/201705/25/143333fpcwfcak7c7gk2lf.png)(所有文件全部删除)

重新同步完成之后，可能会出现登录时提示“*无效的登录凭证*”，请注册一个新账号（账号名不要和原账号相同）并且导入原账号的私钥即可。


如果出现*资产为0*或是资产少于原有账户资产的情况，是因为同步未完成，请耐心等待同步完成即可。



##如何查看自己电脑的username


按快捷键Win+R打开运行框，并输入cmd:
![2](http://bbs.viewfin.com/data/attachment/forum/201706/20/174111e1k33titkz11y085.png)

回车，红框部分就是电脑的username:

![3](http://bbs.viewfin.com/data/attachment/forum/201706/20/174255qav1gsrfrg4pal89.png)

则将C:\Users\ **myka1**\AppData\Roaming\Metaverse 目录下的文件全部删除。


