[ 2025.4.22更新 ]
## Flutter 工程师面试学习线路（七阶段跨平台暴走流）

### 🎯 目标：掌握 Flutter 跨平台开发的核心技能，包括 Dart 语言能力、Widget 树构建、状态管理、原生交互、性能优化与项目架构，胜任中高级岗位的面试挑战。

---

## 第一阶段：Dart 语言基础

**目标：先学 Dart，否则你根本不知道你在写什么。**

### 1. 基础语法
- 类型系统、可选类型、final/const、闭包、异步
- 类、继承、mixin、扩展方法

### 2. 异步机制
- async / await、Future、Stream、await for
- isolate 概念（真正多线程）

### 3. 面试高频
- Future 和 Stream 的区别？
- 什么是 mixin？和继承有什么差异？

---

## 第二阶段：Flutter UI 构建能力

**目标：把 Widget 树写清楚，不然你的页面就会变成咆哮树**

### 1. 核心 Widget
- Scaffold、AppBar、ListView、Column、Row、Container
- Stack、Align、Positioned、Expanded、Flex

### 2. 布局基础
- 嵌套优化、嵌套陷阱、MediaQuery 适配、SafeArea

### 3. 动态 UI 构建
- 条件渲染、Builder 模式、懒加载、Sliver 系列

### 4. 面试常问
- setState 有哪些缺点？何时不能用？
- build() 什么时候会触发？怎么避免重复重建？

---

## 第三阶段：状态管理与响应式设计

**目标：不懂状态管理，就别说你写 Flutter。真的。**

### 1. 状态管理方案
- setState（入门）、InheritedWidget（原生）
- Provider（主流推荐）、Riverpod（现代香饽饽）
- Bloc、GetX、MobX（进阶）

### 2. 数据流设计
- 单向数据流（Unidirectional Data Flow）
- 全局状态共享 vs 局部状态隔离

### 3. 面试重灾区
- Provider 和 Bloc 的核心区别？
- 怎么设计一个响应式搜索框？

---

## 第四阶段：路由与导航系统

**目标：你得让页面能跳转，还不能乱跳**

### 1. 路由系统
- Navigator 1.0 vs Navigator 2.0
- 命名路由、动态参数、路由守卫

### 2. 页面返回机制
- popUntil、pushReplacement、willPopScope

### 3. 面试常问
- Flutter 的路由栈是怎么维护的？
- 如何实现登录拦截？跳转后还能回来吗？

---

## 第五阶段：平台集成与原生通信

**目标：真正的跨端开发，从“敢调原生”开始。**

### 1. 与原生通信
- MethodChannel：Flutter ↔ 原生
- EventChannel / BasicMessageChannel

### 2. 插件机制
- 使用官方/第三方插件（camera, device_info, shared_preferences）
- 自定义插件开发（iOS/Android 双端）

### 3. 面试高频
- 说一下 MethodChannel 的通信流程？
- 如何封装一个 Flutter 插件并发布？

---

## 第六阶段：性能优化与调试

**目标：你的 app 不能卡，不能炸，不能突然掉帧。你就是性能守卫者。**

### 1. 性能优化
- 构建优化（避免 setState 触发重建）
- ListView.builder、const widget、RepaintBoundary
- 图片优化（缓存、压缩、lazy load）

### 2. 调试工具
- Flutter DevTools：UI 检查、性能分析、内存监控
- `flutter analyze` / `flutter doctor` / 热重载原理

### 3. 面试炸弹题
- 为什么你用 const 都没提升性能？
- 如何定位 UI 卡顿？ListView 卡住怎么办？

---

## 第七阶段：项目架构与工程化能力

**目标：你能驾驭一个中大型 Flutter 项目，而不是单页应用写到死**

### 1. 项目结构
- lib 分层结构：pages, widgets, models, providers, services
- 公共组件封装（按钮、对话框、主题样式）

### 2. 国际化与适配
- 多语言支持（i18n）、平台差异处理（Platform.isIOS）
- 响应式布局（LayoutBuilder + MediaQuery）

### 3. 工程能力
- 自动化构建、打包签名（Android/iOS）
- 多环境配置（dev/test/prod）
- 发布到 App Store / Google Play

### 4. 面试综合题
- 如果你负责重构一个 Flutter 项目，你从哪开始？
- 如何设计一个插件化的组件库？

---

## 附录：Flutter 面试高频题 TOP 10

1. Flutter 中 Widget 是怎么构建的？是轻量组件吗？
2. StatelessWidget 和 StatefulWidget 区别？如何选择？
3. 解释一下 Flutter 的渲染机制？
4. setState 为什么会导致性能问题？
5. 怎么设计一个带搜索建议的输入框？
6. MethodChannel 中异步通信怎么处理超时？
7. Provider 为什么推荐？你怎么组织多个 provider？
8. 如何调试一个 ListView 卡顿问题？
9. 你做过哪些 Flutter 性能优化？
10. Navigator 2.0 的核心优势是什么？

---

## 推荐资源 & 学习资料

- 📘 《Flutter实战》by Google Flutter China
- 📚 官方文档：https://flutter.dev
- 🧠 GitHub 项目：
  - awesome-flutter
  - flutter-samples
- 🧰 工具链：
  - Flutter DevTools
  - VSCode + Dart DevTools
  - Firebase + Flutter 集成调试