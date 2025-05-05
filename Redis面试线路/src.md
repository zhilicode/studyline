[ 2025.4.17更新 ]

## Redis 面试学习线路（七阶段全体系）

### 目标：系统掌握 Redis 的核心机制、应用场景、性能优化和面试高频问题，为中高级后端面试打下扎实基础。

---

## 第一阶段：Redis 基础认知 [学习Redis基础](https://gostudynow.cn/home/detail/403)

**目标：理解 Redis 的定位、使用场景与架构优势**

### 1. 什么是 Redis？ 
- 内存级高性能键值数据库
- 支持多种数据结构的 NoSQL 数据库
- 可做缓存、中间件、持久化存储、排行榜、消息队列等用途

### 2. Redis 的应用场景
- 缓存热点数据，减轻数据库压力
- 分布式锁、限流器
- 排行榜（ZSet）
- 用户签到、在线状态
- 发布/订阅系统（Pub/Sub）

### 3. Redis 与 Memcached、MySQL 的区别
- 持久化机制
- 支持的数据结构丰富
- 支持事务与 Lua 脚本
- 单线程模型设计与性能对比

---

## 第二阶段：核心数据结构与应用场景

**目标：掌握 Redis 五大基本数据结构的用法与面试考点**

### 1. 字符串（String） [学习Redis的字符串](https://gostudynow.cn/home/detail/405)
- 简单值存储、计数器、分布式唯一 ID
- 命令：SET、GET、INCR、DECR、APPEND

### 2. 列表（List）  [学习Redis的列表](https://gostudynow.cn/home/detail/406)
- 消息队列、文章评论区
- 命令：LPUSH、RPUSH、LPOP、LRANGE、BLPOP

### 3. 哈希（Hash）[学习Redis的哈希](https://gostudynow.cn/home/detail/408)
- 对象结构存储（如用户信息）
- 命令：HSET、HGET、HGETALL、HDEL

### 4. 集合（Set）[学习Redis的集合](https://gostudynow.cn/home/detail/407)
- 去重统计、共同好友
- 命令：SADD、SMEMBERS、SINTER、SUNION

### 5. 有序集合（Sorted Set）[学习Redis的有序集合](https://gostudynow.cn/home/detail/409)
- 排行榜、延时任务调度
- 命令：ZADD、ZRANK、ZREVRANGE、ZINCRBY

---

## 第三阶段：过期机制与内存淘汰策略

**目标：理解 Redis 的内存控制机制与缓存失效策略** [学习键过期机制+内存淘汰](https://gostudynow.cn/home/detail/428)

### 1. 键的过期机制 
- 设置过期时间：EXPIRE、TTL、SETEX
- 惰性删除 + 定期删除策略
 
### 2. 内存淘汰策略
- noeviction（默认）、allkeys-lru、volatile-lru、allkeys-random、volatile-ttl
- 面试考点：Redis 如何防止内存爆掉？淘汰策略有什么优劣？

### 3. 缓存雪崩、穿透、击穿的解决方案 [学习雪崩+击穿+穿透](https://gostudynow.cn/home/detail/429)
- 加锁、布隆过滤器、异步更新、热点预热

---

## 第四阶段：持久化机制

**目标：深入掌握 Redis 的两种持久化方式及其适用场景**

### 1. RDB 快照 [学习RDB](https://gostudynow.cn/home/detail/418)
- 配置保存周期
- 全量备份，适合冷备份与容灾恢复

### 2. AOF 日志 [学习AOF](https://gostudynow.cn/home/detail/419)
- 每次写操作记录日志
- 重写机制、AOF 文件膨胀问题
- 面试常问：RDB 和 AOF 区别？如何选择？

### 3. 混合持久化 [学习混合持久化](https://gostudynow.cn/home/detail/420)
- RDB + AOF，Jedis 默认开启
- 数据一致性与恢复效率兼顾

---

## 第五阶段：高可用与集群架构

**目标：掌握 Redis 的主从复制、哨兵机制与集群搭建方式**

### 1. 主从复制 [学习主从复制](https://gostudynow.cn/home/detail/421)
- 读写分离，Slave 自动同步主节点
- 延迟问题、复制一致性问题（异步复制）

### 2. Redis Sentinel（哨兵） [学习哨兵模式](https://gostudynow.cn/home/detail/422)
- 自动故障切换
- 哨兵监控主节点状态，选举新的主节点
- 面试高频：Redis 怎么实现高可用？

### 3. Redis Cluster（分片集群）[学习集群模式](https://gostudynow.cn/home/detail/423)
- 水平扩展，数据按 slot 分布
- 节点数、主从模式、复制槽原理
- 面试高频：Redis 集群如何分片？如何保证一致性？

---

## 第六阶段：事务、分布式锁与脚本

**目标：掌握 Redis 的原子性操作与分布式特性**

### 1. 事务机制 [学习原子事务](https://gostudynow.cn/home/detail/412)
- MULTI、EXEC、WATCH 实现事务控制
- 事务不支持回滚！非原子性事务（与数据库事务的区别）

### 2. 分布式锁 [学习分布式锁](https://gostudynow.cn/home/detail/430)
- SETNX + EXPIRE 实现
- Redisson 实现分布式锁的原理
- 如何解决锁续期、死锁、锁释放安全问题？

### 3. Lua 脚本 [学习Lua脚本](https://gostudynow.cn/home/detail/431)
- EVAL 命令执行原子操作
- 面试考点：为什么分布式锁用 Lua 实现更安全？

---

## 第七阶段：性能调优与运维监控

**目标：掌握 Redis 的调优手段、监控工具与常见问题排查**

### 1. 慢查询分析 [学习慢查询+大Key+热Key](https://gostudynow.cn/home/detail/432)
- 设置慢查询阈值
- 使用 MONITOR、SLOWLOG 排查问题

### 2. 常见问题
- 大 key 问题（过大对象导致阻塞）
- 热 key 问题（集中访问导致热点）

### 3. Redis 工具链
- redis-cli：基本命令行工具
- RedisInsight：图形化管理
- redis-benchmark：性能压测工具
- RDB/AOF 文件备份与恢复

---

## 附录：面试高频问题汇总

1. Redis 单线程模型为何性能还这么高？ [学习Redis高频面试系列1（1-9）](https://gostudynow.cn/home/detail/433)
2. Redis 为什么不直接用 Java 实现？
3. 如何实现缓存与数据库双写一致性？
4. Redis 分布式锁如何避免误删？
5. 如何解决 Redis 缓存穿透、雪崩问题？
6. Redis 内存满了之后会发生什么？
7. Redis 如何做主从切换、如何保证数据不丢？
8. Redis 集群如何分片？如何保证一致性？
9. Redis 怎么实现高可用？

---

## 推荐资料

- 《Redis 设计与实现》
- 官方文档：https://redis.io/
- 工具推荐：RedisInsight、Redis Desktop Manager、VisualVM + JMX
- 在线测试环境：https://try.redis.io
