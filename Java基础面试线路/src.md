[ 2025.4.23更新 ]
## Java 基础面试学习线路（九大阶段）

### 目标：系统掌握 Java 核心语法、面向对象思想、集合类、异常机制、反射、泛型等基础面试高频知识点，打牢中高级开发基础。

---

## 第一阶段：Java 基本语法与数据类型

**目标：熟悉 Java 程序结构、变量定义和基本语法规则**

### 1. Java 基础语法 [学习Java基础](https://gostudynow.cn/home/detail/1)
- 标准类结构（main 方法、包导入、注释）
- 标识符、关键字、命名规范

### 2. 数据类型
- 基本类型：byte、short、int、long、float、double、char、boolean [学习数据类型](https://gostudynow.cn/home/detail/89)
- 包装类：Integer、Double、Boolean 等
- 自动装箱与拆箱

### 3. 类型转换
- 隐式转换、强制类型转换 [学习类型转换](https://gostudynow.cn/home/detail/90)
- 面试常问：`int` 和 `Integer` 的区别？为什么推荐用包装类？[学习包装类](https://gostudynow.cn/home/detail/366)

---

## 第二阶段：运算符与控制流程

**目标：掌握 Java 中各种运算符与流程控制语句**

### 1. 运算符类型 [学习运算](https://gostudynow.cn/home/detail/94)
- 算术、关系、逻辑、位运算、三目运算
- `==` 与 `.equals()` 的区别（重点）

### 2. 控制语句 [学习条件控制](https://gostudynow.cn/home/detail/91) [学习循环](https://gostudynow.cn/home/detail/92)
- if / else、switch 
- for、while、do...while
- break、continue、return 的用法与作用范围

---

## 第三阶段：面向对象编程核心

**目标：掌握 OOP 三大特性与类结构相关知识**

### 1. 类与对象 [学习类对象](https://gostudynow.cn/home/detail/96)
- 构造方法、this 关键字、方法重载 
- static 关键字作用 [学习static](https://gostudynow.cn/home/detail/99)
- final 关键字 [学习final](https://gostudynow.cn/home/detail/100)

### 2. 封装、继承、多态
- 访问修饰符：private、default、protected、public [学习访问修饰](https://gostudynow.cn/home/detail/98)
- 继承与方法重写（@Override） [学习继承](https://gostudynow.cn/home/detail/106)｜[学习封装](https://gostudynow.cn/home/detail/105)｜[学习重写/重载](https://gostudynow.cn/home/detail/109)
- 父类引用指向子类对象、多态调用规则

### 3. 面试重点 [高频面试题系列1](https://gostudynow.cn/home/detail/370)
- 成员变量与局部变量的区别？
- final、static 的使用场景？
- 面向对象的三大特性解释？

---

## 第四阶段：接口、抽象类与内部类

**目标：掌握类与接口的使用方式及差异**

### 1. 接口与抽象类  [学习抽象](https://gostudynow.cn/home/detail/107)
- 抽象类只能被继承，接口可以多实现 [学习接口](https://gostudynow.cn/home/detail/108)
- 接口默认方法（Java8）、静态方法

### 2. 内部类 [学习内部类](https://gostudynow.cn/home/detail/101)
- 成员内部类、静态内部类、匿名内部类、局部内部类

### 3. 面试题 [高频面试题系列2](https://gostudynow.cn/home/detail/371)
- 抽象类和接口的区别？
- 为什么 Java 不支持多继承？
- 接口中可以有构造方法吗？

---

## 第五阶段：常用类与工具类（String、Math、包装类）

**目标：掌握 Java 核心类库的使用方法与底层特性**

### 1. 字符串类 [学习字符串](https://gostudynow.cn/home/detail/93)
- String：不可变字符串，底层 char[]
- StringBuilder / StringBuffer 的区别（可变字符串）
- 常见面试：String 为什么不可变？intern() 方法原理？

### 2. 常用工具类 [学习工具类](https://gostudynow.cn/home/detail/367)
- Math、Random、Arrays、Objects、Collections

### 3. 包装类与自动装箱 [学习包装类](https://gostudynow.cn/home/detail/366)
- Integer.valueOf() 与 new Integer() 的区别
- Integer 缓存机制（[-128, 127]）

---

## 第六阶段：集合框架与底层原理

**目标：掌握 Java 容器体系结构与常见集合的底层实现**

### 1. 集合体系结构
- Collection 与 Map 的区别
- List、Set、Queue、Map 等接口体系 [学习List](https://gostudynow.cn/home/detail/123)｜[学习set](https://gostudynow.cn/home/detail/124)｜[学习Map](https://gostudynow.cn/home/detail/125)｜[学习queue](https://gostudynow.cn/home/detail/126)｜[学习deque](https://gostudynow.cn/home/detail/127)|[学习stack](https://gostudynow.cn/home/detail/128)

### 2. 常见集合类 [学习集合类](https://gostudynow.cn/home/detail/368)
- ArrayList vs LinkedList
- HashMap vs Hashtable vs ConcurrentHashMap
- TreeMap、LinkedHashMap
- HashSet、TreeSet、LinkedHashSet

### 3. 面试重点 [高频面试题系列1](https://gostudynow.cn/home/detail/370)｜[高频面试题系列2](https://gostudynow.cn/home/detail/371)
- HashMap 的底层实现原理？如何解决哈希冲突？
- ArrayList 扩容机制？
- Set 为什么不能存重复元素？

---

## 第七阶段：异常处理机制  [学习异常](https://gostudynow.cn/home/detail/115)

**目标：掌握 Java 异常体系与异常处理流程**

### 1. 异常类型
- 编译时异常（Checked） vs 运行时异常（Unchecked）
- 常见异常类：NullPointerException、ArrayIndexOutOfBoundsException、IOException 等

### 2. try-catch-finally
- 多 catch 分支、异常链、finally 保证执行

### 3. 面试重点 [高频面试题系列2](https://gostudynow.cn/home/detail/371)
- throw 与 throws 区别？
- 自定义异常如何写？
- finally 中 return 会覆盖 try 吗？

---

## 第八阶段：反射、泛型、枚举、注解、函数式

**目标：掌握高级语法特性与常用设计模式支持能力**

### 1. 反射 [学习反射](https://gostudynow.cn/home/detail/369)
- Class 类、Constructor、Method、Field
- 动态创建对象与调用方法

### 2. 泛型 [学习泛型](https://gostudynow.cn/home/detail/130)
- 泛型类、泛型方法、通配符 `<?>`、`<? extends T>`、`<? super T>`
- 类型擦除机制

### 3. 枚举类 [学习枚举](https://gostudynow.cn/home/detail/111)
- Enum 实现原理、本质是 class

### 4. 注解  [学习注解](https://gostudynow.cn/home/detail/117)
- 元注解（@Target、@Retention）
- 自定义注解

### 5. 函数式 
- Lambda表达式 [学习Lambda](https://gostudynow.cn/home/detail/116)
- 函数式接口 [学习函数式接口](https://gostudynow.cn/home/detail/143)
- 组合式接口 [学习组合式接口](https://gostudynow.cn/home/detail/144)
- streams [学习streams流](https://gostudynow.cn/home/detail/145)
- 高阶函数 [学习高阶函数](https://gostudynow.cn/home/detail/146)
- Optional [学习可选值](https://gostudynow.cn/home/detail/119)
---

## 第九阶段：Java 基础面试高频题整理

**目标：强化表达能力，系统梳理常问面试题及其回答思路**

### 高频面试题汇总
1. == 和 equals 的区别？[高频面试题系列1(1-6)](https://gostudynow.cn/home/detail/370)
2. 成员变量与局部变量的区别？
3. 面向对象三大特性及实际应用？
4. String 为什么不可变？intern() 方法原理？
5. ArrayList 扩容机制？
6. HashMap 的底层原理？负载因子是什么？如何解决哈希冲突？
7. final、finally、finalize 的区别？final、static 的使用场景？finally 中 return 会覆盖 try 吗？[高频面试题系列2(7-12)](https://gostudynow.cn/home/detail/371)
8. ArrayList 和 LinkedList 区别？
9. Set 为什么不能存重复元素？HashSet 为什么不能存重复值？
10. 接口和抽象类的区别？
11. throw 与 throws 区别？异常机制怎么理解？怎么自定义异常？
12. 泛型中的 `? extends T` 与 `? super T` 区别？
13. `int` 和 `Integer` 的区别？为什么推荐用包装类？[学习包装类(13-15)](https://gostudynow.cn/home/detail/366)
14. Integer.valueOf() 与 new Integer() 的区别
15. Integer 缓存机制（[-128, 127]）


---

## 附录：学习资源推荐与实践建议

### 推荐资料
- 《Java 编程思想》
- 《Effective Java》
- 《Java 核心技术 卷 I》
- Java 官方文档：https://docs.oracle.com/javase/

### 实践建议
- 每学完一个阶段结合 LeetCode、牛客题做实战练习
- 编写小项目巩固基础，如图书管理、通讯录、任务调度等
- 推荐每日一题巩固集合与字符串逻辑题
