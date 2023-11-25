---
aliases:
- 通道
date: 2023-11-15
tags: []
categories: []
toc: true
mathjax: true
comments: true
description: 
---

区块链的 [[Layer2]] 扩展解决方案：通道

通道是一种扩展解决方案，允许两个参与方之间创建点对点通道，可以在链下（ Layer 2 ）进行无限量的交易，而只需将两笔交易提交到链上（第一层）。通道可以提高交易速度，减少网络拥堵、交易费用和交易延迟。

以下是通道的两种常见类型：

1. 状态通道（State Channels）：状态通道用于在区块链网络上更新状态。
    - 例如，假设两个玩家想在以太坊区块链上玩井字游戏。
    - 首先，玩家们在以太坊主链上创建一个多重签名智能合约，其中包含井字游戏的规则、玩家信息和 1ETH 的奖金。
    - 然后，玩家们进入状态通道并开始游戏。
    - 每个玩家的每一步都会创建一个链下交易，
    - 存储在智能合约中。当有获胜者时，玩家们通过签署最终状态并将其提交到多重签名合约来关闭通道。
    - 合约的最终状态将存储在以太坊主链上，并将 1ETH 的奖金转移到获胜者账户上。

2. 支付通道（Payment Channels）：支付通道类似于状态通道，但仅处理支付。
    - 例如，比特币区块链使用的支付通道是闪电网络，以太坊区块链使用的支付通道是 Raiden。
    - 通道允许两个参与方之间创建点对点支付通道，双方可以在没有第一层参与的情况下无限制地相互转移资金。
    - 最终，当两个参与方决定结束交易时，他们可以关闭通道，将最终状态的交易记录在区块链的第一层上。

通道的优点：

- 提高交易速度。
- 降低交易费用。
- 可以进行微支付，例如购买咖啡等小额商品和服务。

通道的局限性：

- 参与方必须始终在线并使用私钥进行签名，这使得他们容易受到黑客攻击和盗窃的威胁。
- 参与方必须在多重签名钱包中锁定一定数量的资金，以打开支付通道。将硬币保存在手机、服务器或个人电脑的热钱包中会增加在线攻击的风险，而冷钱包则不连接到互联网，更安全但不太方便。

---

1. [Layer 2 Blockchain scaling solutions: Channels, Sidechains, Rollups and Plasma (Part 16) | by Techskill Brew | Blockchain 101 by Techskill Brew | Medium](https://medium.com/techskill-brew/layer-2-blockchain-scaling-solutions-channels-sidechains-rollups-and-plasma-part-16-79819e058ef6)
2. [Easy to understand Ethereum Layer 2 scaling solutions: Channels vs Plasma vs Rollups | by The Overpacker Journal | Coinmonks | Medium](https://medium.com/coinmonks/easy-to-understand-ethereum-layer-2-scaling-solutions-channels-vs-plasma-vs-rollups-1dc1d4e9cb52)
3. [Hosam Mahmoud on LinkedIn: 🎯 100 Days Blockchain Development - DAY 10 📅 Today I deployed my first…](https://ug.linkedin.com/posts/hosam-mahmoud-41725550_100-days-blockchain-development-day-activity-7037896089177395200-P4XB)
