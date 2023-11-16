---
title: Circuit
---

Circuits 是一种约束集合，如果满足这些约束，就可以证明计算是正确执行的。ZK 中的 circuits 有时也被称为算术电路，因为电路中的“门”是有限域上的加法和乘法操作。

在 ZK 中，电路的作用是用来验证零知识证明。具体来说，两个参与方共享电路 C 的描述、输出值 y 和可能的一些输入值 x₁,...,xₗ。然后，证明者向验证者证明他们知道额外的秘密输入 s₁,...,sₙ，使得如果将电路 C 在输入 x₁,...,xₗ,s₁,...,sₙ上进行计算，结果将是 y。也就是说，C(x₁,...,xₗ,s₁,...,sₙ) = y。知识的论证属性保证了证明者必须实际上知道这些输入才能说服验证者。零知识属性保证了验证者除了上述陈述是真实的之外，不会从交互中获得任何信息。特别是，验证者对 s₁,...,sₙ不会获得任何信息。

---

[Consensys/gnark: gnark is a fast zk-SNARK library that offers a high-level API to design circuits. The library is open source and developed under the Apache 2.0 license](https://github.com/Consensys/gnark)
