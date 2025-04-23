[ 2025.4.22更新 ]
## Web3 工程师面试学习线路（七阶段全链打怪升维计划）

### 🎯 目标：系统掌握 Web3 应用开发全栈技能，涵盖区块链原理、Solidity 编程、前端钱包交互、链上数据索引、去中心化存储与合约架构，具备独立开发 DApp 的能力并能通过技术岗面试洗礼。

---

## 第一阶段：区块链与加密学基础

**目标：链上世界不能靠“感觉”，你得真的懂点原理**

### 1. 区块链核心概念
- 区块结构、Merkle 树、链式结构
- 公钥/私钥、非对称加密、签名机制、哈希算法

### 2. 共识机制概览
- PoW、PoS、DPoS、PBFT 各种模式
- L1 vs L2：Rollup、Plasma、ZK-SNARK 简介

### 3. 面试高频
- 区块链是怎么防止篡改的？
- 区块链和数据库有啥区别？

---

## 第二阶段：Solidity 智能合约编程

**目标：不是 Remix 点点就能说会 Solidity，要懂合约是怎么编译、运行、炸掉的。**

### 1. Solidity 核心语法
- 函数类型：view、pure、payable
- 状态变量、构造函数、继承、modifier
- mapping、enum、event、struct、library

### 2. 合约部署与测试
- 使用 Hardhat / Foundry 部署测试
- 网络选择、链 ID、测试币 faucet 使用

### 3. 面试必问
- Solidity 中如何设计一个可升级合约？
- 合约之间如何通信？delegatecall 会踩什么雷？

---

## 第三阶段：Web3 前端与钱包交互

**目标：你不能只会“按钮 → alert”，要能连接钱包、签名、发交易。**

### 1. 前端连接能力
- React + Ethers.js or Web3.js 使用
- connectWallet, getSigner, requestAccounts
- 网络切换、链 ID 监听、账户变更检测

### 2. 钱包生态
- MetaMask、WalletConnect、Safe、RainbowKit

### 3. 面试高频
- 钱包连接流程讲一下？
- 你如何在前端发起一个 ERC20 transfer？

---

## 第四阶段：DApp 状态管理与合约读写

**目标：DApp 不是页面，是“链上组件 + 状态管理 + 用户身份系统”**

### 1. 链上数据读写
- Ethers.js `contract.read()` vs `contract.write()`
- 签名 vs 交易、gas 预估、tx 回执监听

### 2. 合约 ABI 与动态交互
- 动态加载合约 ABI、接口抽象、合约地址多链支持
- 多钱包 / 多链支持架构设计

### 3. 面试热点
- 你怎么处理链上数据的缓存与刷新？
- 怎么避免重复交易发送？

---

## 第五阶段：链上数据索引与 The Graph 使用

**目标：不要傻乎乎遍历区块，**你要优雅地做个 GraphQL 查询小能手**

### 1. 事件监听
- Solidity emit → Ethers.js filter
- The Graph 建立 Subgraph：schema + handler

### 2. 数据查询
- GraphQL 查询语法
- 部署到 hosted service / decentralize node

### 3. 面试必问
- 你写过 subgraph 吗？怎么处理 event handler？
- Graph 的好处 vs 手动调用合约事件？

---

## 第六阶段：去中心化服务集成（IPFS / Chainlink / ENS）

**目标：不是所有东西都能“上链”，你得知道链外怎么配合链上演戏。**

### 1. IPFS 与文件存储
- IPFS 上传、pinning、cid 管理
- Web3.Storage / Pinata 使用

### 2. Chainlink 使用
- 预言机基本用法：价格喂价 / VRF 随机数

### 3. ENS / NFT 域名
- 域名解析、反向注册、合约调用绑定域名

### 4. 面试真题
- 你怎么上传用户头像（不是链上存）？
- Chainlink VRF 原理是啥？可预测吗？

---

## 第七阶段：项目架构、安全审计与合约升级

**目标：一个完整 Web3 项目不是几个合约拼一拼，而是系统设计 + 安全闭环**

### 1. DApp 架构设计
- 前端 + 合约 + subgraph + 后台机器人（监听执行）
- 多合约协作（Factory、Proxy、Registry）

### 2. 安全与升级
- 可升级合约（Proxy Pattern）
- 重入攻击、授权漏洞、权限管理、安全库使用（OpenZeppelin）

### 3. 面试综合题
- 设计一个链上拍卖市场 + 热更新机制
- 怎么实现一个 upgrade-safe 的 NFT 销售平台？

---

## 附录：Web3 工程师面试高频 Top 10

1. EVM 是什么？Solidity 最终是怎么在链上跑起来的？
2. payable 有什么限制？call 和 transfer 有啥区别？
3. Metamask 是怎么发起交易的？你是怎么接的？
4. The Graph 是怎么监听链上数据的？你部署过 subgraph 吗？
5. 什么是 reentrancy？如何避免？
6. 合约的 gas 消耗怎么看？如何做优化？
7. 你如何处理用户钱包换链换账号？
8. 写过可升级合约吗？Proxy 是怎么调 storage 的？
9. NFT 合约有哪些标准？你封装过 mint 吗？
10. 前端调用失败但合约执行成功的可能场景？

---

## 推荐学习资料 & 工具链

- 📚 文档党：
  - [Solidity Docs](https://docs.soliditylang.org)
  - [Ethers.js](https://docs.ethers.org)
  - [The Graph](https://thegraph.com/docs/)
- 🧰 工具人必备：
  - Hardhat + Foundry（本地开发与测试）
  - Metamask + WalletConnect
  - OpenZeppelin（合约安全库）
  - IPFS / Web3.Storage / Pinata
  - Safe（多签工具）、RainbowKit（钱包连接 UI）

- 🎮 实战练手：
  - 基于 ERC20 的空投系统
  - NFT + Subgraph 构建链上头像平台
  - DAO 系统（投票 + 可升级合约）
