---
title: Hash Functions
date: 2023-11-18
tags: []
categories: []
toc: true
mathjax: true
comments: true
description: 
---
> Cryptographic hash functions: An efficiently computable function H: M ⇾ T where |M| ≫ |T| -- Defi MOOC

一个高效可计算的函数 H: M ⇾ T，其中 M 是输入的消息空间，T 是输出的散列值空间，且 |M| ≫ |T|，即输入的可能性远远大于输出的可能性。这样的函数可以实现散列值的压缩，即将大量的输入映射到有限的输出。

密码散列函数是一种用于加密的数学函数。它可以将任意长度的输入（称为消息）转换为固定长度的输出（称为散列值或摘要）。密码散列函数具有以下特点：

- 它们是“抗碰撞的”。这意味着不应该有两个不同的输入散列到相同的输出散列。
- 它们是“隐藏的”。这意味着从输出散列推测输入值是困难的。
- 它们是“难解的”。这意味着选择一个能够产生预定义输出的输入是困难的。

密码散列函数在信息安全中有很多应用，例如数字签名，消息认证码，以及其他形式的认证。它们也可以用作普通的散列函数，用于在散列表中索引数据，进行指纹识别，检测重复数据或唯一标识文件，以及作为校验和来检测数据的意外损坏。
