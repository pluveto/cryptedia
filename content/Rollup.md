---
title: Rollup
date: 2023-11-15
tags: []
categories: []
toc: true
mathjax: true
comments: true
description: 
---

## 简要介绍

Rollup 是一种区块链层级解决方案，可以将交易的执行从主链 (Layer1) 转移到辅助链 ([[Layer2]]) 来提供扩容。在 Rollup 中，主链上只记录执行过的交易批次的证明，而不记录每笔交易的细节。这可以大大减轻主链的工作量。

## 工作原理

Rollup 工作原理可以概括为以下几步：

1. 在主链上部署一个 Rollup 合约，存储辅助链当前状态哈希值 (state root)。

2. 当在辅助链上执行交易时，状态哈希值 (state root) 会改变。此时需要将更新后的状态哈希值上链。

3. 执行过的交易会被打包压缩成一个批次，并附带更新前后状态哈希值上链。

4. Rollup 合约验证批次内前后状态哈希值是否匹配，如果匹配则将状态哈希值更新。

## 类型

Rollup 主要有两种类型：

### [[ZK|零知识证明]] Rollup(ZK Rollup)

每批交易执行都需要提交 [[ZK|零知识证明]] (SNARK), 证明新的状态哈希值就是正确执行该批交易后的结果。任何人都可以使用零知识证明验证批次内交易的有效性，而不会泄露交易内容。

例子：

- [[zkSync]]

### 乐观 Rollup(Optimistic Rollup)

批交易上链时不实质验证，采取"无罪推定"方式。如果出现欺诈证明，将回滚不合法的交易批次。验证时间一般需要 7 天。

## 优势

- 比 Plasma 提供更高安全性，由于携带更多关键数据上链
- 可在辅助链运行 EVM, 兼容 Ethereum 现有应用
- 提供更廉价的 Gas 费用

## 限制

- 扩容程度受主链交易记录数量限制
- 辅助链仍需支付 Gas 费用执行交易
- 欢快 Rollup 需要更长的提取时间

所以总之，Rollup 使用辅助链来带来扩容，同时利用主链提供安全保证。它解决了 Plasma 长期安全性问题，提高了通用性，但扩容空间和提取速度依然有待改进。