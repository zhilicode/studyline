[ 2025.4.1更新 ]
## **第一部分：计算机科学基础**

### **1. 编程基础** 

- 选择一门编程语言（Python、Java、C++、Go 等） [学习选择一门编程语言](https://gostudynow.cn/home/detail/25)
- [Java入门](https://gostudynow.cn/home/line/detail/2)｜[Python入门](https://gostudynow.cn/home/line/detail/3)｜[C++入门](https://gostudynow.cn/home/line/detail/10)｜[Go入门](https://gostudynow.cn/home/line/detail/6)｜[JavaScript入门](https://gostudynow.cn/home/line/detail/8)｜[TypeScript入门](https://gostudynow.cn/home/line/detail/7)
- 语言基础语法 [学习编程基础](https://gostudynow.cn/home/detail/26)
- 控制结构（条件判断、循环）
- 函数与递归
- 面向对象编程（OOP）基础
- 伪代码的阅读与书写

### **2. 数据结构概述** [学习数据结构与算法入门](https://gostudynow.cn/home/detail/27)

- 什么是数据结构？
- 数据结构的分类
- 数据结构在算法中的重要性
- 时间复杂度和空间复杂度的影响

---

## **第二部分：数据结构**

### **1. 基础数据结构**

- **数组（Array）** [学习Array数组](https://gostudynow.cn/home/detail/28)
    - 一维数组、二维数组
    - 动态数组 vs 静态数组
    - 时间复杂度分析

- **链表（Linked List）** [学习链表](https://gostudynow.cn/home/detail/29)
    - 单向链表、双向链表、循环链表
    - 链表的插入、删除、查找
    - 与数组的对比

- **栈（Stack）** [学习栈](https://gostudynow.cn/home/detail/30)
    - 先进后出（LIFO）原理
    - 栈的操作（入栈、出栈、取顶）
    - 应用场景（表达式求值、括号匹配）

- **队列（Queue）** [学习队列](https://gostudynow.cn/home/detail/31)
    - 先进先出（FIFO）原理
    - 队列的操作（入队、出队）
    - **双端队列（Deque）**
    - **优先队列（Priority Queue）**

- **哈希表（Hash Table）** [开始哈希表](https://gostudynow.cn/home/detail/32)
    - 哈希函数与冲突解决（拉链法、开放地址法）
    - Python dict，Java HashMap
    - 哈希表的应用（LRU 缓存）

- **基础数据结构总结** [学习基础数据结构总结](https://gostudynow.cn/home/detail/33)
---

### **2. 树（Tree）**

- **二叉树（Binary Tree）** [学习二叉树](https://gostudynow.cn/home/detail/45)
    - 节点、根节点、叶子节点
    - 树的高度与深度

- **二叉搜索树（Binary Search Tree, BST）** [学习二叉搜索树](https://gostudynow.cn/home/detail/46)
    - 二叉搜索树的插入、删除、查找
    - 平衡性问题（最坏情况下退化为链表）

- **平衡二叉树**
    - **AVL 树**：旋转平衡，严格平衡
    - **红黑树**：自平衡，常用于集合和映射

- **B 树 & B+ 树** [学习B树](https://gostudynow.cn/home/detail/47) [学习B树代码实现](https://gostudynow.cn/home/detail/48)
    - 适用于数据库索引
    - B+ 树 vs B 树的区别

- **树的遍历** [学习二叉树&遍历](https://gostudynow.cn/home/detail/45)
    - **前序遍历（Pre-order）**
    - **中序遍历（In-order）**
    - **后序遍历（Post-order）**
    - **层序遍历（Level-order，BFS）**

---

### **3. 图（Graph）**

- **图的基本概念** [学习图](https://gostudynow.cn/home/detail/50)
    - **有向图（Directed Graph）**
    - **无向图（Undirected Graph）**
    - **带权图（Weighted Graph）**
    - **邻接矩阵 vs 邻接表**

- **图的遍历**
    - **深度优先搜索（DFS）**
    - **广度优先搜索（BFS）**

- **最短路径算法**
    - **Dijkstra 算法**（单源最短路径） [学习Dijkstra算法](https://gostudynow.cn/home/detail/51)
    - **Bellman-Ford 算法**（可处理负权边） [学习Bellman-Ford算法](https://gostudynow.cn/home/detail/52)

- **最小生成树（MST）**
    - **Prim 算法** [学习Prim算法](https://gostudynow.cn/home/detail/53)
    - **Kruskal 算法** [学习Kruskal算法](https://gostudynow.cn/home/detail/54)

---

### **4. 高级数据结构**

- **字典树（Trie）**
    - 字符串前缀存储
    - 应用：搜索建议、自动补全

- **线段树（Segment Tree）**
    - 区间查询与更新

- **树状数组（Fenwick Tree）**
    - 适用于动态数组的前缀和查询

- **并查集（Disjoint Set, Union-Find）**
    - 用于连通性判断
    - **路径压缩 + 按秩合并** 优化

- **跳表（Skip List）**
    - 平衡性动态维护
    - 适用于 Redis 中的有序集合

---

## **第三部分：算法分析与复杂度**

### **1. 算法复杂度** [学习算法复杂度](https://gostudynow.cn/home/detail/34)

- **渐进复杂度**  [学习时间复杂度](https://gostudynow.cn/home/detail/35)
    - **O(1)** - 常数时间
    - **O(log n)** - 对数时间
    - **O(n)** - 线性时间
    - **O(n log n)** - 线性对数时间
    - **O(n²)** - 平方时间
    - **O(2ⁿ)** - 指数时间
    - **O(n!)** - 阶乘时间
- **如何计算复杂度**
- **时间复杂度 vs 空间复杂度**
- **算法渐近符号** [学习渐近符号](https://gostudynow.cn/home/detail/36)

---

## **第四部分：经典算法**

### **1. 排序算法**

- **基础排序**
    - **冒泡排序（Bubble Sort）** [学习冒泡排序](https://gostudynow.cn/home/detail/37)
    - **选择排序（Selection Sort）** [学习选择排序](https://gostudynow.cn/home/detail/39)
    - **插入排序（Insertion Sort）** [学习插入排序](https://gostudynow.cn/home/detail/38)

- **高级排序**
    - **归并排序（Merge Sort）** [学习归并排序](https://gostudynow.cn/home/detail/40)
    - **快速排序（Quick Sort）** [学习快速排序](https://gostudynow.cn/home/detail/41)
    - **堆排序（Heap Sort）** [学习堆排序](https://gostudynow.cn/home/detail/42)

---

### **2. 搜索算法**

- **线性搜索（Linear Search）** [学习线性查找](https://gostudynow.cn/home/detail/43)
- **二分搜索（Binary Search）** [学习二分查找](https://gostudynow.cn/home/detail/44)
- **插值搜索（Interpolation Search）**
- **广度和深度搜索** [学习广度和深度搜索](https://gostudynow.cn/home/detail/49)

---

### **3. 递归与回溯**

- **汉诺塔问题**
- **八皇后问题**
- **全排列/子集问题**

---

### **4. 经典算法思想**

- **贪心算法（Greedy Algorithm）**
    - 活动选择问题
    - Huffman 编码
- **分治算法（Divide and Conquer）**
    - 快速排序
    - 归并排序
- **动态规划（Dynamic Programming）**
    - 斐波那契数列
    - 背包问题
    - 最长公共子序列（LCS）
- **滑动窗口（Sliding Window）**
    - 最小覆盖子串
- **双指针（Two Pointer）**
    - 快慢指针检测环
- **随机化算法（Randomized Algorithms）**
    - 快速选择（Quick Select）

---

## **第五部分：实战与练习**

### **1. 代码实践**

- **Leetcode 刷题**
- **Codeforces 竞赛**
- **AtCoder、HackerRank、Edabit**

### **2. 实战项目**

- 实现 LRU 缓存（哈希表 + 双向链表）
- 设计短网址系统（哈希表 + Base62）
- 搜索引擎的 PageRank 算法（图算法）
- 实现 Web 爬虫（BFS + 多线程）

---

## **学习路线总结**

1. **初学者**：
    - 掌握基本数据结构（数组、链表、栈、队列）
    - 了解常见排序算法（冒泡、插入、选择）
    - 熟练使用递归和回溯

2. **进阶者**：
    - 深入理解树、图、高级数据结构（Trie、并查集）
    - 熟练掌握动态规划、贪心算法
    - 练习 Leetcode 经典题目

3. **高级开发者**：
    - 研究算法竞赛（Codeforces、AtCoder）
    - 解决复杂工程问题（缓存、数据库索引优化）
    - 研究分布式系统的数据结构
