[ 2025.4.25更新 ]
## Java 集合框架面试学习线路（七大阶段）

### 目标：全面掌握集合框架结构与底层原理，熟悉常用容器类特性与典型场景，强化高频面试问题的理解与表达能力。

---

## 第一阶段：集合框架总览 [学习集合体系架构](https://gostudynow.cn/home/detail/372)

**目标：建立 Java 集合体系结构的整体认知** 

### 1. 集合体系图结构
- 根接口：`Collection` 与 `Map`
- 子接口：List、Set、Queue、Deque
- 实现类：ArrayList、HashSet、LinkedList、TreeSet、PriorityQueue 等

### 2. Collection 与 Collections 的区别
- `Collection`：接口，集合体系的根
- `Collections`：工具类，提供静态方法（如排序、线程安全包装）

### 3. 面试重点
- Java 集合框架的设计思想？
- Collection 和 Map 的区别是什么？

---

## 第二阶段：List 接口体系 [学习List集合类](https://gostudynow.cn/home/detail/368)

**目标：掌握顺序存储集合的特性、底层实现与使用场景**

### 1. ArrayList
- 底层结构：动态数组，支持随机访问
- 扩容机制：1.5 倍扩容（JDK8 开始）
- 线程不安全，适合读多写少的场景

### 2. LinkedList
- 底层结构：双向链表
- 插入/删除快，但不支持高效随机访问

### 3. Vector
- 同步的动态数组，效率低，已基本淘汰

### 4. 面试高频题 [学习高频面试系列3](https://gostudynow.cn/home/detail/374)
- ArrayList 和 LinkedList 区别？
- ArrayList 的扩容机制是怎样的？
- Vector 为什么不推荐使用？

---

## 第三阶段：Set 接口体系 [学习Set集合类](https://gostudynow.cn/home/detail/368)

**目标：理解去重集合的结构、HashSet 与 TreeSet 的底层原理**

### 1. HashSet
- 底层结构：基于 HashMap 实现，存储元素为 key，value 恒为 Object
- 特性：无序、唯一、允许 null
- 元素必须重写 `hashCode()` 和 `equals()`

### 2. LinkedHashSet
- 有序的 HashSet，底层为链表 + 哈希表结构

### 3. TreeSet
- 底层：红黑树（TreeMap 实现）
- 元素必须实现 `Comparable` 接口，或传入 `Comparator`

### 4. 面试重点 [学习高频面试系列3](https://gostudynow.cn/home/detail/374)
- HashSet 如何保证元素唯一？
- HashSet 和 TreeSet 有什么区别？
- 如果不重写 `equals()`，会发生什么？

---

## 第四阶段：Map 接口体系 [学习Map集合类](https://gostudynow.cn/home/detail/368)

**目标：深入理解键值对容器的结构与实现方式**

### 1. HashMap（重点）
- 底层结构：数组 + 链表 + 红黑树（JDK8）
- 默认容量 16，加载因子 0.75
- Hash 冲突解决：拉链法 + 红黑树优化（链表转树条件）
- 非线程安全，允许 key 为 null

### 2. LinkedHashMap
- 维护插入顺序或访问顺序
- 常用于实现 LRU 缓存策略（重写 `removeEldestEntry`）

### 3. TreeMap
- 底层红黑树，自动排序（基于 key）

### 4. Hashtable（已淘汰）
- 同步哈希表，效率低，不推荐使用

### 5. ConcurrentHashMap
- JDK7：分段锁（Segment）
- JDK8：CAS + synchronized + 链表/红黑树 + Node 数组
- 线程安全，适用于高并发读写场景

### 6. 面试高频题 [学习高频面试系列3](https://gostudynow.cn/home/detail/374)
- HashMap 是如何定位位置的？
- HashMap 线程不安全表现在哪里？
- ConcurrentHashMap 如何实现线程安全？

---

## 第五阶段：Queue 与并发集合 [学习Queue和并发集合](https://gostudynow.cn/home/detail/373)

**目标：掌握常用队列结构与并发容器的使用与原理**

### 1. 队列接口体系
- Queue（单向）与 Deque（双端）
- BlockingQueue（支持阻塞）

### 2. 阻塞队列
- ArrayBlockingQueue、LinkedBlockingQueue
- DelayQueue、PriorityBlockingQueue

### 3. 并发集合
- CopyOnWriteArrayList（读多写少）
- ConcurrentSkipListMap（并发 TreeMap）
- ConcurrentLinkedQueue（无锁队列）

### 4. 面试常问 [学习高频面试系列4](https://gostudynow.cn/home/detail/375)
- CopyOnWriteArrayList 的底层原理？
- 为什么 ArrayBlockingQueue 适合限流场景？

---

## 第六阶段：集合工具类与泛型机制

**目标：掌握 Collections 与 Arrays 工具类，理解泛型在集合中的运用** 

### 1. Collections 工具类 [学习工具类](https://gostudynow.cn/home/detail/367)
- 排序：`sort()`、`reverse()`
- 线程安全包装：`synchronizedList()`、`synchronizedMap()`
- 不可变集合：`unmodifiableList()`

### 2. Arrays 工具类 [学习工具类](https://gostudynow.cn/home/detail/367)
- `Arrays.asList()` 的坑（返回固定大小 List）
- 数组排序、填充、复制

### 3. 泛型在集合中的应用 [高频面试题系列2(第6题)](https://gostudynow.cn/home/detail/371)
- 泛型类、泛型方法、通配符：`<? extends T>`、`<? super T>`

---

## 第七阶段：面试高频问题解析

**目标：强化表达能力，总结典型集合面试题及答题要点**

### 高频面试题汇总（带题眼）
1. **HashMap 是如何实现的？底层结构是怎样的？** [学习高频面试系列3(1-6)](https://gostudynow.cn/home/detail/374)
2. **HashMap 和 Hashtable 区别？为什么说 Hashtable 已过时？**
3. **ConcurrentHashMap 怎么实现线程安全？JDK7 和 JDK8 有何不同？**
4. **ArrayList 和 LinkedList 区别？哪些场景适合用 ArrayList？**
5. **Set 是如何保证唯一性的？必须重写哪些方法？**
6. **HashSet 为什么要求重写 hashCode 和 equals？**
7. **TreeMap 和 TreeSet 的底层结构是什么？** [学习高频面试系列4(7-12)](https://gostudynow.cn/home/detail/375)
8. **CopyOnWriteArrayList 的底层原理和应用场景是什么？**
9. **Java 中的阻塞队列有哪些？适用于哪些场景？**
10. **为什么不建议使用 Collections.synchronizedList() 来实现并发？**
11. **为什么 ArrayBlockingQueue 适合限流场景？**
12. **HashSet 如何保证元素唯一？ HashSet 和 TreeSet 有什么区别？**


---

## 附录：学习资源与实战建议

### 推荐资料
- 《Java 编程思想》
- 《Java 核心技术》
- 《Effective Java》
- Java 官方文档：https://docs.oracle.com/javase/8/docs/api/

### 实战建议
- 自己实现一个简化版的 HashMap / ArrayList 加深理解
- 熟练使用调试工具查看底层结构与执行过程
- 多刷面试题、结合源码看集合类细节
