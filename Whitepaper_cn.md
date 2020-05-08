# 目录

- [全民基本收入](#全民基本收入)
- [准备工作和其他项目](#准备工作和其他项目)
- [经济学](#经济学)
- [反抗女巫攻击](#反抗女巫攻击)
- [共识](#共识)
- [电子护照](#电子护照)
- [签名的不可转移性](#签名的不可转移性)
- [地址结构](#地址结构)
- [交易](#交易)
- [区块](#区块)
- [可能存在的问题](#可能存在的问题)
- [其他应用](#其他应用)

# 全民基本收入

在当前的加密货币方案中，奖励是通过工作证明或股权证明机制分配给保障网络的实体，而作为网络的一部分参与者是没有奖励的。
目前的奖励机制总是导致参与者之间的价值分配非常不均衡，因此UBIC提出了一种新的货币体系，所有参与者通过全民基本收入来获得奖励。

# 准备工作和其他项目

截至2020年，已经存在数千种加密货币，UBI不是第一个实现UBI发行的项目。
非UBI和UBI加密货币的主要区别在于需要解决sybil（女巫）攻击。

例如，一些像 "Duniter "这样的项目已经开始创建一个需要用户之间互相 "验证"的信任网。虽然想法很简单，但建立一个安全信任的网实际上是相当复杂的，需要先进的图论算法和人工验证。另一种方法是对参与者进行图灵测试---比如用 "Idena "在线解谜---这对于有意愿的参与者来说，需要消耗大量的时间，而抵抗人工智能的侵入则是一个长期的挑战。

UBIC 尝试通过另一种方法，利用护照的数字证书来解决这个问题。

# 经济学
无限供应的货币很可能没有任何什么价值，所以每年的总供应量应该被限制在一个固定的数量。
有不同的货币在一个独特的区块链上运行，每个货币将与一个国家或地区相关联，并由U+ ISO2国家代码来识别。
UCH将是瑞士的货币，UDE将是瑞士的货币，UDE将是德国的货币，UAT将是奥地利的货币，UUK将是英国的货币。
供应量的绝大多数将平均分配给成功关联到护照的地址。
这意味着，如果UCH瑞士UBIC货币的区块供应量为每区块100个单位，并且有50个注册护照，每个区块将获得2个单位的货币。
一段时间后，有500本注册护照，奖励仍然是每块100个单位或多一点，现在每个护照持有人将获得每块0.2个单位的货币。

下面的图表是各种UBIC货币的分配情况。

| 货币代码 | 国家  | UBI年供应量 | 补充信息
| :---- | :--------- | :---------------- | :------------- |
| UCH	 | 瑞士	             | 10,196,640	 |  | 
| UDE	 | 德国	                 | 100,599,840	 |  | 
| UAT	 | 奥地利	                 | 10,617,120	 | 2014年10月后的护照 | 
| UUK	 | 英国	         | 79,838,640	 |  | 
| UIE	 | 爱尔兰	                 | 5,781,600 | 	2016年5月后的护照 | 
| UUS	 | 美国	                     | 393,096,240	 |  | 
| UAU	 | 澳大利亚	             | 29,223,360	 |  | 
| UCN	 | 中国	                 | 1,677,767,760	 | 
| USE	 | 瑞典	                 | 12,036,240	 |  | 
| UFR	 | 法国	                 | 81,730,800	 |  | 
| UCA	 | 加拿大	                 | 44,150,400	 |  | 
| UJP	 | 日本	                 | 154,526,400	 | 2016年5月后的护照 | 
| UTH	 | 泰国	                 | 81,520,560 |  | 
| UNZ	 | 新西兰               | 	5,571,360 |  | 
| UAE	 | 阿拉伯 	 | 11,300,400 |  | 
| UFI	 | 芬兰	                 | 6,675,120 |  | 
| ULU	 | 卢森堡	             | 525,600	     | | 
| USG	 | 新加坡	             | 6,832,800	 | | 
| UHU	 | 匈牙利	                 | 11,931,120	 | | 
| UCZ	 | 捷克	         | 12,877,200	 |  | 
| UMY	 | 马拉西亚	                 | 38,684,160	 |  | 
| UUA	 | 乌克兰	                 | 54,767,520	 |  | 
| USP	 | 西拔牙 	                 | 108,000,000	 | 2016年7月后的护照 |
| UHK	 | 香港	                 | 17,100,000	 | 2019年7月后的护照 | 
| UIS	 | 冰岛 	                 | 420,480	 | 2013年2月后的护照 |
| UEE	 | 爱沙尼亚	                 | 1,681,920	 | 暂无人注册 | 
| UMC	 | 摩纳哥	                 | 52,560	 | 暂无人注册 | 
| ULI	 | 列支敦	         | 52,560	 | 暂无人注册 | 

# 反抗女巫攻击
UBICs抵抗网络攻击的能力是基于现代电子护照的安全特性。您可以使用nfc扫描电子护照来加入。得益于不可转移的签名，您的身份不会以这种方式泄漏，只会在区块链上存储一个唯一的护照哈希值，下面会有更详细的解释。

截至目前，UBIC可以在28个国家使用，这些国家或地区目前都满足了UBIC运行所需要的安全要求。当其他国家或者地区支持有关电子护照的安全特性时，就会有更多的参与者加入。

# 电子护照
过去十年来，许多国家都发行了电子护照，有时也被称为生物识别护照。
这些护照通过NFC与加密技术提供了更高的安全性，使其几乎不可能被伪造。
电子护照的标准是由国际民航组织(ICAO)所规范的，因此所有电子护照都必须实现这些规范所要求的特性。
关于使用的加密算法有一些要求，其中一些还没有足够的公钥指数供UBIC使用（比如香港在2019年6月之前用3作为RSA公钥指数，而UBIC需要足够大的RSA公钥指数，65537以上），这就是为什么UBIC不能支持所有护照都的原因。

### NFC芯片
电子护照的关键部分是嵌入其中的NFC芯片，这种芯片存储了32kb到64kb的信息，分以下几组数据中：
 - 数据组1包含机器可读区，也被称为MRZ，它包括姓名、姓氏、出生日期和有效期等
 - 数据组2包含面部图像
 - 数据组3包含了指纹，它只能使用专用的设备访问，目前只有政府部门可以访问。
最后，文档安全对象是一个PKCS7文件，它包含所有不同数据组的哈希值，使用政府颁发的文档签名证书进行签名。
对于UBIC，只读取文档安全性对象，以生成不可篡改的签名哈希值。

### 权限控制
利用NFC技术，可以读出10厘米外的无源标签。理论上来说，可以通过某人的口袋来读出护照。
但是这并不容易，因为有一个叫做 "基本访问控制 "的安全功能。如果启用了这个功能，护照号码、出生日期和到期日就像密码一样，必须提供后NFC芯片才能读出护照内容。

### 文件签名证书
如 DOC9303 所述，文件签名证书至少每三个月重新发放一次，并有一个有限的签名期，之后会销毁私钥。
这样可以确保如果一个DSC被误用，只需要重新签发一组有限的护照。所有的DSC必须由国家签字证书管理局（又称CSCA）签署。
 
### 国家签名证书
国家签名证书由CSCA机构颁发，该实体在政府公钥基础设施中拥有最高级别的特权。

### PKD
公钥目录是一个提供国家签名和文件签名证书的服务。
下载链接是：https://pkddownloadsg.icao.int/。
PKD并不是唯一有可能获得这些证书的来源，有些国家的政府会在网上公布他们的国家签名证书和他们信任的其他国家的证书，DSC也可以在护照上找到。
 
# 签名的不可转移性
签名的不可转移性是UBIC运作的关键要素，它提供了一种方法，可以体面和安全地核实UBIC地址与未知但真实的护照之间的联系。
它包括在不透露数字签名的情况下证明数字签名的知识。
 
### ECDSA 算法
#### 生成证明
当 ![m](https://github.com/UBIC-repo/images/raw/master/formulas/m.png) 是护照的哈希值, ![R](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/R.png) 从签名中提取的椭圆曲线点 ![(r,s)](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/rs.png)
在区块链上，将显示出:

 - ![](https://github.com/UBIC-repo/images/raw/master/formulas/m.png)

 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/R.png)

 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/Qpa.png) 譬如 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/QapsR.png)

 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/Rp.png) 譬如 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/rpkpr.png) 其中 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/kp.png) 是一个随机数.

 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/sp.png) 这样 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/spk1mprps.png) 在哪里 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/mp.png) 是将获得UBI奖励的UBIC地址。

#### 验证

 - 步骤1.确认 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/verif1.png)

 - 步骤2.确认 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/verif2.png)

### RSA算法
#### 生成证明
当 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/X.png) 是护照信息的哈希值, ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/e.png) RSA公钥指数通常是 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/2161.png) 和 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/A.png) 那么根据Guillou-Quisquater协议来证明知识A的解决方案是:

 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/e.png) RSA公钥指数通常是 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/2161.png) 
 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/X.png) 护照信息的哈希值
 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/t1..5eAd1..5r.png) 其中d是从UBIC公钥派生的16位加盐哈希值，r是加密安全的随机数
 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/T.png) 譬如 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/Tre.png)

因为1 < d < e，而e通常等于 ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/2161.png) 所以上面的操作必须使用不同的d值进行数次，事实上，在当前的UBIC实现过程中，至少要进行5次。

#### 验证

 - ![](https://raw.githubusercontent.com/UBIC-repo/images/master/formulas/t1..5vXd1..5T.png)

在证明生成过程中，每生成一个值d，都要重复上述操作。

# 地址结构
地址由base58来构成的二进制结构，结构如下：
```
<program identifier> <payload length> <payload> <checksum>
      1 byte             1-4 bytes     x bytes   3 bytes
```

程序标识符使UBIC可以轻松地发展和添加新功能，例如用于智能合约的新脚本语言。

比如:
```
<program identifier> <payload length>                   <payload>                      <checksum>
       0x02                0x14         0x23be5a8564ebc151004d798ef812aa25ee7ff79        0x23f234
```
```0x02``` 是使用 ```ripemd160((sha256(public key))``` 作为哈希值的程序标识符。

```0x14``` 是20的十六进制表示，也就是ripemd160散列的长度。

```0x23be5a8564ebc151004d798ef812aa25ee7ff79``` 是有效的地址。在这种情况下，是公钥的散列。

```0x23f234``` 是通过从 ```sha256(<program identifier> <payload length> <payload>)``` 的结果中取前3个字节得到的校验值的和。

不需要每个货币都有一个地址，一个地址可以接收、持有和发送所有UBIC货币。

# 事物

### 结构
交易可以有一个或多个输入，零、1个或多个输出。输入值必须是要大于或等于输出值。
总和(输入)-总和(输出)之间的差额是烧掉的交易费用，这是为了减少通货膨胀。
一笔交易可以同时转移几种货币。但是不可能用一种货币兑换成另一种货币。

### 交易事物的结构
交易事物的结构由以下的结构构成:
- network
- txIns
	- amount
	- inAddress
	- nonce
	- script
- txOuts
	- amount
	- script

network：```uint8_t```字段，由它来确定事物在主网或者测试网上广播。
nonce：```uint32_t```字段，他们保证事物广播的唯一性。
amount：由货币ID(```uint8_t```)，货币数量 (```uint64_t```)构成。
script：```std::vector<unsigned char>```，这是一个序列化的对象。

### 链上货币兑换
爱丽丝想用10个UCH兑换鲍勃的10个UDE，他们可以为此发起一笔交易。
假设0x17a6是爱丽丝的地址，x98b1是鲍勃的地址，在交易中，输入为0x17a6(10 UCH)，0x98b1(10 UDE)，输出为0x17a6(10 UDE)，0x98b1(10 UCH)，双方的货币进行交换，就可以达到交易的目的。

# 区块
区块由以下的结构构成:
- BlockHeader
  - version
  - headerHash
  - previousHeaderHash
  - merkleRootHash
  - blockHeight
  - timestamp
  - payout
  - payoutRemainder
  - ubiReceiverCount
  - votes
  - issuerPubKey
  - issuerSignature
- Transactions


# 共识
UBI没有矿工，而是有委托人验证区块。genesis中有8个创世代表，在项目的早期来提供验证服务。随着时间的推移，新的代表会被添加，而gensis中的代表会被替换，从而使uUBIC完成真正的去中心化。
代表的增加和移除是通过投票机制来规范的，只有代表才能投票。
代表可以由个人，公司，非盈利组织或者任何有能力运营节点且愿意长期支持项目的实体组成，由社区指定，然后由其他代表投票表决。
如果代表有不当行为，其他代表可以通过取消投票来取消该代表。


# 可能存在的问题
### 有多个护照的个人
由于私隐原因，我们不会向区块链传送任何个人资料。UBIC项目假定每个人只有一本有效护照，但实际上这只是一般情况。
人们可以在旧护照未过期的时候或者主动挂失护照，来获得新的护照。
因为护照信息是不公开的，所以UBIC假定所有未到期的护照都是有效的。
但是可能最终有些人会有2-3个认证地址，他们不可能再拥有更多。
有一些因素可以降低风险：
 - 在黑市上，一个真实的护照可能售价上千美元，这就是为什么有人经常“遗失”护照，但是不会去办理新护照，因为这会引起政府执法部门的关注。
 - 一个新的护照所需要的成本和时间，可能已经超过获得UBI本身的价值。
 - 政府部门可以吊销护照并公布，这样，这部分的护照就会无法获得UBI。

### 威胁
政府可能对这类加密货币有不同的想法，可能会通过立法或者黑客攻击来破坏它。因为护照的签名证书由他们发行，有可能伪造护照来欺骗区块链，但是在一般情况下，这是不存在的，这会降低政府的权威和信用。
 
### 隐私问题
非政府组织很难将地址和身份信息关联起来，但对于发行护照的政府来说肯定是可以做到的。
 
# 其他应用
### KYC 验证
区块链本身没有存储用户个人信息，但用户可以将日期数据（Data Group 1）或者 数据组2（Data Group 2）中的信息发送给其他的身份，来进行kyc验证

### 投票
UBIC 目前计划有两种投票方案，第一种是根据投票者当前的货币持有量进行加权，许多数字货币都是这样。
第二种方案，UBI的接收方进行投票，每一票的权重为1，投票者的国家是已知的，所以也可以根据国家进行投票。


