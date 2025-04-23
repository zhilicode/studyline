[ 2025.4.17更新 ]

## MyBatis 面试学习线路（七大阶段）

### 目标：全面掌握 MyBatis 核心机制、动态 SQL、缓存策略、插件机制、Spring 整合与常见面试题，胜任中高级 Java 岗位面试。

---

## 第一阶段：MyBatis 基础认知

**目标：理解 ORM 框架的意义与 MyBatis 的定位**

### 1. 什么是 MyBatis？
- 一款优秀的半自动 ORM 框架
- 对 SQL 有较强掌控权，适合复杂 SQL 场景
- 和 Hibernate（全自动 ORM）的区别

### 2. 使用场景与优缺点
- 场景：复杂 SQL、多表联合查询、灵活控制
- 优点：灵活、简单、易于调试
- 缺点：SQL 手写维护成本高、不具备自动建表能力

### 3. 与 SpringBoot 集成方式
- 依赖配置（starter）
- 自动装配 Mapper、SqlSessionFactory

---

## 第二阶段：核心组件与执行流程

**目标：掌握 MyBatis 的核心架构与运行机制**

### 1. MyBatis 的执行流程
- 用户发起请求 → Mapper 接口 → Mapper 映射文件 → SqlSession → Executor → StatementHandler → JDBC 执行

### 2. 核心组件
- SqlSession：与数据库交互的会话
- Executor：执行器（Simple、Reuse、Batch）
- StatementHandler：预处理语句
- ResultSetHandler：结果集处理
- ParameterHandler：参数处理器

### 3. 配置文件结构
- mybatis-config.xml：全局配置
- mapper.xml：SQL 映射文件（一个接口对应一个 XML）

---

## 第三阶段：SQL 映射与注解方式

**目标：熟练掌握 XML 与注解两种 SQL 编写方式**

### 1. XML 映射方式
- `select`、`insert`、`update`、`delete` 标签
- `parameterType` 和 `resultType`
- 示例：用户表的增删改查 XML 配置

### 2. 注解开发方式
- `@Select`、`@Insert`、`@Update`、`@Delete`
- 与 XML 的优劣对比（小型项目推荐注解，大型项目推荐 XML）

### 3. 命名空间与接口绑定
- Mapper 接口与 XML 文件同名 + 同路径
- 使用代理对象完成 SQL 执行

---

## 第四阶段：动态 SQL 与高级映射

**目标：掌握 MyBatis 的动态 SQL 能力和复杂数据映射技巧**

### 1. 动态 SQL 标签
- `if`、`choose`、`when`、`otherwise`
- `where`、`set`、`trim`、`foreach`
- 场景：条件查询、多字段更新、批量操作

### 2. 高级结果映射
- `resultMap` 映射复杂对象
- 一对一映射：association
- 一对多映射：collection
- 多表联合查询结果封装技巧

### 3. SQL 片段重用
- `sql` + `include` 标签实现 SQL 复用

---

## 第五阶段：缓存机制与分页插件

**目标：掌握一级缓存、二级缓存原理与常用插件机制**

### 1. 一级缓存
- 默认开启，基于 SqlSession 作用域
- 同一个会话中，相同查询不会重复访问数据库
- 清除方式：手动清除、执行更新操作

### 2. 二级缓存
- 基于 Mapper 作用域，跨 SqlSession
- 可自定义缓存实现（如 EhCache、Redis）
- 开启方式与序列化要求

### 3. 分页插件
- PageHelper 插件原理（利用拦截器）
- MyBatis Plus 自带分页插件

---

## 第六阶段：插件机制与自定义扩展

**目标：理解 MyBatis 的插件机制与常用拦截器开发场景**

### 1. 插件原理（拦截器机制）
- 拦截对象：Executor、StatementHandler、ResultSetHandler、ParameterHandler
- 自定义插件实现 Interceptor 接口
- 使用 @Intercepts、@Signature 注解绑定目标

### 2. 常见插件使用
- SQL 打印插件（打印真实执行 SQL）
- 性能分析插件
- 参数加解密插件（敏感字段处理）

---

## 第七阶段：Spring 整合与实战优化

**目标：掌握 SpringBoot + MyBatis 项目实战要点及面试考点**

### 1. SpringBoot 整合 MyBatis
- 使用 `@MapperScan`、`@Mapper`
- 自动装配 SqlSessionFactoryBean
- Mapper 注入方式（依赖注入）

### 2. 实战注意事项
- Mapper 接口必须与 XML 一一对应
- 防止全表更新的写法（`<where>` 标签）
- SQL 调试技巧（日志级别设为 debug）

### 3. 面试常问问题
- MyBatis 如何实现动态 SQL？
- MyBatis 中如何做一对多映射？
- MyBatis 和 Hibernate 区别？
- MyBatis 的缓存有哪些，如何清除？
- 怎么解决 XML 映射文件不生效问题？
- MyBatis 插件的原理？你写过自定义拦截器吗？
- 分页插件为什么有效？是怎么实现的？

---

## 附录：面试实战建议与资源推荐

### 面试建议
- 动态 SQL 与映射是重点
- 多表查询结果封装建议重点演练
- 一级/二级缓存问题易被深挖
- 插件开发原理需理解 Java 动态代理

### 学习资源
- 官方文档：https://mybatis.org/mybatis-3/
- 实战框架推荐：MyBatis Plus
- 面试题仓库：GitHub 搜索 "MyBatis Interview Questions"
- 推荐图书：《MyBatis 从入门到精通》、《Java 数据持久层开发实战》
