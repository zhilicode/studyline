[ 2025.4.17更新 ]
## Java 并发编程面试学习线路（八大阶段）

### 目标：系统掌握 Java 并发编程的核心原理与实战能力，深入理解线程调度、锁机制、内存模型、并发容器、并发工具类等面试必考内容。

---

## 第一阶段：并发基础与线程创建 [学习线程并发](https://gostudynow.cn/home/detail/135)

**目标：理解并发编程的本质与 Java 创建线程的方式**

### 1. 并发与并行的区别 [学习线程基础与创建](https://gostudynow.cn/home/detail/376)
- 并发：逻辑同时执行（单核交替）
- 并行：物理同时执行（多核）

### 2. Java 中创建线程的方式
- 继承 Thread 类
- 实现 Runnable 接口
- 使用 Callable + Future
- 使用线程池（Executor）

### 3. 常见面试题
- 三种线程创建方式有何区别？
- Runnable 和 Callable 的区别？

---

## 第二阶段：线程生命周期与调度  [学习线程调度控制](https://gostudynow.cn/home/detail/376)

**目标：掌握线程状态、调度流程与线程常见 API 的作用**

### 1. 线程六种状态（Thread.State） [学习Java线程基础](https://gostudynow.cn/home/detail/134)
- NEW、RUNNABLE、BLOCKED、WAITING、TIMED_WAITING、TERMINATED

### 2. 线程控制方法
- `sleep()`、`yield()`、`join()`
- `wait()`、`notify()`、`notifyAll()`（配合 synchronized 使用）

### 3. 面试高频题
- sleep 和 wait 的区别？
- join 的底层原理？
- 什么情况下线程会进入 BLOCKED 状态？

---

## 第三阶段：synchronized 与锁机制 [学习synchronized锁机制](https://gostudynow.cn/home/detail/378)

**目标：掌握 Java 内置锁的底层实现与优化方式**

### 1. synchronized 详解
- 修饰实例方法、静态方法、代码块
- 锁对象、锁重入、锁升级过程

### 2. 锁的优化机制
- 偏向锁 → 轻量级锁 → 重量级锁
- 锁消除、锁粗化

### 3. 面试高频题
- synchronized 的底层实现？
- 锁升级过程是怎样的？
- 什么是可重入锁？

---

## 第四阶段：volatile 与 Java 内存模型（JMM）[学习JMM内存模型](https://gostudynow.cn/home/detail/132)

**目标：理解可见性、有序性、原子性和 Java 内存模型的设计初衷**

### 1. Java 内存模型（JMM）
- 主内存与工作内存
- happens-before 规则

### 2. volatile 关键字
- 保证可见性与禁止指令重排序
- 不保证原子性

### 3. 面试高频题
- volatile 实现原理？
- volatile 和 synchronized 区别？
- 什么是指令重排序？

---

## 第五阶段：显示锁与 Lock 框架 [学习线程显示锁Lock](https://gostudynow.cn/home/detail/379)

**目标：理解 Lock 接口与不同实现类的特性与适用场景**

### 1. ReentrantLock
- 可重入、可中断、公平/非公平
- 显式加锁解锁（try-finally）

### 2. 读写锁 ReentrantReadWriteLock
- 读写分离，提高并发性能

### 3. Condition 条件变量
- 代替传统的 Object.wait/notify

### 4. 面试高频题 [学习高频面试系列5](https://gostudynow.cn/home/detail/382)
- ReentrantLock 和 synchronized 的区别？
- Condition 和 wait/notify 有什么不同？

---

## 第六阶段：线程通信与并发工具类 [学习并发工具类](https://gostudynow.cn/home/detail/380)

**目标：掌握线程间协调与常用工具类使用方式**

### 1. 线程通信
- Object 的 wait/notify
- Condition.await/signal

### 2. 常见并发工具类
- CountDownLatch：线程计数器
- CyclicBarrier：线程屏障
- Semaphore：信号量限流
- Exchanger：线程数据交换
- Phaser：多阶段控制器

### 3. 面试题解析 [学习高频面试系列6](https://gostudynow.cn/home/detail/383)
- CountDownLatch 和 CyclicBarrier 的区别？
- Semaphore 应用场景？

---

## 第七阶段：并发容器与原子类 [学习并发容器和原子类](https://gostudynow.cn/home/detail/381)

**目标：理解线程安全集合与 CAS 原子操作机制**

### 1. 并发容器（java.util.concurrent）
- CopyOnWriteArrayList、ConcurrentHashMap
- BlockingQueue 系列（ArrayBlockingQueue、LinkedBlockingQueue）

### 2. 原子类（java.util.concurrent.atomic）
- AtomicInteger、AtomicLong、AtomicReference
- 底层实现：CAS（Compare-And-Swap）

### 3. 面试重点 [学习高频面试系列6](https://gostudynow.cn/home/detail/383)
- HashMap 和 ConcurrentHashMap 的区别？
- CAS 是什么？ABA 问题如何解决？

---

## 第八阶段：线程池与并发实战优化 [学习Java线程池](https://gostudynow.cn/home/detail/136)

**目标：理解线程池核心参数，掌握实战中的调优思路**

### 1. 线程池原理（Executor 框架） 
- Executors 工具类（不推荐直接用）
- ThreadPoolExecutor 参数详解： 
  - corePoolSize
  - maximumPoolSize
  - keepAliveTime
  - BlockingQueue
  - RejectedExecutionHandler

### 2. 线程池七大参数配置建议
- 拒绝策略：AbortPolicy、DiscardPolicy、CallerRunsPolicy、DiscardOldestPolicy
- 自定义线程工厂 ThreadFactory

### 3. 面试题重点 [学习高频面试系列6](https://gostudynow.cn/home/detail/383)
- 线程池如何防止 OOM？
- 线程池适合什么业务场景？
- 为什么不推荐使用 Executors 创建线程池？

---

## 附录：推荐资料与面试技巧

### 高频面试问题汇总
1. Java 中如何实现线程通信？[学习高频面试系列5（1-10）](https://gostudynow.cn/home/detail/382)
2. synchronized 和 Lock 有什么区别？
3. synchronized 的底层实现？volatile 和 synchronized 区别？
4. 锁升级过程是怎样的？
5. 什么是可重入锁？
6. ThreadLocal 的作用与原理？
7. 如何设计一个线程安全的计数器？
8. 线程池的核心参数你是怎么配置的？
9. 什么是死锁？怎么排查和避免？
10. HashMap 和 ConcurrentHashMap 的区别？
11. ConcurrentHashMap 为什么不需要加锁？[学习高频面试系列6（11-21）](https://gostudynow.cn/home/detail/383)
12. CAS 的底层实现与常见问题？ABA 问题如何解决？
13. Thread.join 底层如何实现等待？
14. synchronized 的底层实现？ 
15. ReentrantLock 和 synchronized 的区别？ 
16. Condition 和 wait/notify 有什么不同？ 
17. CountDownLatch 和 CyclicBarrier 的区别？ 
18. Semaphore 应用场景？
19. 线程池如何防止 OOM？ 线程池适合什么业务场景？ 
20. 为什么不推荐使用 Executors 创建线程池？ 
21. AQS的内部原理是什么？
22. 虚拟线程？[学习虚拟线程](https://gostudynow.cn/home/detail/133)

---

### 推荐学习资料
- 《Java 并发编程的艺术》
- 《深入理解 Java 虚拟机》
- Java 官方并发包文档：https://docs.oracle.com/javase/8/docs/api/java/util/concurrent/package-summary.html
- 阿里 P7 Java 面经汇总、LeetCode 并发类题目