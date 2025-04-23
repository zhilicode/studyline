[ 2025.4.18更新 ]
## 第一阶段：语言入门（基础语法）

目标：理解 C++ 的基本语法和程序结构，能编写简单程序。

### 1. C++ 概述 [学习C++入门](https://gostudynow.cn/home/detail/212)
- 什么是 C++
- C 与 C++ 的区别
- C++ 的应用领域（系统开发、游戏、嵌入式、高性能计算）

### 2. 开发环境配置 [学习C++环境](https://gostudynow.cn/home/detail/213)
- 安装编译器（GCC / Clang / MSVC）
- 配置 IDE（Visual Studio / CLion / VSCode）
- 编译与运行第一个程序

### 3. 基本语法
- 数据类型与变量
- 运算符：算术、逻辑、位运算 [学习运算基础](https://gostudynow.cn/home/detail/214)
- 控制结构：if / else、switch、for、while、do...while [学习if控制](https://gostudynow.cn/home/detail/215)|[学习while控制](https://gostudynow.cn/home/detail/216)
- 输入输出：cin / cout（iostream）
- 数组 [学习数组](https://gostudynow.cn/home/detail/217)
- 类型系统 [学习类型系统](https://gostudynow.cn/home/detail/223)
- 结构体和枚举 [学习结构体和枚举](https://gostudynow.cn/home/detail/255)

---

## 第二阶段：函数与结构化编程

目标：掌握函数调用机制，理解作用域与代码组织方式。

### 1. 函数 [学习函数](https://gostudynow.cn/home/detail/220)
- 函数声明与定义
- 值传递与引用传递
- 默认参数
- 函数重载（静态多态）
- lambda匿名函数 [学习匿名函数](https://gostudynow.cn/home/detail/221)

### 2. 代码组织 
- 作用域与命名空间 [学习命名空间](https://gostudynow.cn/home/detail/232)｜[学习作用域](https://gostudynow.cn/home/detail/233)
- 头文件与源文件（.h 和 .cpp 分离） [学习代码分离](https://gostudynow.cn/home/detail/231)
- 前向声明 [学习前向声明](https://gostudynow.cn/home/detail/230)

---

## 第三阶段：内存管理与指针机制

目标：掌握 C++ 内存模型与指针使用，理解智能指针用法。

### 1. 指针与引用
- 基本指针语法、空指针、野指针
- 引用与引用传参[学习引用](https://gostudynow.cn/home/detail/225)
- 指针与数组关系
- 函数指针 [学习函数指针](https://gostudynow.cn/home/detail/222)

### 2. 动态内存管理 [学习内存模型](https://gostudynow.cn/home/detail/226)
- new 与 delete [学习原始指针](https://gostudynow.cn/home/detail/229)
- 内存泄漏与检测工具（Valgrind）
- RTTI运行时类型 [学习RTTI](https://gostudynow.cn/home/detail/224)
- 对象生命周期 [学习生命周期](https://gostudynow.cn/home/detail/227)

### 3. 智能指针（C++11 起） [学习RAII智能指针](https://gostudynow.cn/home/detail/228)
- unique_ptr
- shared_ptr / weak_ptr
- 生命周期与引用计数

---

## 第四阶段：面向对象编程（OOP）

目标：掌握 C++ 的类与继承体系，理解多态和虚函数原理。

### 1. 类与结构体 [学习面向对象](https://gostudynow.cn/home/detail/234)
- 成员变量与成员函数
- 构造函数、析构函数
- this 指针与对象拷贝
- 结构体和枚举

### 2. 面向对象三大特性
- 封装：访问控制、友元函数 [学习封装友元](https://gostudynow.cn/home/detail/237)
- 继承：单继承、多继承、菱形继承 [学习继承](https://gostudynow.cn/home/detail/238)
- 多态：
  - 静态多态（函数重载、运算符重载）[学习静态多态](https://gostudynow.cn/home/detail/236)
  - 动态多态（虚函数、虚表）[学习动态多态](https://gostudynow.cn/home/detail/235)

### 3. C++ 特有规则
- Rule of Three / Rule of Five / Rule of Zero [学习Rule资源管理](https://gostudynow.cn/home/detail/239)
- 抽象类与接口设计 [学习抽象类和接口](https://gostudynow.cn/home/detail/240)

---

## 第五阶段：模板与元编程

目标：掌握泛型编程能力，了解模板高级特性。

### 1. 模板基础 [学习模板基础](https://gostudynow.cn/home/detail/241)
- 函数模板、类模板
- 模板参数推导

### 2. 高级模板技巧 [学习模板高级技巧](https://gostudynow.cn/home/detail/242)
- 偏特化与全特化
- 可变参数模板（Variadic Templates）
- SFINAE（Substitution Failure Is Not An Error）
- Type Traits 与模板元编程

### 3. 常用模板编程 Idioms [学习模板Idioms](https://gostudynow.cn/home/detail/243)
- CRTP（Curiously Recurring Template Pattern）
- Pimpl（指针隐藏实现）

---

## 第六阶段：标准库与 STL 容器

目标：熟练使用 STL 提供的容器与算法。

### 1. 容器
- 顺序容器：vector、list、deque [学习vector](https://gostudynow.cn/home/detail/218)|[学习List链表](https://gostudynow.cn/home/detail/244)|[学习Deque双端队列](https://gostudynow.cn/home/detail/245)
- 关联容器：set、unordered_set、map、unordered_map [学习集合set](https://gostudynow.cn/home/detail/256)|[学习map](https://gostudynow.cn/home/detail/219)|[学习unordered_map](https://gostudynow.cn/home/detail/246)
- 适配器容器：stack、queue [学习stack/queue](https://gostudynow.cn/home/detail/247)

### 2. 算法与迭代器
- 常用算法（查找、排序、遍历）
- Lambda 表达式（C++11） [学习匿名函数](https://gostudynow.cn/home/detail/221)
- 自定义排序器与谓词 [学习排序器与谓词](https://gostudynow.cn/home/detail/248)

### 3. 工具类 [学习工具类](https://gostudynow.cn/home/detail/249)
- std::string
- 时间处理
- std::optional / std::variant / std::any（C++17）

---

## 第七阶段：异常处理与调试工具

目标：掌握错误处理机制，能使用调试器排查问题。

### 1. 异常处理 [学习异常](https://gostudynow.cn/home/detail/250)
- try / catch / throw
- 自定义异常类
- 程序崩溃原因与访问违规

### 2. 调试器与工具链 [学习调试工具](https://gostudynow.cn/home/detail/251)
- GDB / WinDbg 调试技巧
- 编译阶段与调试符号
- 断点、内存查看、调用栈

---

## 第八阶段：构建系统与依赖管理

目标：了解项目构建流程与常用包管理工具。

### 1. 构建系统
- Makefile
- CMake
- Ninja 构建系统

### 2. 包管理工具
- vcpkg
- Conan
- NuGet / Spack

---

## 第九阶段：现代 C++ 与生态实践

目标：掌握 C++11/14/17/20 标准中的重要特性。

### 1. 自动类型推导 [学习auto自动推导](https://gostudynow.cn/home/detail/252)
- auto、decltype、constexpr

### 2. 并发与多线程 [学习多线程](https://gostudynow.cn/home/detail/253)
- std::thread
- std::mutex / condition_variable [学习高级并发](https://gostudynow.cn/home/detail/254)

### 3. 第三方库与框架
- 图形界面：Qt
- 数学/图像：OpenCV、Eigen
- 网络与 RPC：Boost、gRPC、POCO
- 机器学习：TensorFlow C++、PyTorch C++

### 4. 日志与测试框架
- 日志库：spdlog、fmt
- 单元测试：gtest、Catch2

---

## 附录：推荐资源与学习建议

### 推荐资源：
- [cppreference.com](https://en.cppreference.com/)
- [ISO C++ 官方网站](https://isocpp.org/)

### 学习建议：
- 一边学语法一边写小项目（如图书管理系统、贪吃蛇）
- 多阅读开源库源码理解底层设计
- 持续关注 C++ 标准演进（C++20 / C++23）

---