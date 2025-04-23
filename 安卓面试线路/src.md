[ 2025.4.22更新 ]

## 安卓工程师面试学习线路（七阶段打怪升级流）

### 🎯 目标：系统掌握 Android 开发核心知识，覆盖基础组件、UI体系、线程机制、Jetpack架构、性能优化、系统原理与面试实战，成为面试官不会轻视的那种候选人。

---

## 第一阶段：四大组件与基础能力

**目标：理解 Android 应用的基本运行单位，能写、能调、能解释生命周期**

### 1. 四大组件
- Activity：生命周期、任务栈、启动模式
- Service：前台服务、绑定服务、JobIntentService
- BroadcastReceiver：静态 vs 动态注册、粘性广播
- ContentProvider：数据共享机制、URI 格式解析

### 2. 基础能力
- Intent 机制、Bundle 传参、权限请求机制
- App 启动流程与冷启动优化

### 3. 面试常问
- Activity 被杀后如何恢复数据？
- 四种启动模式分别适用在哪些场景？

---

## 第二阶段：UI、布局与自定义视图

**目标：掌握视图绘制流程，能熟练实现复杂交互和性能优化**

### 1. 布局系统
- ConstraintLayout、LinearLayout、FrameLayout 差异
- measure → layout → draw 三大流程
- ViewGroup 的事件分发机制（onInterceptTouchEvent）

### 2. 自定义 View
- Canvas 绘图、Path 动画
- 属性动画、ValueAnimator、Interpolator
- ViewStub、merge、include 性能技巧

### 3. 面试爆点
- 自定义 View 如何避免重绘卡顿？
- 事件冲突怎么解决？写出案例！

---

## 第三阶段：线程与异步机制

**目标：掌握 Handler、Looper、HandlerThread 的底层运行机制**

### 1. Handler 机制
- Looper.prepare() 到 Looper.loop() 执行原理
- 主线程 Handler 和子线程 Handler 差异
- MessageQueue 的阻塞唤醒机制

### 2. 异步机制
- AsyncTask（已废）、Thread + Runnable、Executor
- Kotlin 协程（CoroutineScope, Dispatchers）

### 3. 面试高频
- Handler 为什么不会内存泄漏？
- Message 是怎么调度的？如何避免丢失？

---

## 第四阶段：Jetpack 与架构模式

**目标：掌握现代安卓开发生态，能写出可维护的 MVVM 应用**

### 1. Jetpack 核心组件
- Lifecycle、LiveData、ViewModel、Navigation
- Room：本地数据库 ORM
- DataStore：代替 SharedPreferences

### 2. 架构模式
- MVP、MVVM、Clean Architecture
- Repository 模式与单向数据流

### 3. 面试加分项
- 如何实现一个 LiveData 替代方案？
- MVVM 的缺点是什么？什么时候用 Clean 更合适？

---

## 第五阶段：网络、存储与数据交互

**目标：掌握网络通信与数据存储相关能力，提升系统完整度**

### 1. 网络开发
- Retrofit、OkHttp 原理与拦截器链
- 请求缓存、超时重试、异常处理

### 2. 数据存储
- Room 数据库增删改查
- 文件存储、DataStore、SQLite、MMKV

### 3. 面试高频
- Retrofit 的请求流程？
- 怎么优雅地在应用中实现离线缓存？

---

## 第六阶段：性能优化与内存分析

**目标：能分析卡顿、泄露、ANR 等大厂必问问题，证明你不是写了就跑的那种人**

### 1. 启动优化
- 冷启动时间分析
- Application onCreate 延迟初始化技巧

### 2. 卡顿优化
- 帧率优化、掉帧检测、Choreographer 原理
- 性能检测工具：Systrace、HierarchyViewer、UI Automator

### 3. 内存优化
- 内存泄露排查（LeakCanary）
- Bitmap 优化、内存缓存策略（LruCache）

### 4. 面试爆炸题
- 什么情况下应用会出现 ANR？你如何解决？
- 你在某项目中优化过什么？怎么衡量效果？

---

## 第七阶段：NDK、系统原理与面试应战

**目标：提升系统层理解与源码级调试能力，在高级岗面试中不被轻视**

### 1. 系统机制
- Android 启动流程、Zygote、AMS、WMS 原理
- Binder 通信机制
- APK 安装流程与签名验证

### 2. JNI & NDK
- C/C++ 与 Java 通信机制
- native 层异常处理、日志调试技巧

### 3. 面试狂暴区
- App 是怎么被 AMS 启动的？
- 说说 Binder 为什么要用它？它和 AIDL 是啥关系？

---

## 附录：面试高频问题 TOP 10

1. Android 为什么使用 Handler？它内部原理是怎样的？
2. Activity 启动流程你能从源码讲一下吗？
3. 什么情况下出现内存泄漏？你怎么查？
4. View 的 measure/layout/draw 是怎么执行的？
5. Retrofit 是怎么实现网络请求的？能换成其他库吗？
6. 冷启动慢如何优化？你都做过哪些手段？
7. App 卡顿问题如何定位？你怎么调过帧率？
8. Jetpack Navigation 有什么坑？你怎么规避？
9. App 被杀重启时如何恢复状态？
10. 怎么使用协程和 Retrofit 优雅组合？

---

## 推荐学习资源（别光刷博客，自己造 Bug 才是真的）

- 📘《Android开发艺术探索》by 任玉刚
- 📘《Android高级进阶》by 刘望舒
- 📚 官方文档：developer.android.com
- 🛠️ 工具：LeakCanary、BlockCanary、Systrace、Profiler、Android Studio Memory Inspector
- 🧪 练习项目：
  - 仿微信聊天界面（消息流 + 异步 + 多端适配）
  - 组件化电商 App（模块解耦 + MVVM + Jetpack）
  - 自定义 View 系列（图表组件、滑动开关、折叠面板）
