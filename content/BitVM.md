---
title: BitVM
date: 2023-11-16
tags: []
categories: []
toc: true
mathjax: true
comments: true
description: 
---

BitVM 是由ZeroSync的Robin Linus设计的一种新的optimistic rollup + fraud proof + Taproot Leaf + Bitcoin Script计算范式。BitVM 提供了一个计算框架，允许在 Bitcoin 上执行复杂的合约，而不改变其核心原则。它是比特币虚拟机，可以被理解为 Bitcoin 宇宙中的一个安全、封闭的领域，允许执行任何程序或智能合约。

BitVM 的机制采用了简单但强大的结构，包括两个关键实体：Prover 和 Verifier。Prover 发起计算，而 Verifier 验证其合法性。这种双系统确保结果既可靠又一致。BitVM 的智慧在于其链下计算策略。与传统的区块链不同，BitVM 外部加载了大多数要求严格的计算，节省了 Bitcoin 区块链上的空间，提高了速度，并削减了成本。但当争议出现时，BitVM 会使用 "Fraud Proofs" 转向链上验证，确保没有任何虚假的声明被忽视。

BitVM 的主要吸引力是其支持高级和多样化合约的能力。用户现在不仅可以参与货币合约，而且可以利用它们运行复杂的 Decentralised Applications (DApps)，如策略游戏或任何当前的 Web3 DApp。此外，BitVM 的结构使得创建真正的去中心化预测领域成为可能，从而扩大了 Bitcoin 智能合约的范围。

尽管有其优点，但了解 BitVM 的局限性也是必要的。其当前的设计偏向于两方互动，限制了其在多方环境中的使用。随着 Decentralised Finance (DeFi) 变得越来越复杂，这一约束可能会妨碍 BitVM 的相关性。此外，链下计算的要求可能会对没有足够计算资源的用户或那些参与多个 BitVM 合约的用户造成负担。然而，随着 BitVM 的成长，有潜力解决这些障碍，并通过演变和适应成为 Bitcoin 相关交易和合约的关键工具。

---
Learn more:
1. [关于BitVM你需要知道的一切 - 金色财经](https://m.jinse.cn/blockchain/3661767.html)
2. [图说｜四张图详解BitVM是什么？ - BlockBeats](https://m.theblockbeats.info/news/46221)
3. [什么是 BitVM，比特币智能合约的关键一步 | TokenInsight](https://tokeninsight.com/zh/tokenwiki/all/what-is-bitvm-the-next-step-in-advancing-smart-contracts-on-bitcoin)
