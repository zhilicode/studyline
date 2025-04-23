[ 2025.4.22更新 ]
## AI 算法工程师面试学习线路（七阶段智力+算力消耗流）

### 🎯 目标：全面掌握 AI 算法工程师岗位的核心技能，包括数学基础、机器学习、深度学习、模型调优、部署优化与业务落地，具备研发、复现与讲人话的能力，通过面试并留下 GPU。

---

## 第一阶段：数学基础与算法素养

**目标：会用 PyTorch 不能叫 AI 工程师，你得配得上“算法”这俩字**

### 1. 高数 & 线代
- 偏导、梯度、链式法则、泰勒展开
- 矩阵乘法、特征值、SVD、PCA

### 2. 概率统计
- 贝叶斯公式、最大似然、KL 散度
- 分布建模：正态、伯努利、指数族

### 3. 最优化理论
- 梯度下降、Adam、SGD、牛顿法
- L1/L2 正则、拉格朗日乘子法

### 4. 面试必问
- 为什么用交叉熵损失？和 MSE 有啥区别？
- Dropout 是怎么工作的？它优化了什么？

---

## 第二阶段：机器学习基础算法

**目标：不能连 KNN 和 SVM 都说不出就去搞大模型，那是纯抽象攻击。**

### 1. 常见算法
- 分类：SVM、KNN、决策树、随机森林、XGBoost
- 回归：线性回归、岭回归、Lasso、SVR
- 聚类：K-means、DBSCAN、GMM

### 2. 特征工程
- One-hot, Embedding, 标准化/归一化
- 特征选择：信息增益、方差、模型重要性

### 3. 模型评估
- ROC/AUC、混淆矩阵、Precision/Recall、F1 Score
- 交叉验证、偏差-方差平衡

### 4. 面试高频
- 什么情况下用随机森林？用过 LightGBM 吗？
- 你怎么处理不平衡样本？

---

## 第三阶段：深度学习原理与模型结构

**目标：会跑模型不够，你得懂它为什么能跑。**

### 1. 基础网络
- MLP、CNN（卷积、池化、BatchNorm）、RNN、LSTM、GRU
- 激活函数：ReLU、Sigmoid、Tanh、Swish

### 2. 训练细节
- 初始化方法（Xavier, He）
- 损失函数选择
- 过拟合处理：Dropout、EarlyStopping、数据增强

### 3. 框架实战
- PyTorch：模型定义、DataLoader、自定义训练循环
- TensorFlow：Keras 风格 API，tf.data

### 4. 面试热题
- 卷积核大小怎么选？stride 有什么影响？
- 为什么梯度消失/爆炸？怎么解决？

---

## 第四阶段：NLP / CV / 推荐等方向进阶

**目标：你不能“什么都懂一点”，你得有一个方向打穿**

### 1. NLP
- Embedding、RNN、Attention、Transformer、BERT
- 文本分类、NER、情感分析、问答系统

### 2. CV
- 图像分类、目标检测（Faster RCNN、YOLO）、图像分割
- 数据增强（MixUp、CutMix）、迁移学习、fine-tune

### 3. 推荐系统
- FM/DeepFM、Wide&Deep、DSSM、DIN、点击率预估

### 4. 面试例题
- 请讲讲 Transformer 的结构与多头注意力机制？
- YOLO 和 Faster RCNN 哪个快？为什么？

---

## 第五阶段：模型调参与实验管理

**目标：调不出准确率不叫“收敛难”，叫“不会调”。**

### 1. 超参调优
- 学习率、batch size、epoch、weight decay
- 网格搜索、随机搜索、Bayesian Optimization

### 2. 训练技巧
- 学习率预热 / 衰减（WarmUp, Cosine Annealing）
- Gradient Clipping、MixPrecision

### 3. 实验管理
- wandb / tensorboard / mlflow
- 多组实验日志、模型 checkpoint 策略

### 4. 面试加分
- 你训练过哪些大模型？用什么工具记录实验？
- 你调过最奇怪的参数是哪个？结果如何？

---

## 第六阶段：部署优化与工程能力

**目标：AI 不上线，等于白跑。你得会部署，否则模型只是论文附件。**

### 1. 推理优化
- ONNX、TensorRT、TorchScript
- Batch 推理 vs 单样本请求、量化/剪枝/蒸馏

### 2. 模型部署
- Flask + Gunicorn + Nginx 模型服务
- FastAPI、GRPC、TorchServe、Triton

### 3. 工程能力
- Docker 化部署、CI/CD、GPU 资源管理
- 模型版本管理、服务监控

### 4. 面试重点
- 模型太大推不动你怎么办？
- 怎么做多模型版本管理？

---

## 第七阶段：业务落地 + 系统设计 + 面试输出

**目标：你得能讲业务价值、讲模型结构、还能画系统图打全场**

### 1. 项目讲解结构
- 业务背景 → 技术选型 → 模型结构 → 训练优化 → 部署上线 → 效果指标

### 2. 系统设计题
- 实时推荐系统架构
- 智能客服问答系统架构
- 图像识别 + OCR 自动审批流程系统

### 3. 面试实战题
- 怎么设计一个“AI 智能打标签”系统？
- 模型训练耗时 12 小时，有没有优化手段？

---

## 附录：AI 算法工程师面试高频题 TOP 10

1. 为什么神经网络可以拟合任意函数？
2. L1 和 L2 正则分别抑制什么问题？
3. Transformer 中的 Position Encoding 是干嘛的？
4. Batch Normalization 有什么作用？
5. CNN 是怎么处理图像平移不变性的？
6. Attention 是怎么提升模型表达能力的？
7. 你在什么场景下使用了迁移学习？
8. 如何处理样本标签错误？对模型影响大吗？
9. 如何优化模型推理速度？你压缩过模型吗？
10. AI 模型上线后怎么做监控和反馈？

---

## 推荐资料 & 工具

- 📘 经典书籍：
  - 《深度学习》（Goodfellow）
  - 《动手学深度学习》
  - 《机器学习实战》

- 🛠️ 工具集：
  - PyTorch / TensorFlow / HuggingFace / Scikit-learn
  - wandb / mlflow / tensorboard
  - Docker / Triton / ONNX / TensorRT

- 🎮 项目练习：
  - 图像分类 + 增强 + 推理部署全流程
  - 情感分析 → fine-tune BERT → API部署
  - 推荐系统 CTR 预测 + AUC 对比 + 多模型融合