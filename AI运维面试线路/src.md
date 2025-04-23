[ 2025.4.22更新 ]

## MLOps 面试学习线路（七阶段系统工程流）

### 🎯 目标：掌握从模型训练到上线的完整生命周期管理技能，具备自动化部署、数据治理、可观测性与协同开发能力，为 MLOps 岗位打下钢筋混凝土级面试基础。

---

## 第一阶段：基础认知与体系概览

**目标：理解 MLOps 的架构构成与核心目标**

### 1. MLOps 是什么？
- DevOps + Machine Learning
- 解决模型上线难、监控难、复现难、协作难的综合工程体系

### 2. 典型 MLOps 生命周期
- 数据准备 → 模型训练 → 模型评估 → 模型部署 → 监控反馈 → 回流优化

### 3. 面试常问
- MLOps 与传统 DevOps 的本质区别？
- MLOps 为什么比普通工程更复杂？

---

## 第二阶段：数据工程与版本管理

**目标：掌握数据处理流程、版本控制与可追踪性方案**

### 1. 数据处理流程
- ETL / ELT 基础
- 数据清洗、特征工程、数据质量检测（Great Expectations）

### 2. 数据版本管理
- DVC（Data Version Control）
- LakeFS、DeltaLake 等数据湖系统

### 3. 面试常问
- 你如何管理每天变动的数据版本？
- 如果训练数据出错，如何定位并回滚？

---

## 第三阶段：模型训练与实验管理

**目标：规范训练流程，记录与比较实验，支持团队协同开发**

### 1. 自动化训练流程
- 使用流水线框架（如 Kubeflow、Airflow、Dagster）
- 可重现训练：Docker + Conda + Script Tracking

### 2. 实验跟踪工具
- MLflow、Weights & Biases（WandB）、Comet
- 跟踪参数、指标、代码快照与模型工件

### 3. 面试必问
- 怎么判断两个模型训练结果是否公平对比？
- 实验跑多了怎么管理与快速查找最优？

---

## 第四阶段：模型部署与服务管理

**目标：掌握模型服务部署形式与版本调度策略**

### 1. 部署方式
- Batch Inference：离线预测
- Online Inference：API 接口服务
- Streaming Inference：Kafka + 实时数据流预测

### 2. 常用部署平台
- Seldon Core、KServe、Triton Inference Server
- FastAPI + Docker + Kubernetes（手工部署组合拳）

### 3. 版本管理与回滚
- 蓝绿部署 / 灰度发布
- Canary 策略 + A/B Testing

### 4. 面试问题
- 如何确保部署模型版本的一致性？
- 模型服务怎么支持多模型共存？

---

## 第五阶段：监控与反馈机制

**目标：保障上线模型的健康状态并构建闭环优化**

### 1. 在线监控
- 模型漂移检测（Data Drift / Concept Drift）
- 性能监控指标：延迟、吞吐、预测准确度变化

### 2. 监控工具链
- Prometheus + Grafana
- Evidently AI：模型偏移自动检测工具
- Sentry / ELK：服务异常日志系统

### 3. 自动反馈机制
- Label Drift 报警 + 自动标注管道
- 在线模型评估（Shadow Model、Challenger vs Champion）

### 4. 面试高频
- 你怎么判断一个上线模型“老化”了？
- 模型准确率下降时，你的第一反应是什么？

---

## 第六阶段：CI/CD 与自动化流水线构建

**目标：构建全流程自动化模型开发与部署通道**

### 1. CI/CD for ML
- GitOps 思路（Git 作为唯一事实源）
- Jenkins / GitHub Actions / GitLab CI 配合 DVC + MLflow

### 2. TFX / Kubeflow Pipelines
- 用 DSL 描述任务依赖与运行策略
- 支持断点恢复与组件重用

### 3. 环境隔离与可复现
- Docker 镜像管理、Python 环境封装
- 环境漂移检测：环境 hash、依赖锁定

### 4. 面试问题
- 你如何保证每次部署结果都完全一致？
- 什么叫“模型不可复现”？你遇到过吗？

---

## 第七阶段：治理、安全与团队协作

**目标：提升生产级模型管理能力，保障安全性与合规性**

### 1. 模型治理
- 模型卡（Model Card）、数据来源溯源
- 模型审批与责任链机制（模型上线前 checklist）

### 2. 权限控制与安全合规
- 模型访问控制（RBAC）
- 数据脱敏、日志保留策略
- 模型审计追踪（Who/What/When/How）

### 3. 团队协作机制
- 模型交付规范（Artifact 格式统一）
- MLOps 与数据科学团队协同方式

### 4. 面试必问
- 如何对上线模型做责任归属追踪？
- 团队如何避免“我训练的模型你部署不了”这种尴尬？

---

## 附录：面试高频问题汇总

1. 模型漂移是什么？怎么检测和应对？
2. 你怎么做模型上线后的回滚方案？
3. MLOps 怎么做 CI/CD 自动化？
4. 如何保证模型部署的版本管理可控？
5. 如何对比多个实验的效果？哪些指标你最关注？
6. 在线模型服务挂了，你怎么查？
7. MLflow 和 DVC 各解决了什么问题？
8. 用 Airflow 做数据管道有什么坑？
9. 实时流预测要注意哪些性能瓶颈？
10. 你做过的最大 MLOps 项目长啥样？

---

## 推荐工具/项目/资源

- [MLflow](https://mlflow.org/)：实验+模型+部署一站式管理
- [DVC](https://dvc.org/)：数据和代码版本控制
- [KServe](https://kserve.github.io/): 模型服务平台（原 KFServing）
- [Kubeflow Pipelines](https://www.kubeflow.org/)：MLOps 流水线平台
- [Evidently AI](https://www.evidentlyai.com/)：漂移监控工具
- [FastAPI](https://fastapi.tiangolo.com/)：轻量化部署神器
- YouTube 频道：MLOps Community Talks、Made With ML
