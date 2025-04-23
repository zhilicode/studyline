[ 2025.4.19更新 ]
## 第一阶段：TypeScript 入门

目标：了解 TypeScript 的作用、与 JavaScript 的关系，以及开发环境配置。

### 1. TypeScript 简介 [学习简介](https://gostudynow.cn/home/detail/193)
- TypeScript 是什么？
- TypeScript 与 JavaScript 的区别
- 为什么使用 TypeScript？

### 2. 安装与配置 [学习安装与配置](https://gostudynow.cn/home/detail/194)
- 安装 TypeScript（npm install -g typescript）
- 初始化配置文件（tsc --init）
- 常见 tsconfig.json 配置项讲解 [学习配置详解](https://gostudynow.cn/home/detail/195)
- 使用方式：tsc 编译、ts-node 运行、TS Playground

---

## 第二阶段：基础类型系统

目标：掌握 TypeScript 提供的基础与特殊类型。

### 1. 原始类型 [学习原始类型](https://gostudynow.cn/home/detail/196)
- boolean、number、string
- null、undefined、void

### 2. 特殊类型 [学习特殊类型](https://gostudynow.cn/home/detail/197)
- any（任意类型）
- unknown（安全的任意类型）
- never（不可能的值）
- object（非原始类型）

### 3. 断言与推断 [学习断言与推断](https://gostudynow.cn/home/detail/198)
- 类型断言（as、! 非空断言）
- as const 与 satisfies
- 类型推断机制（自动识别变量类型）

---

## 第三阶段：复合类型与函数类型

目标：掌握 TypeScript 的组合类型、函数参数与重载特性。

### 1. 复合类型 [学习复合类型](https://gostudynow.cn/home/detail/199)
- 联合类型（string | number）
- 交叉类型（A & B）
- 元组类型（Tuple）
- 数组类型（number[] 或 Array<number>）

### 2. 类型别名与守卫 [学习别名和守卫](https://gostudynow.cn/home/detail/200)
- type 关键字
- 类型保护（typeof、instanceof、类型谓词）

### 3. 函数相关 [学习函数](https://gostudynow.cn/home/detail/201)
- 函数声明与返回值类型
- 可选参数、默认值参数
- 剩余参数（Rest）
- 函数重载（Overload）

---

## 第四阶段：对象类型与面向对象

目标：学习接口、类、访问修饰符、继承与抽象等面向对象特性。

### 1. 接口（Interface） [学习接口](https://gostudynow.cn/home/detail/202)
- 接口定义与可选属性
- 只读属性（readonly）
- 接口扩展（继承多个接口）
- 混合类型（Hybrid Type）
- 接口 vs 类型别名

### 2. 类与访问修饰符 [学习类与访问修饰符](https://gostudynow.cn/home/detail/203)
- 构造函数与参数简写
- public、private、protected
- 继承与多态
- 方法重写、抽象类
- keyof 操作符使用

---

## 第五阶段：泛型与高级类型

目标：掌握泛型编程，理解 TypeScript 中的高级类型特性。

### 1. 泛型基础 [学习泛型基础](https://gostudynow.cn/home/detail/204)
- 泛型函数与泛型类
- 泛型约束（extends）
- 默认类型参数

### 2. 高级类型系统 [学习高级系统](https://gostudynow.cn/home/detail/205)
- 条件类型（T extends U ? X : Y）
- 映射类型（Mapped Types）
- 模板字面量类型（Template Literal Types）
- 递归类型（Recursive Types）

### 3. 实用工具类型（Utility Types）[学习使用工具](https://gostudynow.cn/home/detail/206)
- Partial<T>、Pick<T, K>、Omit<T, K>
- Readonly<T>、Record<K, T>
- Exclude<T, U>、Extract<T, U>
- NonNullable<T>
- ReturnType<T>、Parameters<T>、InstanceType<T>、Awaited<T>

---

## 第六阶段：模块系统与声明

目标：理解模块化开发与声明文件的书写与使用。

### 1. 模块类型 [学习模块类型](https://gostudynow.cn/home/detail/207)
- 外部模块（import/export）
- 命名空间模块（namespace）
- Ambient 模块（全局模块声明）

### 2. 模块扩展 [学习模块扩展](https://gostudynow.cn/home/detail/208)
- 命名空间增强（Augmentation）
- 全局变量扩展

---

## 第七阶段：项目实践与生态工具

目标：掌握 TypeScript 项目开发所需的生态工具链。

### 1. 编译与构建 [学习编译构建](https://gostudynow.cn/home/detail/209)
- 构建工具：Webpack、Vite、Rollup 与 TypeScript 配合使用
- 集成 Babel 转译兼容性

### 2. 格式化与规范 [学习格式化规范](https://gostudynow.cn/home/detail/210)
- Lint 工具：ESLint + typescript-eslint
- 格式化工具：Prettier

### 3. 常用生态库 [学习生态库](https://gostudynow.cn/home/detail/211)
- 类型安全网络请求（Axios + 类型）
- React / Vue 的 TypeScript 支持
- 工具库类型提示（如 Lodash）

---

## 附录：学习建议与推荐资源

### 学习建议：
- 从 JS 项目迁移开始练习 TS
- 学会使用 VSCode 的自动补全提示
- 多写声明文件理解类型系统

### 推荐资源：
- [TypeScript 中文文档](https://www.typescriptlang.org/zh/)
- [Type Challenges（类型体操）](https://github.com/type-challenges/type-challenges)

---