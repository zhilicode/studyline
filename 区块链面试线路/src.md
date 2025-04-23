[ 2025.4.22更新 ]
## Blockchain工程师面试学习线路（七阶段“链上火葬场”流）

### 🎯 目标：系统掌握区块链核心原理、Solidity 编程、智能合约安全、EVM 调试、链上交互与 DApp 架构，具备构建安全可用 Web3 项目的能力，并能从面试中活着出来。

---

## 第一阶段：区块链基础原理

**目标：搞清楚你到底是写代码，还是在维护一种“共识幻觉”**

### 1. 区块链原理
- 区块结构：Hash、Merkle Tree、Timestamp、Nonce
- 链式存储、工作量证明（PoW）、权益证明（PoS）

### 2. 常见公链比较
- 比特币 vs 以太坊 vs Polygon vs Solana
- Layer 1 / Layer 2、EVM vs 非 EVM

### 3. 面试高频
- 什么是 Merkle 树？你知道它干嘛的吗？
- 区块链如何防止数据篡改？

---

## 第二阶段：Solidity 编程与智能合约基础

**目标：写合约不是 copy paste，要知道自己调的是谁的钱包**

### 1. Solidity 基础
- 数据类型、mapping、array、struct、modifier
- 合约生命周期、构造函数、继承、抽象合约、interface

### 2. 函数执行特性
- view / pure / payable / fallback / receive
- msg.sender / msg.value / address(this)

### 3. 部署与调用
- Remix IDE、Truffle/Hardhat、MetaMask 调用流程

### 4. 面试必问
- payable 是什么意思？哪个函数不能加它？
- 合约中如何访问另一个合约的方法？

---

## 第三阶段：智能合约安全与审计常识

**目标：链上不允许“修 Bug 重部署”，你上线前就得想好自己挖了几个坑。**

### 1. 常见漏洞
- 重入攻击（Reentrancy）
- 整数溢出（SafeMath）
- delegatecall 被滥用
- 时间依赖性、随机数可预测、权限控制失误

### 2. 安全防范
- ReentrancyGuard、check-effect-interaction 模式
- OpenZeppelin 安全库、Slither 静态分析工具

### 3. 面试生死线
- 重入攻击的完整触发条件？
- 你做过哪些安全加固措施？

---

## 第四阶段：合约编译部署与链上交互

**目标：你不是 Remix 工程师，你得能跑全流程**

### 1. 本地开发框架
- Truffle、Hardhat（合约开发 + 测试 + 部署）
- Ganache 本地链模拟

### 2. 合约交互方式
- Web3.js / Ethers.js：合约 ABI、provider、signer
- 调用 view 方法 vs 发起交易、gas 费用控制

### 3. 面试问题
- 你更喜欢 Truffle 还是 Hardhat？为什么？
- Web3.js 怎么调用一个合约的函数？

---

## 第五阶段：前端 DApp 开发与钱包交互

**目标：链上不只有合约，DApp 才是通往真实用户的钱包钥匙。**

### 1. 钱包接入
- MetaMask / WalletConnect / Phantom
- EIP-1193 接口、账户连接、网络切换监听

### 2. Web3 前端集成
- React + Ethers.js/Web3.js + Tailwind
- 状态管理：连接状态、链 ID、合约调用结果

### 3. 面试高频
- 用户切换了钱包地址，你怎么检测？
- 钱包签名和发起交易有啥区别？

---

## 第六阶段：链上数据管理与 The Graph 索引

**目标：合约数据可查 ≠ 数据好用，你要建索引，要查得快！**

### 1. 事件与日志
- emit 事件、自定义事件结构
- 区块链日志存储机制（Logs）

### 2. The Graph 使用
- subgraph 构建、schema.graphql 编写
- handler 函数触发、部署 subgraph

### 3. 面试高频
- The Graph 是怎么监听链上事件的？
- 如何查询某个地址的 NFT 持仓？

---

## 第七阶段：高级架构与链下协作

**目标：你写的不是合约，你写的是一整套链上链下协作系统。**

### 1. 多合约架构
- Proxy 模式（可升级合约）、Factory 合约、合约依赖图

### 2. 链下服务
- Chainlink（预言机）、IPFS（链下存储）
- Gelato（自动执行）、后台监听机器人

### 3. 进阶面试题
- 如何实现一个支持升级的 ERC20 Token？
- 怎么用 Chainlink 做一个预言机汇率服务？

---

## 附录：Blockchain 面试高频题 Top 10

1. 什么是重入攻击？怎么防？
2. payable 和 call 的使用场景区别？
3. 你写过可升级合约吗？用的是哪种 Proxy 模式？
4. EVM 是什么？它怎么执行合约？
5. Gas 是怎么算的？如何估算交易费用？
6. Chainlink 的基本原理？用过哪些模块？
7. 你是怎么用 The Graph 做数据索引的？
8. ERC20 和 ERC721 有哪些关键接口？
9. 你部署合约时用过哪些测试工具？
10. 如果合约出了严重 bug，你怎么办？怎么补救？

---

## 推荐资源 & 工具

- 📚 文档党：
  - Solidity 官方文档（https://docs.soliditylang.org）
  - Ethers.js / Web3.js 官方文档
  - The Graph 文档
- 🛠️ 工具流派：
  - Remix（快速试验）
  - Hardhat（本地开发神器）
  - Ethers.js + MetaMask（最主流前端组合）
  - Slither + MythX（智能合约安全分析）
- 🚀 学习项目练手：
  - ERC20 币种发行系统
  - NFT 市场前后端全栈项目
  - 可升级投票合约 + subgraph 查询 + DApp 前端

