[ 2025.4.22更新 ]

## iOS 工程师面试学习线路（七阶段高性能修炼法）

### 🎯 目标：系统掌握 iOS App 开发核心技能，涵盖 UIKit & SwiftUI、内存管理、异步编程、网络请求、架构设计与性能调优，具备中高级岗位的技术深度与面试答题力。

---

## 第一阶段：基础语法与开发环境认知

**目标：会用 Swift 写代码，不是照抄 Stack Overflow 的 Hello World**

### 1. Swift 基础语法
- 可选类型（Optionals）、类型推断、值类型 vs 引用类型
- 协议（Protocols）与扩展（Extensions）
- 枚举 + 关联值，闭包（Closures）

### 2. Xcode 环境
- 工程结构、Target 配置
- 真机调试 / 模拟器运行 / Profile 工具使用

### 3. 面试必问
- 什么是 Optional Chaining？
- Swift 中 struct 和 class 有什么关键区别？

---

## 第二阶段：UIKit 与 UI 框架实战

**目标：能写出复杂 UI 交互，不被 storyboard 玩死**

### 1. UIKit 核心组件
- UIViewController 生命周期
- TableView / CollectionView 数据源 + 复用机制
- AutoLayout、StackView、约束优先级

### 2. UI 进阶
- 自定义 Cell、Header/Footer View
- 手势识别、事件传递机制（响应链）

### 3. 面试高频
- Autolayout 的冲突怎么解决？
- 响应链是怎么走的？点到哪个 view 结束？

---

## 第三阶段：SwiftUI 入门与组合开发

**目标：掌握现代 UI 框架 SwiftUI，知道 declarative 是什么玩意儿**

### 1. SwiftUI 基础
- State / Binding / Environment
- ViewBuilder、NavigationStack、List、ScrollView
- 动画、交互响应、条件渲染

### 2. UIKit 混合
- UIViewRepresentable、UIViewControllerRepresentable
- 旧项目渐进式引入 SwiftUI 的方法

### 3. 面试重点
- SwiftUI 是如何更新 UI 的？
- @State 和 @ObservedObject 有什么区别？

---

## 第四阶段：异步编程与数据持久化

**目标：理解线程管理与存储方案，避免写出崩溃的异步逻辑**

### 1. 异步基础
- GCD：DispatchQueue、async/after/group
- OperationQueue：依赖、优先级控制
- Swift Concurrency（async/await, Task, Actor）

### 2. 数据持久化
- UserDefaults、FileManager、Keychain
- CoreData、Realm 基本增删改查

### 3. 面试高频
- GCD 和 OperationQueue 区别？
- Swift 的 Actor 是为了解决什么问题？

---

## 第五阶段：网络编程与请求处理

**目标：掌握基础网络通信与响应式请求流程**

### 1. 网络工具链
- URLSession：GET/POST、超时控制、缓存策略
- Codable 解码、自定义 JSON 结构
- 第三方库 Alamofire（优雅但不是必选）

### 2. 响应式编程
- Combine 框架：Publisher、Subscriber、assign
- 和 SwiftUI 的联动机制

### 3. 面试炸点
- 如何封装网络层？怎么做请求重试？
- Combine 和 RxSwift 有哪些区别？

---

## 第六阶段：内存管理与性能优化

**目标：真正理解 ARC，而不是遇到循环引用才去百度**

### 1. ARC 工作机制
- 引用计数、strong/weak/unowned 区别
- 闭包捕获列表、循环引用避免策略

### 2. 性能调优
- Instruments 使用：Leaks、Time Profiler、Allocations
- View 层级分析、内存泄漏排查
- 离屏渲染、卡顿定位（掉帧分析）

### 3. 面试硬核
- strong 和 weak 的循环引用场景？
- 什么是离屏渲染？为什么影响性能？

---

## 第七阶段：架构设计与系统能力

**目标：让你不只是 App 搬砖工，而是能架构能拆模块的灵魂工程师**

### 1. 架构模式
- MVC、MVVM、MVP、VIPER、Clean Swift
- 响应式架构设计（Combine 驱动视图）

### 2. 模块化与组件化
- 多 Target 管理、CocoaPods / SPM / Carthage 使用
- 通用组件提取（网络层、UI 库、基础工具库）

### 3. 系统能力拓展
- 通知机制（UNUserNotificationCenter）
- 蓝牙（CoreBluetooth）、定位权限（CoreLocation）
- 应用启动优化、冷/热启动时长分析

### 4. 面试必问
- 你用的架构是什么？怎么做模块解耦？
- 如何进行 App 启动优化？实战讲讲。

---

## 附录：面试高频问题 TOP 10

1. Swift 中 class 和 struct 有什么区别？什么时候用哪个？
2. ARC 如何避免内存泄漏？有哪些你遇到的陷阱？
3. iOS 如何实现图片缓存策略？
4. SwiftUI 和 UIKit 的核心思想差异是什么？
5. GCD 的队列类型有哪些？用例是什么？
6. 如何封装一个线程安全的网络层？
7. App 启动慢，你从哪几方面分析？
8. Instruments 中如何查找内存泄露？
9. CoreData 和 Realm 有什么区别？你用过哪个？
10. 你在项目中做过哪些性能优化？

---

## 推荐资源 & 学习工具

- 📘 《Advanced Swift》by objc.io
- 📕 《iOS 面试之道》经典面试题合集
- 官方文档：[https://developer.apple.com](https://developer.apple.com)
- 🚀 教程平台：
  - Hacking With Swift
  - Swift By Sundell
  - Raywenderlich（神仙级别）

- 🧪 实战项目：
  - Todo App（SwiftUI + Combine）
  - 多页面商城 Demo（MVVM + 网络层封装）
  - 组件化博客系统（UIKit + 多模块拆分）
