[ 2025.4.22更新 ]
## AI 大模型工程师面试学习线路（七阶段全体系）

### 🎯 目标：系统掌握大语言模型底层原理、工程实践、模型部署与调优技能，具备胜任大模型研发岗位的技术储备与面试硬实力。

---

## 第一阶段：深度学习基础回顾

**目标：牢固掌握深度学习核心概念，为大模型理解打基础**

### 1. 神经网络基础
- 前向传播与反向传播
- 激活函数（ReLU, GELU, Swish）
- 损失函数与优化器（SGD, Adam, LAMB）

### 2. CNN / RNN 回顾（为了忘掉而学）
- CNN 原理与应用场景
- RNN/LSTM/GRU 结构与局限性

### 3. 面试考点
- 反向传播如何计算？
- 为什么使用 LayerNorm 而不是 BatchNorm？
- LSTM 和 Transformer 的核心区别是什么？

---

## 第二阶段：Transformer 及其衍生模型

**目标：深入理解 Transformer 架构及其演变路线图**

### 1. Transformer 架构全解析
- Self-Attention 与 Multi-Head Attention
- Position Encoding：正余弦 vs Learnable
- Masking 技术与 Decoder 的注意力机制

### 2. GPT / BERT / T5 对比
- GPT：自回归语言建模
- BERT：双向编码器，填空式任务
- T5：统一文本到文本架构

### 3. 面试高频
- Transformer 的计算复杂度？
- 为什么用残差连接 + LayerNorm？
- Attention 为什么比 RNN 更适合并行？

---

## 第三阶段：预训练与微调机制

**目标：理解大模型训练流程及参数高效调优技巧**

### 1. 预训练任务类型
- Causal LM（GPT系）、Masked LM（BERT系）、Span Corruption（T5系）

### 2. 微调方式
- Full fine-tuning：整个模型微调
- Parameter-efficient tuning（LoRA、Adapter、Prefix Tuning）
- Prompt Tuning 与 In-context Learning

### 3. 面试常问
- LoRA 如何降低显存消耗？
- 微调一个大模型时最关键的工程难点是什么？
- 什么情况下推荐用 Prompt Tuning？

---

## 第四阶段：模型训练工程化

**目标：掌握大模型训练的工程实践与分布式策略**

### 1. 分布式训练策略
- Data Parallel / Model Parallel / Pipeline Parallel
- ZeRO（Zero Redundancy Optimizer）技术详解

### 2. 训练框架
- PyTorch Distributed、DeepSpeed、FSDP、Megatron-LM
- 微调框架：PEFT, Hugging Face Transformers

### 3. 训练优化技巧
- Mixed Precision (fp16/bf16)
- Gradient Checkpointing
- Dynamic Loss Scaling

### 4. 面试必备
- 说说 DeepSpeed 怎么节省内存？
- 如何训练一个百亿参数模型但 GPU 只有 24GB？
- 什么是 Megatron-LM 的特点？

---

## 第五阶段：大模型部署与推理优化

**目标：掌握大模型推理与部署方案，实现低延迟、高吞吐的部署效果**

### 1. 模型量化与剪枝
- 8bit/4bit 量化（BitsAndBytes, GPTQ）
- 结构化 vs 非结构化剪枝
- Sparse Attention 机制

### 2. 推理加速工具链
- ONNX、TensorRT、vLLM、ggml、llama.cpp
- 大模型并发推理服务框架：vLLM、TGI、OpenVINO

### 3. 多设备部署策略
- GPU、TPU、CPU、边缘设备部署差异
- Flash Attention、KV cache 优化推理速度

### 4. 面试问题
- 如何部署 70B 参数模型？
- 什么是 Flash Attention？它如何加速推理？
- 模型量化会不会影响效果？

---

## 第六阶段：系统集成与产品化落地

**目标：实现从模型到应用的闭环落地，具备实战集成能力**

### 1. 多模态与长上下文模型接入
- 文本生成、图像生成、RAG（检索增强生成）
- 长上下文窗口模型（Claude、GPT-4 Turbo、Mistral）

### 2. 接口封装与服务架构
- API 网关、Token 限流、异步调用
- LLMOps：监控、日志、A/B测试、Prompt 路由

### 3. 结合知识库 / 搜索引擎
- 使用 Faiss、Weaviate 构建向量检索系统
- OpenAI Function Calling / LangChain Agent 使用方式

### 4. 面试常问
- 如何实现向量检索 + LLM 的融合问答系统？
- 一个 LLM 服务怎么防止 prompt 注入？
- 你怎么评估 LLM 接入后的产品效果？

---

## 第七阶段：大模型安全、伦理与前沿技术

**目标：了解大模型面临的现实挑战与未来发展方向**

### 1. 模型安全问题
- Prompt Injection、Jailbreak
- 输出有害内容监测（毒性检测、多轮意图识别）

### 2. 模型监管与合规
- 欧盟 AI 法规、国内管理办法（合规审查、备案）
- 可解释性与透明性需求

### 3. 大模型趋势前瞻
- MoE（专家混合）、SFT + RLHF + DPO 微调三部曲
- 多模态统一模型（GPT-4V、Gemini）
- 自动编程、Agent系统（AutoGPT、OpenDevin）

---

## 附录：面试高频问题 Top 10

1. Transformer 的 Attention 是怎么计算的？有哪些优化方法？
2. GPT 为什么是 Decoder-only？Decoder 结构和 Encoder 有什么区别？
3. LoRA 为什么高效？底层原理是什么？
4. 怎么评估一个大模型是否过拟合？
5. 大模型部署时怎么做负载均衡？
6. 微调大模型有哪些稳定性风险？如何排查？
7. 为什么 ChatGPT 能对话上下文那么强？
8. 大模型训练过程中可能遇到哪些梯度爆炸/消失问题？
9. 怎么对模型进行 online hot update？
10. 你怎么看大模型对中小企业的影响？

---

## 推荐学习资源

- 《Attention Is All You Need》原论文
- HuggingFace Transformers 官网教程：[https://huggingface.co/docs](https://huggingface.co/docs)
- 微调神器 PEFT: [https://github.com/huggingface/peft](https://github.com/huggingface/peft)
- 超神部署工具 vLLM: [https://github.com/vllm-project/vllm](https://github.com/vllm-project/vllm)
- GPT 模型全景图：paperswithcode.com、arxiv-sanity
