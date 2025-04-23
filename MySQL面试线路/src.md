[ 2025.4.17更新 ]
## MySQL 面试学习线路（八大阶段）

### 目标：系统掌握 MySQL 的基本语法、索引优化、事务隔离、锁机制、执行计划与高频面试题，提升数据库性能调优与排障能力。

---

## 第一阶段：MySQL 基础与常用语法

**目标：掌握 MySQL 基础概念与常用数据操作**

### 1. MySQL 简介
- 常用版本（MySQL、MariaDB、Percona）
- MySQL 架构图：连接层、SQL 层、存储引擎层

### 2. 基本 SQL 操作
- 数据查询：SELECT、WHERE、ORDER BY、LIMIT
- 数据修改：INSERT、UPDATE、DELETE
- 数据定义：CREATE TABLE、ALTER、DROP
- 分组聚合：GROUP BY、HAVING

### 3. 表设计基础
- 主键、外键、唯一约束
- NOT NULL、DEFAULT、AUTO_INCREMENT
- 表的三范式概念

---

## 第二阶段：索引机制与优化策略

**目标：理解索引类型与原理，掌握建索引与优化技巧**

### 1. 索引基础
- 索引分类：主键索引、唯一索引、普通索引、联合索引、全文索引
- 索引底层结构：B+ 树（重点）、哈希索引（Memory）

### 2. 索引优化
- 最左前缀原则
- 覆盖索引（使用 SELECT 的字段都在索引中）
- 索引下推（ICP）

### 3. 常见索引失效场景
- 使用函数、like '%xx'、or、隐式转换等
- 面试常问：为什么索引会失效？如何避免？

---

## 第三阶段：事务与隔离级别

**目标：掌握事务机制、并发问题与隔离级别实现方式**

### 1. 事务四大特性（ACID）
- 原子性、一致性、隔离性、持久性

### 2. MySQL 事务管理
- InnoDB 支持事务，MyISAM 不支持
- 显式事务：START TRANSACTION、COMMIT、ROLLBACK

### 3. 并发问题
- 脏读、不可重复读、幻读

### 4. 隔离级别（重点）
- READ UNCOMMITTED
- READ COMMITTED
- REPEATABLE READ（MySQL 默认）
- SERIALIZABLE
- MVCC 多版本并发控制机制

---

## 第四阶段：锁机制详解

**目标：掌握 MySQL 的行锁、表锁与死锁排查**

### 1. 锁类型
- 表锁 vs 行锁
- 意向锁、共享锁（S）、排他锁（X）
- GAP 锁、临键锁、Next-Key Lock

### 2. 死锁问题
- 如何产生死锁？
- 死锁检测与日志分析

### 3. 面试重点问题
- InnoDB 是怎么加锁的？
- 如何查看当前锁信息？（`information_schema.innodb_locks`）

---

## 第五阶段：查询优化与执行计划分析

**目标：掌握 SQL 执行过程与常见性能调优手段**

### 1. SQL 执行流程
- 解析器 → 查询优化器 → 执行器

### 2. EXPLAIN 分析
- type（访问类型：ALL、index、range、ref、const）
- key、rows、Extra 字段含义
- 示例分析慢 SQL 原因

### 3. 慢查询排查
- 开启慢查询日志
- 使用 `show processlist`、`mysqlslap` 压测工具

---

## 第六阶段：表结构设计与范式应用

**目标：掌握高性能表结构设计原则与范式灵活应用**

### 1. 三大范式
- 第一范式（字段原子性）
- 第二范式（消除部分依赖）
- 第三范式（消除传递依赖）

### 2. 反范式设计
- 实战中为查询效率牺牲部分范式

### 3. 字段类型选择
- int / bigint / varchar / char 差异
- NULL 字段对索引影响

---

## 第七阶段：主从复制与高可用架构

**目标：掌握 MySQL 的读写分离与高可用方案**

### 1. 主从复制
- 原理：binlog → relay log → io thread/sql thread
- 异步、半同步、全同步复制模式
- 延迟问题与解决方案

### 2. 高可用架构方案
- keepalived + VIP
- MHA（已不推荐）/Orchestrator
- 多主复制与冲突处理

### 3. 面试考点
- 如何做读写分离？
- 主从一致性怎么保证？
- 一主多从架构下如何选主？

---

## 第八阶段：面试高频题精讲

**目标：强化面试常见数据库问题的理解与表达能力**

### 高频题目整理
1. InnoDB 和 MyISAM 的区别？
2. B 树和 B+ 树的区别？为什么用 B+ 树？
3. 什么情况下索引失效？
4. 如何排查慢 SQL？
5. SQL 中 group by 和 having 的执行顺序？
6. 事务隔离级别与对应并发问题？
7. MVCC 的原理？Undo log、Redo log？
8. 你们公司怎么做数据库主从架构的？
9. 说说你做过的 SQL 优化？
10. MySQL 如何防止幻读？间隙锁和 next-key lock 是什么？

---

## 附录：推荐学习资料

### 官方与经典文档
- MySQL 官方手册：https://dev.mysql.com/doc/
- 《高性能 MySQL（第 3 版）》
- 《MySQL 技术内幕：InnoDB 存储引擎》

### 常用工具
- Navicat、DataGrip
- explain、show profile、慢日志
- pt-query-digest（Percona 工具集）
