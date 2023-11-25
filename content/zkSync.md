---
title: zkSync
date: 2023-11-16
tags: []
categories: []
toc: true
mathjax: true
comments: true
description: 
---
zkSync 是一种 Layer 2 解决方案中的一种 [[Rollup|rollup]] 技术，具体来说，zkSync 是一种 ZK rollup。每个交易批次都会发送到一个[[Off-chain proof|离线的证明者]]，该证明者会生成一个密码学证明（在 zkSync 的情况下称为 SNARK），证明这些交易是有效的。生成证明的过程很困难，但验证证明的有效性很容易。这种便利性意味着可以将证明发送到 Layer 1 并在智能合约中进行验证，从而实现 Layer 1 和 Layer 2 之间几乎无摩擦的转账。

与其他支持 EVM 兼容性的 ZK rollup（zkEVMs）不同，zkSync 支持账户抽象。账户抽象将每个账户转化为具有自己逻辑的智能合约，这是一个重大突破，使每个人都可以拥有适合自己需求的账户，使加密货币安全、易用，并与其他系统无缝兼容。

zkSync 是由 Matter Labs 开发的，他们获得了以太坊基金会和顶级投资者（如 Union Square Ventures）的资金支持。zkSync 自 2020 年 9 月以来一直处于运行状态。
