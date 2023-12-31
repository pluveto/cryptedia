---
title: ZK
aliases:
- 零知识证明
- ZKP
---

## ZK

零知识证明（Zero-Knowledge Proof，简称ZK）是一种密码学概念，用于证明某个主体拥有某个信息，而不需要将实际信息透露给验证者。它允许一个主体在不泄露私密数据的情况下，向另一个主体证明某个陈述是正确的。

### 原理

原理是通过在证明者和验证者之间进行交互，证明者可以向验证者证明某个陈述的正确性，而不需要透露陈述的具体内容。在这个过程中，证明者通过展示对陈述的知识，使验证者相信陈述是正确的，但并不泄露陈述的实际信息。

### 特点

- 隐私保护：零知识证明允许证明者在不泄露私密数据的情况下向验证者证明某个陈述的正确性。
- 高效性：零知识证明可以在较短的时间内完成验证，即使对于复杂的陈述内容，验证长度也相对较短。
- 非交互式：在最初的零知识协议中，证明者和验证者需要多次来回通信。但在非交互式结构中，证明者只需发送一条证明给验证者，从而实现了一次性的交互。

## 目前主要的实现方式

- ZK-SNARKS
- ZK-STARKS
- Bulletproofs
- Plonk

## zk-SNARKs

zero知识证明(zk-SNARKs)是什么?

zk-SNARK是Zero-Knowledge Succinct Non-Interactive Argument of Knowledge的缩写,它指一种证明构造,其中一个人可以证明某些信息的有效性,例如秘密密钥,而不展示该信息内容,也不需要证明者和验证者之间的交互。

Zcash是首个广泛应用zk-SNARK技术的项目,它利用一种新的零知识加密技术。Zcash中的受保护交易可以完全加密在区块链上,但是使用zk-SNARK证明还是可以验证其有效性,符合网络共识规则,从而获得强大的隐私保护能力。

“零知识”证明允许一方(证明者)向另一方(验证者)证明某个语句的正确性,而不会泄露该语句有效性之外的任何信息。例如,给定一个随机数的哈希值,证明者可以确保该数字存在,而不展示其具体值。

在“知识证明”中,证明者可以证明不仅该数字存在,而且他实际拥有这个数值- 同样不展示任何数值信息。

“简洁”的零知识证明可以在几毫秒内验证,证明长度只有几百字节,即使针对非常大的程序陈述。之前的零知识协议需要多轮交互,而“非交互”构造仅需要一个从证明者到验证者的消息。Halo前,产生非交互且短小能上链的零知识证明最高效方法是初始化阶段生成一个公共参考字符串。如果有人获取生成这个公共参数的秘密随机性,就能伪造出看起来有效的错误证明。

---

1. [zkSNARKs与zcash | Zhuang's Diary](https://willzhuang.github.io/2018/03/21/zkSNARKs%E4%B8%8Ezcash/)
2. [详解零知识证明：未来 10 年 Web3 和区块链最重要的解决方案之一 | CoinVoice](https://www.coinvoice.cn/articles/29217)
3. [[译]对于 zk-SNARKs 运行的简介 - DavidCai](https://davidc.ai/2022/02/27/%E8%AF%91-%E5%AF%B9%E4%BA%8E-zk-SNARKs-%E8%BF%90%E8%A1%8C%E7%9A%84%E7%AE%80%E4%BB%8B/)
