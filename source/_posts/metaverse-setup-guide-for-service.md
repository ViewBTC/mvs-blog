---
title: Metaverse（元界）ETP钱包服务端使用指南
date: 2017-05-08 13:44:21
tags: wallet
categories: blockchain metaverse wallet service
---

# 前言
元界钱包基于Libbitcoin实现。
rpc的使用上的概念与比特币十分类似，但是接口不同。

# rpc的调用
rpc开启的默认端口是 8820, 暂不支持https。
您也可以在 mvs.conf 中配置为其他端口。
php 对接ETP钱包的示例代码请参考： <https://github.com/ViewBTC/mvs-exchange-tools>
后续会开放其他语言的示例代码。

mvs-cli 默认也是调用8820端口，执行rpc。
所以在用户浏览器中查看的数据，与mvs-cli调用其实是同一个。

# 查看帮助信息
所有的命令都支持help命令，执行
mvs-cli 也可以是用户浏览器中的控制台
```bash
# 查看所有命令
mvs-cli help
# 查看具体命令参数和描述
mvs-cli help send 
#或
mvs-cli send -h
```

# 遍历区块的命令

```bash
# 查询块高对应的块哈希
./mvs-cli fetch-header -t  $block_height
# 查询块哈希对应的先块结构
./mvs-cli getblock  $block_hash --json=true
```


# HD账户的新建和地址的管理

元界在一开始设计的时候就摒弃了随机keys的想法，一切交易均由主私钥对应的子私钥管理。
由主私钥匙+index生成对应的子私钥。
且您所使用的帐号和密码属于该钱包本地的，非链上的数据，所以不可随主私钥助记符(主私钥助记符是为了方便用户记忆的24个单词或汉字,与主私钥是映射关系)导入。
如果切换新钱包，原账户名和密码不可使用，需要重新设置，即使忘记也没有关系，只需要备份好主私钥助记符即可。

```bash
# 生成新账户
mvs-cli getnewaccount $name $password
# 使用该账户生成地址，这些地址一定属于该账户
mvs-cli getnewaddress $name $password
# 查看我的帐户的地址
mvs-cli listaddresses $name #password
```

账户名和账户口令相当于你的主私钥在这个钱包里的别名，账户名与主私钥一一对应，使用账户名和口令相当于调用对应的主私钥，所以以上命令就是使用某个主私钥生成新地址的意思。


一个主私钥对应的index总数大概40亿，默认都是从0自增的，所以您只需要备份主私钥即可，不应当备份账户名和密码。
如果忘记账户名和密码，重新导入主私钥助记符即可，可以使用importaccount命令，导入时可指定index大小，钱包将为您生成相应个数的地址，具体参见help。
在元界上，所有个人资产的唯一凭证只有主私钥助记符，包括您发行的资产。

元界钱包目前还没有做文件级别的备份，您千万备份好您的主私钥助记符（也就是那24个单词）
备份主私钥助记符会确保您不会有任何资产损失，通过账户名和密码是无法查看主私钥助记符的。

# 发送交易（重点）
```bash
# send 命令
mvs-cli send $name $password $target_address $amount
# sendfrom 命令
mvs-cli send $name $password $from_address $target_address $amount
```

* send 命令详细解释（重要）:
send 命令是一个为普通用户优化后的命令，支持规整交易，打乱找零输出到其他地址，
即找零随机到一个本账户其他地址的命令，**不建议在交易平台后台使用**。
send 命令的在服务端的使用场合：需要规整零钱或者全额发送到其他地址。确定性的发送请使用sendfrom替代！

* sendfrom 命令详细解释：
sendfrom 命令支持找零到发送地址，sendfrom命令是十分类似其他钱包的命令的。

# 资产和交易管理QA
1. 如何从交易记录查看资产？
交易记录中有attachment，里面有type，type的类型是etp就是etp，如果是发行的资产则就是其他符号，目前有一些测试token，使用listassets不加任何参数可以看到

2. 如何看待ETP和其他资产的关系？
ETP相当于是以太里面的ETH，其他的资产相当于都是token.

3. 如果通过接口获得某个account或者地址的private key?
无法获得指定地址的private key，如果是指定地址发交易，我们有sendfrom命令支持指定地址，该地址属于该账户即可。

4. 如何通过转账记录创建raw transaction， 就是类似比特币的createrawtransaction?
针对rawtransaction， 属于自己组件交易，这个是由libbitcoin原生命令支持的，我们保留了这部分功能，但是不推荐使用，
可以参照 <https://github.com/libbitcoin/libbitcoin-explorer/wiki/How-to-Spend-Bitcoin>，将其中bitcoin部分替换成元界的地址和utxo，依然成立。

5. 如何使用private key对raw transaction进行sign?
同上, 推荐使用HD方式的地址.

6. 如何通过HD方式生成地址?
```bash
./mvs-cli getnewaddress $account_name $account_password
```
账户名和账户口令相当于你的主私钥在这个钱包里的别名，账户名与主私钥一一对应，使用账户名和口令相当于调用对应的主私钥，所以以上命令就是使用某个主私钥生成新地址的意思。
