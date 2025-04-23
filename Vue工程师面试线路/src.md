[ 2025.4.22更新 ]

## Vue 工程师面试学习线路（七阶段响应式灵魂修炼流）

### 🎯 目标：系统掌握 Vue2 / Vue3 的响应式机制、组件设计、状态管理、路由控制、性能调优与项目架构，打通“写页面 → 搭系统”的全链路打怪升级路径，能过面试也能撑住项目。

---

## 第一阶段：Vue 基础语法与响应式机制

**目标：你得知道“数据变了页面就变”的魔法是怎么发生的**

### 1. 基本语法
- `v-if`, `v-for`, `v-bind`, `v-model`, `v-on`
- 计算属性 vs 方法 vs 侦听器

### 2. 响应式原理
- Vue2：Object.defineProperty
- Vue3：Proxy + Reflect + reactive + ref

### 3. 面试必问
- Vue 的响应式系统是怎么实现的？
- Vue2 和 Vue3 响应式的本质差异？

---

## 第二阶段：组件系统与通信机制

**目标：Vue 的核心是组件，别写成 DOM 操控框架**

### 1. 组件通信
- props / emit（父子）
- eventBus / mitt（非父子）
- provide / inject（祖孙）
- Vuex / Pinia（跨组件全局）

### 2. 生命周期
- Vue2：beforeCreate → created → mounted...
- Vue3：setup + onMounted、onBeforeUnmount 等

### 3. 面试经典
- 组件之间怎么通信？有哪些方式？
- Vue3 的 setup 和 Vue2 的 mounted 有什么区别？

---

## 第三阶段：路由系统与页面管理

**目标：跳转、守卫、动态路由，页面调度别乱套**

### 1. Vue Router 使用
- 静态路由、动态路由、嵌套路由
- params vs query、路由懒加载

### 2. 路由守卫
- 全局前置守卫 / 路由独享守卫 / 组件内守卫
- 登录拦截、权限控制、页面缓存（keep-alive）

### 3. 面试高频
- 怎么做权限路由控制？
- 页面跳转后缓存怎么处理？

---

## 第四阶段：状态管理方案（Vuex / Pinia）

**目标：页面多了，全局状态一定要稳得住**

### 1. Vuex（老派但经典）
- state / getters / mutations / actions / modules
- mapState、mapGetters 映射用法

### 2. Pinia（新一代更轻量）
- defineStore、storeToRefs、setup语法糖
- SSR 兼容、模块热更新支持更好

### 3. 面试必问
- Vuex 和 Pinia 有啥区别？
- 你用状态管理是怎么组织模块的？

---

## 第五阶段：异步请求与表单交互

**目标：你不写接口的代码，但你必须把接口调得顺顺的**

### 1. 请求工具
- axios 封装：请求拦截、响应拦截、token 自动刷新
- 接口错误统一处理、loading 状态管理

### 2. 表单处理
- 双向绑定、校验、表单组件封装
- Element Plus / Vant 表单控件集成

### 3. 面试高频
- 你如何封装 axios 请求层？
- 一个表单很多字段，怎么管理状态和校验？

---

## 第六阶段：性能优化与复杂交互

**目标：你不能再说“这页面卡是后端接口的问题”了。别赖锅。**

### 1. 页面性能
- 分包加载、组件懒加载、虚拟滚动、大表格渲染
- computed / watch 合理使用、v-if vs v-show

### 2. 交互体验优化
- 防抖 / 节流、loading skeleton 骨架屏、错误回退机制

### 3. 面试常问
- v-for 加 key 有啥用？为啥建议写 key？
- 大量数据渲染怎么优化？

---

## 第七阶段：项目架构与工程能力

**目标：Vue 项目你要能写，也要能拆、能测、能上线**

### 1. 项目结构设计
- 多模块拆分、按业务域组织、组件库设计
- 公共工具类封装、全局 mixin / 指令 / filter

### 2. 构建与发布
- Vue CLI / Vite：构建速度对比
- 环境配置（dev/test/prod）、动态路由权限
- CI/CD、打包分析、mock 调试、ESLint + Prettier

### 3. 面试大题
- 你项目是怎么组织结构的？
- 你做过哪些工程化优化？

---

## 附录：Vue 面试高频题 Top 10

1. Vue 的响应式原理？Vue3 用了哪些新特性？
2. setup 是什么时候执行的？里面能用 this 吗？
3. Vue 的 diff 算法是怎么工作的？
4. v-if 和 v-show 区别？什么时候选哪个？
5. ref 和 reactive 有什么区别？
6. 父子组件怎么通信？非父子组件通信方案？
7. Vuex 和 Pinia 差异？你更推荐哪个？
8. 怎么封装一个全局 loading 组件？
9. 怎么做权限控制？你是怎么实现动态路由的？
10. 你在 Vue 项目中做过哪些性能优化？

---

## 推荐学习资源

- 📘《Vue.js 设计与实现》（黄轶老师著，讲响应式原理）
- 📚 官方文档（非常清晰）：https://vuejs.org / https://v3.cn.vuejs.org/
- 🧰 工具推荐：
  - Vue Devtools
  - Vite + TypeScript
  - Element Plus / Vant / ArcoDesign

- 🧪 实战项目练手：
  - 电商后台管理系统（用户管理、权限、商品管理）
  - 移动端小程序壳（Vue + Vant）
  - Vue3 + Vite + Pinia 构建一套组件库