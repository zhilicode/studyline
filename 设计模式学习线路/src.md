[ 2025.4.1更新 ]
## **第一部分：设计模式基础**
### **1. 设计模式概述**

- 什么是设计模式？
- 设计模式的分类（创建型、结构型、行为型）
- 设计模式的六大原则：
    - **单一职责原则（SRP）**
    - **开放封闭原则（OCP）**
    - **里氏替换原则（LSP）**
    - **依赖倒置原则（DIP）**
    - **接口隔离原则（ISP）**
    - **合成复用原则（CRP）**

### **2. 设计模式的应用场景**

- 什么时候应该使用设计模式？
- 设计模式如何提高代码的可维护性、可复用性和扩展性？

---

## **第二部分：创建型模式（Creational Patterns）**

创建型模式用于对象的创建，确保对象的创建过程更加灵活、可复用。

### **1. 单例模式（Singleton Pattern）** [学习单例模式](https://gostudynow.cn/home/detail/2)

- **作用**：保证一个类仅有一个实例，并提供一个全局访问点
- **实现方式**：
    - 饿汉式单例
    - 懒汉式单例
    - 双重检查锁单例
    - 静态内部类单例
    - 枚举单例
- **应用场景**：
    - 线程池
    - 数据库连接池
    - 配置管理类

### **2. 工厂方法模式（Factory Method Pattern）** [学习简单工厂](https://gostudynow.cn/home/detail/3)

- **作用**：定义一个创建对象的接口，让子类决定实例化哪一个类
- **实现方式**：
    - 普通工厂模式
    - 静态工厂模式
- **应用场景**：
    - 日志系统
    - 连接数据库驱动

### **3. 抽象工厂模式（Abstract Factory Pattern）** [学习抽象工厂](https://gostudynow.cn/home/detail/4)

- **作用**：提供一个创建一系列相关对象的接口，而无需指定具体的类
- **应用场景**：
    - GUI 库（不同操作系统的 UI 组件）
    - 数据库访问（支持多种数据库）

### **4. 建造者模式（Builder Pattern）** [学习建造者模式](https://gostudynow.cn/home/detail/5)

- **作用**：将一个复杂对象的创建过程与其表示分离
- **应用场景**：
    - 构建 SQL 语句
    - 创建复杂的 Java 对象（如 StringBuilder）

### **5. 原型模式（Prototype Pattern）** [学习原型模式](https://gostudynow.cn/home/detail/6)

- **作用**：通过复制已有实例创建新的对象
- **应用场景**：
    - 需要避免创建大量相似对象
    - 需要高效地创建对象

---

## **第三部分：结构型模式（Structural Patterns）**

结构型模式关注类和对象的组合，以形成更大的结构。

### **1. 适配器模式（Adapter Pattern）** [学习适配器模式](https://gostudynow.cn/home/detail/7)

- **作用**：将一个类的接口转换成用户期望的另一个接口
- **应用场景**：
    - Java I/O 适配器
    - JDBC 驱动适配
 
### **2. 桥接模式（Bridge Pattern）** [学习桥接模式](https://gostudynow.cn/home/detail/8)

- **作用**：将抽象部分与实现部分分离，使二者可以独立变化
- **应用场景**：
    - 数据库驱动与数据库类型的解耦

### **3. 组合模式（Composite Pattern）** [学习组合模式](https://gostudynow.cn/home/detail/10)

- **作用**：将对象组合成树形结构，以表示“部分-整体”层次结构
- **应用场景**：
    - 组织架构树
    - 文件系统

### **4. 装饰器模式（Decorator Pattern）** [学习装饰模式](https://gostudynow.cn/home/detail/9)

- **作用**：动态地给对象增加新的功能
- **应用场景**：
    - Java I/O 流
    - 过滤器设计

### **5. 外观模式（Facade Pattern）** [学习外观模式](https://gostudynow.cn/home/detail/11)

- **作用**：为子系统提供一个统一的接口
- **应用场景**：
    - Spring MVC Controller
    - 统一异常处理

### **6. 享元模式（Flyweight Pattern）** [学习享元模式](https://gostudynow.cn/home/detail/12)

- **作用**：减少对象的创建，提高性能
- **应用场景**：
    - 线程池
    - 数据库连接池

### **7. 代理模式（Proxy Pattern）** [学习代理模式](https://gostudynow.cn/home/detail/13)

- **作用**：为对象提供一个代理，以控制对该对象的访问
- **应用场景**：
    - 动态代理（Spring AOP）
    - 静态代理（RPC 远程调用）

---

## **第四部分：行为型模式（Behavioral Patterns）**

行为型模式关注对象之间的通信和交互方式。

### **1. 责任链模式（Chain of Responsibility Pattern）** [学习责任链模式](https://gostudynow.cn/home/detail/23)

- **作用**：将请求沿着处理者链传递，直到某个处理者能够处理
- **应用场景**：
    - Java 过滤器链
    - 日志处理系统

### **2. 命令模式（Command Pattern）** [学习命令模式](https://gostudynow.cn/home/detail/15)

- **作用**：将请求封装为对象，从而实现请求的参数化
- **应用场景**：
    - 事务管理
    - 按钮点击事件

### **3. 解释器模式（Interpreter Pattern）** [学习解释器模式](https://gostudynow.cn/home/detail/20)

- **作用**：定义一种语言的语法并解析表达式
- **应用场景**：
    - SQL 解析器
    - 正则表达式解析

### **4. 迭代器模式（Iterator Pattern）** [学习迭代器模式](https://gostudynow.cn/home/detail/16)

- **作用**：提供一种顺序访问集合对象的方法，而不暴露内部结构
- **应用场景**：
    - Java Iterator
    - 数据库游标

### **5. 中介者模式（Mediator Pattern）** [学习中介者模式](https://gostudynow.cn/home/detail/18)

- **作用**：用一个中介者对象封装一系列对象的交互
- **应用场景**：
    - MVC 控制器
    - 线程调度

### **6. 备忘录模式（Memento Pattern）** [学习备忘录模式](https://gostudynow.cn/home/detail/19)

- **作用**：保存对象的状态，以便恢复
- **应用场景**：
    - 历史记录功能
    - 游戏存档

### **7. 观察者模式（Observer Pattern）** [学习观察者模式](https://gostudynow.cn/home/detail/17)

- **作用**：定义对象间的一对多依赖关系
- **应用场景**：
    - 事件监听机制（GUI 按钮）
    - 发布订阅系统

### **8. 状态模式（State Pattern）** [学习状态模式](https://gostudynow.cn/home/detail/21)

- **作用**：允许对象在状态改变时改变行为
- **应用场景**：
    - 流程控制
    - 订单状态管理

### **9. 策略模式（Strategy Pattern）** [学习策略模式](https://gostudynow.cn/home/detail/22)

- **作用**：定义一组算法，将每个算法封装起来，使它们可以互换
- **应用场景**：
    - 支付方式（支付宝、微信）
    - 负载均衡策略

### **10. 模板方法模式（Template Method Pattern）** [学习模版方法](https://gostudynow.cn/home/detail/14)

- **作用**：定义算法框架，并让子类实现某些步骤
- **应用场景**：
    - Spring JdbcTemplate
    - 代码生成器

### **11. 访问者模式（Visitor Pattern）** [学习访问者模式](https://gostudynow.cn/home/detail/24)

- **作用**：分离算法与对象结构
- **应用场景**：
    - 编译器解析
    - XML/JSON 解析

---

## **第五部分：设计模式学习路线**

1. **初学者**：学习单例、工厂、策略等基础模式。
2. **进阶者**：掌握适配器、装饰器、代理等结构型模式，提升代码复用性。
3. **高级开发者**：深入研究责任链、观察者、状态、命令模式，优化系统设计。
4. **架构师**：综合运用多种模式，优化企业级应用架构，提高可扩展性与维护性。
