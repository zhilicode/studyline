[ 2025.4.2更新 ]
## 第一阶段：Node.js 入门基础

目标：理解 Node.js 的概念、历史以及执行方式。

### 1. Node.js 简介
- 什么是 Node.js？
- Node.js 与浏览器的区别
- Node.js 的核心应用场景（Web 后端、命令行工具、爬虫、构建工具）

### 2. 环境配置
- 安装 Node.js 与 npm
- 使用 node 执行 .js 文件
- 使用 npx 执行命令

### 3. 模块系统
- CommonJS（require / module.exports）
- ESM（ES Modules：import / export）
- 创建自定义模块
- 常见内置模块（如 fs、path、events）

---

## 第二阶段：npm 与项目管理

目标：掌握 Node.js 项目的依赖管理与包开发。

### 1. npm 基础
- 本地安装 vs 全局安装
- 使用 npm install / npm update / npm uninstall
- package.json 配置详解

### 2. 脚本与工具
- npm run 执行自定义脚本
- npx 的使用场景
- npm workspace 多包管理

### 3. 创建自己的包
- 包结构设计
- 发布到 npm（公有与私有）
- 版本控制（语义化版本号）

---

## 第三阶段：异步编程与事件机制

目标：理解 Node.js 的异步机制和事件模型。

### 1. 异步模型
- 回调函数（Callback）
- Promise 与 .then/.catch
- async/await 的使用
- 异步错误处理

### 2. 时间控制
- setTimeout / setInterval
- setImmediate / process.nextTick

### 3. 事件驱动
- Event Loop 概念
- EventEmitter 类的使用

---

## 第四阶段：文件系统与命令行工具开发

目标：使用 Node.js 操作文件、构建命令行工具。

### 1. 文件与路径
- fs 模块（读写、创建、删除文件）
- fs-extra 模块的增强操作
- path 模块与路径拼接
- 获取运行路径：__dirname、__filename、process.cwd()

### 2. 命令行输入输出
- process.stdin / process.stdout / process.stderr
- 使用 chalk 输出彩色文本
- 使用 figlet 显示 ASCII 字符艺术
- 使用 cli-progress 实现进度条

### 3. 用户交互
- prompt、inquirer 实现命令行交互
- commander 管理命令参数
- 环境变量处理（dotenv、process.env）

---

## 第五阶段：Web 开发与 API 构建

目标：使用 Node.js 构建 Web 应用和 API 服务。

### 1. 原生 HTTP 模块
- 创建服务器、解析请求
- 发送响应，处理路由

### 2. Web 框架
- Express.js（轻量流行）
- Fastify（性能优化）
- Nest.js（结构清晰、支持装饰器）

### 3. 中间件与认证
- 使用 passport.js 实现登录认证
- 使用 jsonwebtoken 实现 JWT 认证
- 使用 morgan 记录日志

---

## 第六阶段：数据库与模板引擎

目标：使用 Node.js 操作数据库，构建动态页面。

### 1. 数据库操作
- SQL：
  - Prisma、Sequelize、TypeORM
  - 使用 knex 执行原始 SQL
- NoSQL（MongoDB）：
  - Mongoose（ORM）
  - 原生驱动操作 MongoDB

### 2. 模板引擎
- ejs、pug、marko 等页面模板语言

---

## 第七阶段：测试、日志与部署

目标：掌握项目测试、运行维护与性能调优。

### 1. 测试框架
- 单元测试：Jest、Mocha
- 端到端测试：Cypress

### 2. 日志与监控
- 日志工具：Winston、Morgan
- 进程管理工具：PM2、Forever、nohup
- 性能分析：--inspect、APM 工具
- 内存泄漏与垃圾回收调试

### 3. 多进程与并发
- Worker Threads、Child Process
- Cluster 模块处理多核任务

---

## 附录：常见内置模块快速索引

| 模块名       | 功能说明              |
|--------------|-----------------------|
| fs         | 文件系统操作          |
| os         | 获取系统信息          |
| path       | 路径操作              |
| url        | URL 解析              |
| events     | 事件管理              |
| http       | 创建 Web 服务器       |
| assert     | 断言工具              |
| crypto     | 加密解密操作          |
| net        | TCP 网络通信          |
| perf_hooks | 性能测量工具          |

---

## 推荐资源与学习建议

### 学习建议：
- 多用控制台打印调试日志
- 结合 Express + MongoDB 实战构建项目
- 学习 DevTools 或 APM 工具调试内存

### 推荐网站：
- [Node.js 官方文档](https://nodejs.org/zh-cn/)
- [Awesome Node.js](https://github.com/sindresorhus/awesome-nodejs)

---