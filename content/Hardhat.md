---
title: Hardhat
date: 2023-11-17
tags: []
categories: []
toc: true
mathjax: true
comments: true
description: 
---

Hardhat 是一个以太坊开发环境，它可以帮助你编译、部署、测试和调试智能合约和去中心化应用（DApps）。它是一个灵活和可扩展的任务运行器，让你可以管理和自动化开发过程中的重复性任务，并且可以轻松地集成你现有的工具和插件 。

## 使用

要使用 Hardhat，你需要先在你的项目文件夹中安装它，然后运行 `npx hardhat init` 来创建一个 Hardhat 项目。你可以选择创建一个 JavaScript 或 TypeScript 项目，我们推荐使用 TypeScript，因为它可以帮助你避免一些错误。

创建好项目后，你就可以使用 Hardhat 提供的一些内置任务，如 `npx hardhat compile` 来编译你的智能合约，npx hardhat test 来运行你的测试，`npx hardhat run` 来执行你的脚本，等等。你也可以自定义或覆盖这些任务，或者使用 Hardhat 的插件系统来增加更多的功能。

## Hardhat Network

Hardhat 还提供了一个本地的以太坊网络，叫做 Hardhat Network，它可以让你在本地运行和调试你的智能合约和 DApps。Hardhat Network 支持 Solidity 的堆栈跟踪、console.log 和明确的错误信息，让你的调试过程更加方便和高效。

Hardhat 的本地网络运行在你的本地机器上，它不是基于 geth 或者 docker 的，而是基于@ethereumjs/vm 的 EVM 实现，它是一个专为开发设计的以太坊网络节点，可以让你在本地部署、测试和调试你的智能合约和 DApps

## 例子

下面是一个使用 Hardhat 库的简单实例代码，它是一个简单的 ERC20 代币合约，你可以在 Hardhat 的文档中找到更多的例子和教程。

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("MyToken", "MTK") {
        _mint(msg.sender, initialSupply);
    }
}
```

```js
// scripts/deploy.js
async function main() {
  // We get the contract to deploy
  const MyToken = await ethers.getContractFactory("MyToken");
  const myToken = await MyToken.deploy(1000000);

  console.log("MyToken deployed to:", myToken.address);
}

main()
  .then(() => process.exit(0))
  .catch(error => {
    console.error(error);
    process.exit(1);
  });
```

```js
// test/MyToken.test.js
const { expect } = require("chai");

describe("MyToken", function () {
  it("Should return the new greeting once it's changed", async function () {
    const MyToken = await ethers.getContractFactory("MyToken");
    const myToken = await MyToken.deploy(1000000);

    await myToken.deployed();
    expect(await myToken.name()).to.equal("MyToken");
    expect(await myToken.symbol()).to.equal("MTK");
    expect(await myToken.totalSupply()).to.equal(1000000);
  });
});
```

你可以运行 `npx hardhat node` 来启动 Hardhat 的本地网络，然后运行 `npx hardhat run scripts/deploy.js --network localhost` 来部署你的合约，或者运行 `npx hardhat test` 来运行你的测试。你也可以使用 Hardhat 的 VSCode 插件来在你的编辑器中直接调试你的合约。
