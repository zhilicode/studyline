[ 2025.4.28更新 ]
## Spring 面试学习线路（八大阶段）

### 目标：全面掌握 Spring 核心模块与运行机制，强化面试中常见底层问题的理解与表达能力。

---

## 第一阶段：Spring 框架概览与核心组成

**目标：理解 Spring 的整体架构与使用场景**

### 1. Spring 是什么？ [学习Spring基础](https://gostudynow.cn/home/detail/384)
- 一个轻量级容器 + 全家桶生态框架
- 提供 IoC、AOP、事务管理、MVC、数据访问等能力

### 2. Spring 架构组成  [学习Spring架构](https://gostudynow.cn/home/detail/385)
- 核心容器（Core、Beans、Context、Expression）
- AOP
- JDBC / ORM（与 MyBatis/Hibernate 整合）
- Web（Spring MVC）
- Testing（测试支持）

### 3. 与 Spring Boot 的区别  [学习Spring和Spring Boot](https://gostudynow.cn/home/detail/386)
- Spring 更底层、配置自由度高
- Spring Boot 主要做自动配置和快速启动

---

## 第二阶段：IoC 容器与 Bean 管理

**目标：理解 Spring 核心的依赖注入与容器机制**

### 1. 什么是 IoC（控制反转）？ [学习IOC](https://gostudynow.cn/home/detail/387)
- 对象创建和依赖由 Spring 容器统一管理

### 2. Bean 的创建方式 [学习Bean创建](https://gostudynow.cn/home/detail/388)
- 注解方式：`@Component`、`@Service`、`@Repository`、`@Controller`
- XML 配置方式（早期）

### 3. 依赖注入（DI） [学习DI](https://gostudynow.cn/home/detail/389)
- `@Autowired`、`@Qualifier`
- 构造器注入 vs Setter 注入
- 面试常问：`@Autowired` 的注入原理？如何按名称注入？

---

## 第三阶段：Bean 生命周期与循环依赖

**目标：深入理解 Bean 的完整生命周期与三级缓存原理**

### 1. Bean 生命周期流程 [学习Bean生命周期](https://gostudynow.cn/home/detail/390)
- 实例化 → 属性注入 → 初始化 → 使用 → 销毁
- 生命周期扩展点：`InitializingBean`、`@PostConstruct`、`BeanPostProcessor`

### 2. 循环依赖原理 [学习循环依赖](https://gostudynow.cn/home/detail/391)
- 单例循环依赖的三级缓存解决方案：
  - 一级缓存：单例池
  - 二级缓存：提前暴露对象
  - 三级缓存：ObjectFactory 延迟初始化

### 3. 面试高频题
- Spring 如何解决循环依赖？
- BeanPostProcessor 的作用是什么？

---

## 第四阶段：AOP 原理与实现机制  [学习AOP](https://gostudynow.cn/home/detail/392)

**目标：掌握切面编程思想与 Spring AOP 的底层实现**

### 1. 什么是 AOP？
- 面向切面编程，关注横切关注点（如日志、事务）

### 2. Spring AOP 实现方式
- 基于 JDK 动态代理（接口）或 CGLIB（类）
- 常见注解：`@Aspect`、`@Before`、`@After`、`@Around`

### 3. 面试常问
- Spring AOP 的底层原理？
- JDK 动态代理和 CGLIB 区别？
- 如何实现一个简单的切面日志？

---

## 第五阶段：事务管理机制

**目标：掌握 Spring 声明式事务与传播行为**

### 1. 声明式事务注解  [学习事务注解](https://gostudynow.cn/home/detail/393)
- `@Transactional` 基本用法与位置
- 事务传播行为（Propagation）：
  - REQUIRED、REQUIRES_NEW、NESTED 等

### 2. 事务隔离级别（Isolation）[学习隔离级别](https://gostudynow.cn/home/detail/394)
- 防止脏读、幻读、不可重复读
- 配置方式：`@Transactional(isolation = Isolation.READ_COMMITTED)`

### 3. 事务失效的常见场景 [学习事务失效](https://gostudynow.cn/home/detail/395)
- 非 public 方法、被调用方法非代理调用
- 多线程场景下事务不生效

---

## 第六阶段：Spring MVC 原理与组件

**目标：掌握 Web 层 MVC 架构与请求处理流程**

### 1. 核心组件
- DispatcherServlet（前端控制器）
- HandlerMapping、HandlerAdapter
- ViewResolver、ModelAndView

### 2. 请求流程
- 请求 → DispatcherServlet → HandlerMapping → Controller → ViewResolver → 响应

### 3. 常用注解
- `@RequestMapping`、`@GetMapping`、`@PostMapping`
- `@RequestParam`、`@PathVariable`、`@ResponseBody`

### 4. 面试考点
- Spring MVC 的请求流程？
- `@Controller` 和 `@RestController` 有何区别？

---

## 第七阶段：扩展点机制与容器刷新流程

**目标：理解 Spring 的 SPI 扩展机制和上下文刷新过程**

### 1. Spring 扩展机制
- BeanFactoryPostProcessor、BeanPostProcessor
- ApplicationListener、ApplicationContextAware
- FactoryBean 接口机制

### 2. 容器启动刷新流程（重点）
- prepareRefresh() → obtainFreshBeanFactory() → invokeBeanFactoryPostProcessors() → registerBeanPostProcessors() → finishRefresh()

### 3. 面试高频
- BeanFactory 和 ApplicationContext 区别？
- Spring 容器初始化过程？

---

## 第八阶段：面试高频问题与实战技巧

**目标：提升表达能力，总结常见高频题并强化回答能力**

### 高频问题清单
1. Spring Bean 的生命周期是怎样的？
2. Spring 如何解决循环依赖？
3. 什么是 AOP？Spring 是如何实现的？
4. `@Autowired` 注入原理是什么？
5. BeanFactory 和 ApplicationContext 的区别？
6. Spring 容器初始化过程？
7. 事务失效的场景有哪些？
8. Spring 如何处理多线程下的事务？
9. Spring MVC 的请求处理流程？
10. `@Controller` 和 `@RestController` 有何区别
11. 如何自定义一个注解 + BeanPostProcessor 实现参数加解密？
12. Spring 中的事件发布机制是怎么做的？

---

## 附录：推荐资源与学习建议

### 学习资源推荐
- 《Spring 源码深度解析》
- 《Spring 实战（第 5 版）》
- Spring 官方文档：https://docs.spring.io/spring-framework/docs/current/reference/html/

### 实践建议
- 多结合实际项目做调试实验（如事务失效、循环依赖）
- 阅读源码建议从 `AbstractApplicationContext`、`BeanDefinition` 入手
- 结合 SpringBoot 一起使用可提升理解效率
