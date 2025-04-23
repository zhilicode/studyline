[ 2025.4.18更新 ]
## 第一阶段：SQL 与关系数据库基础

目标：理解关系型数据库基本概念与 SQL 语言的整体结构。

### 1. 什么是关系型数据库[学习关系型数据库](https://gostudynow.cn/home/detail/257)
- 表格式存储（行与列）
- 主键、外键与关系模型
- 常见 RDBMS：MySQL、PostgreSQL、SQL Server、Oracle

### 2. SQL 与 NoSQL 的区别 [学习SQL和NoSQL](https://gostudynow.cn/home/detail/258)
- SQL 强一致性、结构化
- NoSQL 灵活扩展、弱一致性

### 3. SQL 的分类 [学习SQL分类](https://gostudynow.cn/home/detail/259)
- 数据定义语言（DDL）：CREATE、ALTER、TRUNCATE
- 数据操作语言（DML）：SELECT、INSERT、UPDATE、DELETE
- 数据控制语言（DCL）：GRANT、REVOKE
- 事务控制语言（TCL）：BEGIN、COMMIT、ROLLBACK、SAVEPOINT

---

## 第二阶段：基础 SQL 查询语法

目标：掌握最常用的查询与数据操作指令。

### 1. 数据操作语句（DML） [学习DML基础](https://gostudynow.cn/home/detail/260)
- 查询数据：SELECT
- 插入数据：INSERT INTO
- 更新数据：UPDATE ... SET ... WHERE
- 删除数据：DELETE FROM

### 2. 关键子句 [学习SQL子句](https://gostudynow.cn/home/detail/261)
- FROM：指定查询表
- WHERE：条件筛选
- ORDER BY：排序（ASC / DESC）
- GROUP BY + HAVING：分组聚合
- LIMIT / OFFSET：分页

### 3. 聚合函数 [学习聚合函数](https://gostudynow.cn/home/detail/262)
- COUNT()、SUM()、AVG()、MIN()、MAX()

---

## 第三阶段：数据建模与约束

目标：了解如何设计数据表并设置数据完整性。

### 1. 创建与修改表结构（DDL） [学习DDL基础](https://gostudynow.cn/home/detail/264)
- CREATE TABLE
- ALTER TABLE
- TRUNCATE TABLE

### 2. 数据类型与列属性 [学习SQL类型和列属性](https://gostudynow.cn/home/detail/265)
- 字符类型、数字类型、时间类型
- NULL、NOT NULL
- DEFAULT 默认值设置

### 3. 约束类型 [学习约束类型](https://gostudynow.cn/home/detail/266)
- PRIMARY KEY
- FOREIGN KEY
- UNIQUE
- CHECK

---

## 第四阶段：多表连接与子查询 [学习子查询和嵌套](https://gostudynow.cn/home/detail/263)

目标：学会在多表之间进行联合查询与嵌套查询。

### 1. JOIN 操作 [学习JOIN全家桶](https://gostudynow.cn/home/detail/267)
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL OUTER JOIN
- SELF JOIN
- CROSS JOIN

### 2. 子查询 [学习子查询](https://gostudynow.cn/home/detail/268)
- 标量子查询（返回单个值）
- 行子查询（返回单行）
- 表子查询（返回多行多列）

### 3. 子查询类型 [学习进阶子查询](https://gostudynow.cn/home/detail/269)
- 嵌套子查询
- 相关子查询（使用主查询中的值）

---

## 第五阶段：函数与表达式

目标：掌握 SQL 中的字符串、时间、数值函数与条件表达式。

### 1. 字符串函数 [学习字符串函数](https://gostudynow.cn/home/detail/270)
- CONCAT、LENGTH、SUBSTRING、REPLACE
- UPPER() / LOWER()

### 2. 日期时间函数 [学习日期函数](https://gostudynow.cn/home/detail/271)
- NOW()、DATEPART()、DATEADD()
- TIMESTAMP 操作

### 3. 数值函数 [学习数值函数](https://gostudynow.cn/home/detail/272)
- FLOOR()、ROUND()、ABS()、MOD()、CEILING()

### 4. 逻辑函数 [学习逻辑函数](https://gostudynow.cn/home/detail/273)
- CASE WHEN
- NULLIF()、COALESCE()

---

## 第六阶段：视图与索引

目标：提高查询效率与逻辑结构复用。

### 1. 视图（View） [学习视图View](https://gostudynow.cn/home/detail/274)
- 创建视图：CREATE VIEW
- 修改视图：ALTER VIEW
- 删除视图：DROP VIEW

### 2. 索引（Index） [学习索引](https://gostudynow.cn/home/detail/275)
- 什么是索引，如何提升查询性能
- 创建、修改、删除索引
- 使用 BTree 索引、哈希索引
- 避免索引失效的常见原因

---

## 第七阶段：事务控制与数据一致性

目标：理解数据库事务和隔离级别，确保数据可靠性。

### 1. 事务基本操作 [学习事务基本操作](https://gostudynow.cn/home/detail/276)
- 开始事务：BEGIN
- 提交事务：COMMIT
- 回滚事务：ROLLBACK
- 设置保存点：SAVEPOINT

### 2. ACID 原则 [学习ACID原则](https://gostudynow.cn/home/detail/277)
- 原子性（Atomicity）
- 一致性（Consistency）
- 隔离性（Isolation）
- 持久性（Durability）

### 3. 隔离级别 [学习隔离级别](https://gostudynow.cn/home/detail/278)
- Read Uncommitted
- Read Committed
- Repeatable Read
- Serializable

---

## 第八阶段：高级 SQL 与优化技巧

目标：掌握复杂 SQL 编写和性能优化技巧。

### 1. 高级查询语法 [学习高级查询](https://gostudynow.cn/home/detail/279)
- 递归查询（WITH RECURSIVE）
- CTE（公共表表达式）[学习CTE](https://gostudynow.cn/home/detail/282)
- PIVOT / UNPIVOT 操作
- 动态 SQL（如 EXECUTE IMMEDIATE）

### 2. 窗口函数 [学习窗口函数](https://gostudynow.cn/home/detail/280)
- ROW_NUMBER()、RANK()、DENSE_RANK()
- LEAD()、LAG()
- OVER() 分区与排序

### 3. 查询优化 [学习查询优化](https://gostudynow.cn/home/detail/281)
- 使用索引进行过滤
- 选择性投影（只查询需要的列）
- 避免过度嵌套子查询
- EXPLAIN 查询分析工具使用

---

## 第九阶段：权限控制与安全性

目标：保障数据的安全访问与最小权限原则。

### 1. 用户权限 [学习用户权限](https://gostudynow.cn/home/detail/283)
- GRANT 授权
- REVOKE 撤销权限

### 2. 数据完整性控制 [学习数据完整性](https://gostudynow.cn/home/detail/284)
- 通过约束限制数据错误写入
- 使用视图限制敏感列访问

### 3. 最佳实践 [学习最佳实践](https://gostudynow.cn/home/detail/285)
- 防止 SQL 注入
- 使用参数化查询
- 最小权限原则

---

## 推荐资源与学习建议

### 学习建议：
- 多练习 SELECT 查询与 JOIN 组合
- 每学一个函数就在本地数据库实践
- 用一个实际系统（如图书馆管理系统）设计数据库

### 推荐资源：
- [w3schools SQL 教程](https://www.w3schools.com/sql/)
- [PostgreSQL 官方文档](https://www.postgresql.org/docs/)
- [SQLZoo 在线练习](https://sqlzoo.net/)

---