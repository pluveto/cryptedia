---
title: Layer2
date: 2023-11-15T20:28:23.000+08:00
---

Layer-1 是用于描述底层主区块链架构的术语， [[Layer2]] 是位于底层主区块链 Layer1 之上的叠加网络。

之所以被称为 Layer2，是因为它们没有写入影响 Layer1 的代码中。

以比特币和闪电网络为例。比特币是 Layer1 网络，而闪电网络是 Layer2。

再以以太坊为例，Plasma、Polygon 等是 Layer 2。Layer2 扩展解决方案不需要在 Layer1 中进行更改。它可以使用现有元素（例如智能合约）构建在 Layer1 之上。

第 2 层扩展解决方案通过处理链下交易来帮助提高第 1 层的能力。可以改进的两个主要功能是事务速度和事务吞吐量。例如，以太坊目前可以在其基础/主链第 1 层上每秒处理大约 15 笔交易。以太坊 2.0 已经在一定程度上扩展了以太坊 1.0 区块链。它使用权益证明和分片，增加了第 1 层的交易吞吐量。但第 2 层扩展解决方案可以使以太坊 2.0 每秒处理数十万笔交易。

最重要的是，第 2 层解决方案可以大大降低交易费用（以太坊区块链中的 gas 费用）。

扩展解决方案可分为 4 类：

- [[Channel|Channels]]
- [[Rollup|roll-ups]]
- [[Plasma]]
- [[Sidechain|Sidechains]].
