---
title: Digital signature
date: 2023-11-18
tags: []
categories: []
toc: true
mathjax: true
comments: true
description: 
---

包括如下接口：

- Gen(): outputs a key pair (pk, sk) 生成公私钥对
- Sign(sk, msg) outputs sig. σ 用私钥对消息签名
- Verify(pk, msg, σ) outputs ‘accept’ or ‘reject’ 用公钥验证签名

## 方案

## 必应

这些算法是一些基于不同数学问题的数字签名方案，它们可以用来保证消息的完整性和发送者的身份。我将简要介绍每种算法的特点和优缺点。

- RSA签名（不用于区块链）：
  - RSA签名是基于大整数的因数分解难题的签名方案，它可以快速地验证签名的有效性，但是签名和公钥的长度都很长（至少256字节），这会增加存储和传输的开销。
  - RSA签名也有一些安全性的问题，比如它不是确定性的，也就是说对同一个消息可以生成多个有效的签名，这可能导致重放攻击或签名伪造。另外，RSA签名也不能抵抗量子计算机的攻击，因为量子计算机可以在多项式时间内分解大整数。

- 离散对数签名：Schnorr和ECDSA
  - 离散对数签名是基于离散对数难题的签名方案，它通常使用椭圆曲线群作为底层的数学结构，这样可以使签名和公钥的长度很短（48或64字节），节省空间和带宽。
  - Schnorr签名是一种简单而高效的离散对数签名方案，它具有唯一性和确定性，也就是说对同一个消息只有一个有效的签名，这可以防止签名的篡改和重放。Schnorr签名还支持多重签名和聚合签名，这可以减少签名的数量和大小，提高效率。
  - ECDSA是一种广泛使用的离散对数签名方案，它是基于DSA的椭圆曲线版本，它的安全性依赖于椭圆曲线离散对数难题。ECDSA的优点是它已经被许多标准和协议所采用，有很好的兼容性和可靠性。ECDSA的缺点是它不是确定性的，也不支持多重签名和聚合签名，而且它的实现比较复杂，容易出现错误或漏洞。

- BLS签名：48字节，可聚合，易于阈值
  - BLS签名是一种基于双线性对的签名方案，它的签名和公钥都是椭圆曲线群的元素，长度为48字节。BLS签名的特点是它可以对任意数量的签名进行聚合，得到一个单一的签名，这可以大大减少签名的空间和验证的时间。
  - BLS签名还支持阈值签名，也就是说只需要一定比例的签名者参与就可以生成一个有效的签名，这可以提高容错性和安全性。BLS签名的缺点是它需要一个安全的哈希函数，将消息映射到椭圆曲线群上，这可能会影响性能和兼容性。

- 后量子签名：长（≥768字节）
  - 后量子签名是一种抵抗量子计算机攻击的签名方案，它基于一些量子计算机难以解决的数学问题，比如编码理论、多项式系统、哈希函数等。后量子签名的优点是它可以保证在量子计算机出现后，签名的安全性不会被破坏。
  - 后量子签名的缺点是它的签名和公钥的长度都很长（至少768字节），这会增加存储和传输的成本。另外，后量子签名的效率和可靠性还没有得到充分的验证和测试，它还没有被广泛地应用和标准化。
