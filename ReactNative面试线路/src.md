[ 2025.4.22更新 ]

## React Native 工程师面试线路（七阶段跨平台折磨流）

### 🎯 目标：系统掌握 React Native 的核心开发能力，包括组件构建、状态管理、性能调优、原生模块集成、打包发布与多平台兼容，胜任中高级 RN 工程岗位。

---

## 第一阶段：JavaScript / ES6 / React 核心能力

**目标：JS 不会写好，RN 只能崩得比你快**

### 1. JS 语言基础
- let/const、箭头函数、解构赋值、闭包、this
- async/await、Promise、事件循环、原型链

### 2. React 基础语法
- 函数组件、Hooks（useState/useEffect/useMemo）
- JSX、props、context、事件绑定

### 3. 面试必问
- React 生命周期的演变？
- useEffect 的依赖数组不写会发生什么？

---

## 第二阶段：React Native 基础组件与布局系统

**目标：你要能写出能跑的组件，还不能炸样式**

### 1. 核心组件
- View、Text、ScrollView、Image、FlatList、Touchable 系列
- StyleSheet、Flexbox 布局、Dimensions、Platform

### 2. 动画系统
- Animated API、LayoutAnimation
- Reanimated（进阶）

### 3. 面试高频
- 如何实现一个无限滚动的列表？
- RN 的 Flexbox 和 CSS 的区别在哪？

---

## 第三阶段：状态管理与数据流方案

**目标：你的组件状态不能一改就全页面闪白**

### 1. 状态管理方案
- useState、useReducer、Context API
- Redux、Redux Toolkit、MobX（大项目常用）
- Zustand / Jotai（现代轻量）

### 2. 数据流思路
- 单向数据流
- 全局状态拆分、模块化管理

### 3. 面试题：
- Redux 和 Context 有啥区别？
- Redux 中如何处理异步请求？用过哪些中间件？

---

## 第四阶段：路由与导航系统

**目标：点个按钮跳转个页面，别崩，别重复，别出 bug。**

### 1. react-navigation
- Stack / Tab / Drawer Navigator
- params 传参、动态标题、路由守卫（Navigation Listener）

### 2. Deep Link 支持
- 自定义 URI scheme、universal link、App 通知跳转处理

### 3. 面试常问
- 页面跳转传值与回传怎么处理？
- 说说你实现 deep link 的全过程？

---

## 第五阶段：原生模块与平台集成

**目标：你说你跨平台，平台你得能搞得定**

### 1. 原生通信桥接
- NativeModule：JS ↔ Android / iOS
- react-native-camera、react-native-geolocation 等原生能力接入

### 2. 自动/手动 Linking
- `react-native link` vs pod install vs gradle 配置

### 3. 原生能力常见问题
- 权限问题、图片选取、文件读写、Push 通知接入

### 4. 面试炸弹
- 你写过自定义 NativeModule 吗？JS 怎么调用？
- React Native 调原生性能瓶颈在哪？

---

## 第六阶段：性能优化与调试手段

**目标：跑得慢、闪得快、卡得狠——这些都要能解决**

### 1. 性能问题处理
- 大列表优化（FlatList、虚拟列表、键值绑定）
- 图片缓存、懒加载、shouldComponentUpdate / memo

### 2. 调试工具链
- Flipper 调试、LogBox、Chrome Inspector
- 性能监控工具：why-did-you-render、Perf Monitor

### 3. 面试常问
- 你遇到过哪些卡顿问题？怎么解决的？
- 如何避免组件不必要的重渲染？

---

## 第七阶段：构建发布与多平台适配

**目标：你的 App 得上线，而不是死在模拟器里**

### 1. 构建 & 发布流程
- Android：Gradle + Keystore 签名
- iOS：Xcode 配置 + Pod 管理 + App Store 上传

### 2. 多平台适配
- Platform API、Platform-specific 文件（`.ios.js`, `.android.js`）
- 屏幕适配：响应式布局、比例计算

### 3. OTA 热更新
- CodePush、Expo OTA、版本兼容性控制

### 4. 面试真题
- 你怎么构建生产包？CI/CD 用什么？
- 多端样式适配怎么做？iPhone 14 Pro 和 Android Pad 能同时兼容吗？

---

## 附录：React Native 面试高频题 TOP 10

1. React Native 的渲染流程是怎样的？
2. JS 线程、UI 线程和 Bridge 分别干嘛的？
3. 你写过原生模块吗？通信流程讲一下？
4. RN 项目怎么做 OTA 更新？风险在哪？
5. FlatList 为什么会卡？你做过哪些优化？
6. Android 构建失败最多的是哪一步？你怎么查？
7. React Navigation 和原生导航的底层差异？
8. React Native 和 Flutter 比你怎么看？
9. JS 崩溃了，但原生没挂，用户白屏怎么办？
10. 你踩过哪些 RN 的构建大坑？

---

## 推荐资源 & 实战工具

- 📘《React Native 实战》
- 官方文档：https://reactnative.dev
- 社区神器：
  - react-native-gallery
  - GitHub 上的 react-native-boilerplate
- 实用库：
  - react-navigation
  - react-native-firebase
  - react-native-permissions
  - CodePush 热更新 SDK
