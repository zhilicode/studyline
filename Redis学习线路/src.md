[ 2025.4.17更新 ]

## 第一阶段：Redis 概述与安装

**目标**：了解 Redis 是什么、适用场景，以及如何安装运行 Redis。

### 1. Redis 简介 [学习Redis基础](https://gostudynow.cn/home/detail/403)
- Redis 是什么？
- 内存数据库 + 键值存储 + 缓存中间件 + 消息队列
- 和 SQL、NoSQL 的对比：数据结构灵活，适合高性能读写
- 常见应用场景：
  - 缓存热点数据
  - 排行榜 / 计数器系统
  - 用户登录会话管理
  - 实时消息发布订阅

### 2. 安装与启动 Redis [学习安装启动](https://gostudynow.cn/home/detail/404)
- 安装方式：
  - 包管理器（apt、brew、yum）
  - 官方预编译包
  - Docker 运行 Redis 容器
- 启动服务：
  - `redis-server`
- 连接客户端：
  - `redis-cli` 基本用法
- 关闭与后台运行设置

---

## 第二阶段：基础命令与数据类型

**目标**：掌握 Redis 最基本的数据类型和操作方式。

### 1. 字符串（String） [学习Redis的字符串](https://gostudynow.cn/home/detail/405)
- 设置和获取：`SET`、`GET`
- 数值操作：`INCR`、`DECR`
- 其他命令：`APPEND`、`STRLEN`

### 2. 列表（List） [学习Redis的列表](https://gostudynow.cn/home/detail/406)
- 插入：`LPUSH`、`RPUSH`
- 弹出：`LPOP`、`RPOP`
- 查询：`LRANGE`、`LLEN`、`LINDEX`

### 3. 集合（Set） [学习Redis的集合](https://gostudynow.cn/home/detail/407)
- 添加与删除元素：`SADD`、`SREM`
- 查询与运算：`SMEMBERS`、`SINTER`、`SUNION`、`SDIFF`

### 4. 哈希（Hash）[学习Redis的哈希](https://gostudynow.cn/home/detail/408)
- 增删改查：`HSET`、`HGET`、`HDEL`
- 获取全部字段：`HGETALL`、`HEXISTS`

### 5. 有序集合（Sorted Set）[学习Redis的有序集合](https://gostudynow.cn/home/detail/409)
- 添加元素：`ZADD`
- 查询：`ZRANGE`、`ZRANK`、`ZCOUNT`
- 修改分数：`ZINCRBY`
- 删除元素：`ZREM`

---

## 第三阶段：键管理与通用功能

**目标**：掌握键名管理、通配符查询、过期设置和基本通用命令。

### 1. 键操作 [学习键操作](https://gostudynow.cn/home/detail/410)
- 删除键：`DEL`
- 查询键：`KEYS`、`SCAN`
- 判断是否存在：`EXISTS`
- 设置过期时间：`EXPIRE`、`TTL`

### 2. 批量操作 [学习批量操作](https://gostudynow.cn/home/detail/411)
- 多键写入：`MSET`
- 多键读取：`MGET`

### 3. 原子性与流水线 [学习原子性](https://gostudynow.cn/home/detail/412)
- Redis 命令天然原子性
- `MULTI` / `EXEC` 实现事务
- `WATCH` 实现乐观锁
- Pipelining 提高网络性能

---

## 第四阶段：高级数据结构与场景实战

**目标**：掌握 Redis 提供的高级数据结构，理解它们的应用场景。

### 1. 位图（Bitmaps）[学习位图](https://gostudynow.cn/home/detail/413)
- 存储用户行为：`SETBIT`、`GETBIT`
- 统计签到次数：`BITCOUNT`、`BITOP`

### 2. HyperLogLog（基数估算）[学习HyperLogLog](https://gostudynow.cn/home/detail/414)
- 统计去重访问数：`PFADD`、`PFCOUNT`、`PFMERGE`

### 3. 流（Streams） [学习Redis的流](https://gostudynow.cn/home/detail/415)
- 高性能日志队列：`XADD`、`XREAD`、`XRANGE`

### 4. 地理空间数据 [学习地理空间数据](https://gostudynow.cn/home/detail/416)
- 添加坐标：`GEOADD`
- 附近搜索：`GEOSEARCH`

### 5. 发布与订阅（Pub/Sub）[学习发布订阅](https://gostudynow.cn/home/detail/417)
- 消息广播机制：`SUBSCRIBE`、`PUBLISH`、`UNSUBSCRIBE`

---

## 第五阶段：数据持久化机制

**目标**：理解 Redis 持久化选项、保存策略与故障恢复能力。

### 1. RDB（快照）[学习RDB](https://gostudynow.cn/home/detail/418)
- 定期保存数据文件
- 配置 `save` 规则
- 适合冷备份和灾难恢复

### 2. AOF（追加日志）[学习AOF](https://gostudynow.cn/home/detail/419)
- 每次写操作都会记录日志
- 日志重放恢复数据
- 自动重写防止文件膨胀

### 3. 持久化策略选择 [学习持久化策略选择](https://gostudynow.cn/home/detail/420)
- RDB vs AOF 区别与权衡
- 混合持久化
- 禁用持久化模式

---

## 第六阶段：高可用与分布式部署

**目标**：掌握 Redis 的主从复制、高可用机制与集群能力。

### 1. 主从复制 [学习主从复制](https://gostudynow.cn/home/detail/421)
- `slaveof` 指令配置
- 主从同步机制
- 读写分离应用

### 2. Sentinel 哨兵模式 [学习哨兵模式](https://gostudynow.cn/home/detail/422)
- 自动故障转移
- 高可用架构推荐方式
- 配置示例与实践

### 3. Redis Cluster [学习集群模式](https://gostudynow.cn/home/detail/423)
- 分区存储，支持水平扩展
- 节点之间数据迁移
- 使用 `CLUSTER` 命令操作

---

## 第七阶段：安全配置与性能优化

**目标**：保障 Redis 安全运行，掌握性能调优技巧。

### 1. 安全设置 [学习安全设置](https://gostudynow.cn/home/detail/424)
- 设置访问密码
- 禁用危险命令
- 启用 TLS 加密连接

### 2. 性能调优 [学习性能调优](https://gostudynow.cn/home/detail/425)
- 最大内存策略：LRU、LFU
- 慢查询日志分析
- 使用 `INFO`、`MONITOR` 监控运行状态
- `redis-benchmark` 压测工具

---

## 第八阶段：模块扩展与企业版本

**目标**：了解 Redis 模块生态与企业级增强功能。

### 1. 官方模块 [学习官方模块](https://gostudynow.cn/home/detail/426)
- RedisJSON：存储结构化文档
- RedisBloom：概率数据结构
- RedisTimeSeries：时间序列数据处理
- RedisSearch：全文搜索能力

### 2. Redis Enterprise（商业版） [学习企业版](https://gostudynow.cn/home/detail/427)
- 多活数据同步（Active-Active）
- Redis on Flash（冷热分层存储）
- 更强的安全、合规性与 SLA 支持

---

## 附录：推荐学习资源与实践建议

### 推荐资源
- 官方文档：[https://redis.io](https://redis.io)
- Redis 教程网站：roadmap.sh、菜鸟教程
- GUI 工具推荐：RedisInsight、Redis Commander

### 学习建议
- 从安装 Redis + CLI 实验开始
- 每学一个数据结构就模拟一个小场景练习
- 后期搭建主从 + 哨兵 + 集群综合练习
- 用真实小项目强化缓存设计理解，如博客点赞、秒杀系统等
