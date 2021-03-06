---
layout: article
title:  "Some My Understandings for Bitcoin And  Blockchain"
pageview: true
comment: true
key: books_notes_some_my_understandings_for_bitcoin_and_blockchain_20170227
tags:
- book-notes
---

> StartTime: 2017-02-27,ModifyTime:2017-02-27

<!---more--->

## Introduction for Bitcoin
比特币的本质其实就是一堆复杂算法所生成的特,而每一个特解都能解开方程并且是唯一的。[9]  以人民币来比喻的话，比特币就是人民币的序列号，你知道了某张钞票上的序列号，你就拥有了这张钞票。

### 挖矿与产出新比特币
每一个比特币的节点都会收集所有尚未确认的交易，并将其归集到一个数据块中，矿工节点会附加一个随机调整数，并计算前一个数据块的SHA-256散列运算值。挖矿节点不断重复进行尝试，直到它找到的随机调整数使得产生的散列值低于某个特定的目标。**由于散列运算是不可逆的，查找到匹配要求的随机调整数非常困难，需要一个可以预计总次数的不断试错过程。** 这时，工作量证明机制就发挥作用了。当一个节点找到了匹配要求的解，那么它就可以向全网广播自己的结果。其他节点就可以接收这个新解出来的数据块，并检验其是否匹配规则。如果其他节点通过计算散列值发现确实满足要求（比特币要求的运算目标），那么该数据块有效，其他的节点就会接受该数据块。

### 交易
当你交易时，另一个重要概念就是区块链。区块链本质上是一个被超大量节点存储的超级账本，除非你修改了这里面的51%的节点，否则更改无效。**确认一项交易的过程**，是由解决一系列计算难题的工作量证明机制来实现的。工作量证明机制要求电脑的计算能力为某个有限值的情况下，需要运算一定的时间才能解决，这就使得攻击者无法重写交易历史，除非他能够拥有比其比特币点对点网络系统更强大的计算能力，从而能以更快地速度产生区块链(区块链总是认为最长的区块链是正确的)。工作量证明机制的难度由系统自动调节，所以新区块的生成平均需时10分钟(交易生效时间,实际上，如果缩短那么就是把风险转移给了第三方交易平台)。整个比特币P2P点对点网络的节点都会自动检测交易和区块的有效性，并忽略任何违背规则的交易和区块，比如那些产生错误数量的区块，或多次发送同一份额比特币的交易行为。比特币应该是拥有自己的区块链(未查证)。

比特币的最小单位是 0.00000001 比特币，称为1“聪”。

### Refenrece:
[百度百科对比特币的定义](http://baike.baidu.com/item/%E6%AF%94%E7%89%B9%E5%B8%81/4143690)  
[维基百科对比特币的定义](https://zh.wikipedia.org/wiki/%E6%AF%94%E7%89%B9%E5%B8%81)
>百度百科的解释不是很客观，举例太多有点乱但优点是举了很多负面例子可以提醒人们谨慎。维基百科的资料比较有条理性以及描述原理更标准和准确。

### Questions
Q1:![Why the maximum number of Bitcoin is 21 million]:http://www.8btc.com/21million00
> The rule is that and it will reach this number in 2140. In fact, its number maybe alway under 21 million.(假定其他setting参数不变)

Q2:![比特幣的發行上限會不會有通縮的問題]:http://forum.bitcoin-tw.com/t/topic/23
> Maybe not. Beacause its smallest unit can become to smaller and smaller.
> 比特币的位元币是可以尽可能分割成更小的单位的，比如亿份之一，当然受制于现实和计算机的能力肯定有极限。

Q3:百度百科对比特币描述的 “产生原理”一节说，如果格式化装有钱包数据的硬盘，个人的比特币将会完全丢失。This maybe not all right. 准确的说法应该是丢失了自己所生产的未交易的比特币的序号。

---

## Introduction for Blockchain
### 1.区块链提出 AND 形式
区块链（英语：blockchain 或 block chain）是用分布式数据库识别、传播和记载信息的智能化对等网络, 起源自比特币。区块链是一串使用密码学方法相关联产生的数据块，每一个数据块中包含了若干次比特币网络交易的信息，用于验证其信息的有效性（防伪）和生成下一个区块。该概念于2008年在中本聪的白皮书[1]中提出，在随后一年当比特币网络开始，中本聪在实现了第一个区块，即“创世区块”。

区块链在网络上是公开的，可以在每一个离线比特币钱包数据中查询。比特币钱包的功能依赖于与区块链的确认，一次有效检验称为一次确认。通常一次交易要获得数个确认才能进行。轻量级比特币钱包使用在线确认，即不会下载区块链数据到设备存储中。

### 2.区块链原理
分布式地重复存储一个超级账本，大量节点重复储存避免中心化的导致唯一数据被篡改

### 4.特点
- 分布式 -> 去中心化
- 极难篡改 -> 值得完全信任、唯一性
- 匿名交易
- 开放透明

### 5.区块链应用领域
- 全球金融行业(提高效率、节约成本、减少风险、防洗钱、防假钱)
- 数字化资产唯一认证(土地、艺术品、医药品等固定资产产权确认和登记、防贪污)
- 智能合同自动执行(法律和保险行业)

### 6.个人看法
鉴于事实上每个区块链节点都需要大量存储设备和网络设备等，所以一般个人几乎难以成为节点之一。终究，区块链目标中的去中心化实际上也只能是将现有银行业的职能转变为区块链节点而已。这是不是会给小银行带来更大的压力，给资本家控制金融带来更大的方便？这些都要经过慎重考量。

而且所谓匿名交易，实际上只要节点设置想要做到追踪还是能够追踪的。

### 7.其它
[Slides For Blockchain Speeching ](http://slides.com/daxiang/deck)

### 7.Questions

Q1: 区块链如何存放如此巨大的数据量、全球的资产和物联网设备，这是不是会由各个大公司代为保存而不是个人? 结果就是被全球资本家控制中心？   
[知乎:区块链信息越来越大怎么办？](https://www.zhihu.com/question/39067000)
