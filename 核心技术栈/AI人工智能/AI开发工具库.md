## 基础框架/库

### 核心框架与模型库

| 名称           | 描述                                                                      | 地址                                                  |
| ------------ | ----------------------------------------------------------------------- | --------------------------------------------------- |
| PyTorch      | PyTorch是一个开源的Python机器学习库，基于Torch库，底层由C++实现，应用于人工智能领域，如计算机视觉和自然语言处理.     | [Link](https://github.com/pytorch/pytorch)          |
| TensorFlow   | TensorFlow是一个开源软件库，用于各种感知和语言理解任务的机器学习。                                  | [Link](https://github.com/tensorflow/tensorflow)    |
| JAX          | Google JAX，是Google开发的用于变换数值函数的Python机器学习框架。                             | [Link](https://github.com/jax-ml/jax)               |
| Transformers | 为 Jax、PyTorch 和 TensorFlow 打造的先进的自然语言处理。                                | [Link](https://github.com/huggingface/transformers) |
| Keras        | Keras 是一个用 Python 编写的高级神经网络 API，它能够以 TensorFlow, CNTK 或者 Theano 作为后端运行。 | [Link](https://github.com/keras-team/keras)         |

### 数据处理与科学计算

| 名称                         | 描述                                                                                                                                                                     | 地址                                                   |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| NumPy                      | NumPy是Python语言的一个扩展程序库。支持高阶大规模的多维数组与矩阵运算，此外也针对数组运算提供大量的数学函数函数库。                                                                                                        | [Link](https://github.com/numpy/numpy)               |
| Pandas                     | Pandas是用于数据操纵和分析的Python软件库。它建造在**NumPy**基础上，并为操纵数值表格和时间序列，提供了数据结构和运算操作。                                                                                                | [Link](https://github.com/pandas-dev/pandas)         |
| SciPy                      | SciPy是一个开源的Python算法库和数学工具包。SciPy包含的模块有最优化、线性代数、积分、插值、特殊函数、快速傅里叶变换、信号处理和图像处理、常微分方程求解和其他科学与工程中常用的计算。                                                                     | [Link](https://github.com/scipy/scipy)               |
| PyTorch DataLoader&Dataset | PyTorch provides two data primitives: `torch.utils.data.DataLoader` and `torch.utils.data.Dataset` that allow you to use pre-loaded datasets as well as your own data. |                                                      |
| Datasets                   | datasets是**HuggingFace**提供的一个用于加载、处理、查询数据集的库                                                                                                                           | [Link](https://github.com/huggingface/datasets)      |
| scikit-learn               | Scikit-learn（曾叫做scikits.learn与sklearn）是用于Python编程语言的自由并开源的机器学习库。它包含了各种分类、回归和聚类算法，包括多层感知器、支持向量机、随机森林、梯度提升、k-平均聚类和DBSCAN，它被设计协同于Python数值库**NumPy**和和科学库**SciPy**。        | [Link](https://github.com/scikit-learn/scikit-learn) |

### 模型训练与优化

| 名称                | 描述                                                                                   | 地址                                                        |
| ----------------- | ------------------------------------------------------------------------------------ | --------------------------------------------------------- |
| `Megatron-LM`     | 用于大规模训练 Transformer 模型的 GPU 优化技术。                                                    | [Link](https://github.com/NVIDIA/Megatron-LM)             |
| PyTorch Lightning | PyTorch Lightning 是一个基于 PyTorch 的高级深度学习框架，旨在简化研究流程、提高代码可维护性，并减少重复的工程代码。              | [Link](https://github.com/Lightning-AI/pytorch-lightning) |
| DeepSpeed         | DeepSpeed 是一个深度学习优化库，可以使得分布式训练和推理变得简单、高效、有效。出自**Microsoft**                          | [Link](https://github.com/microsoft/DeepSpeed)            |
| FairScale         | 用于高性能和大规模训练的 PyTorch 扩展。出自**Meta**                                                   | [Link](https://github.com/facebookresearch/fairscale)     |
| Weights & Biases  | The AI developer platform.                                                           | [Link](https://github.com/wandb/wandb)                    |
| Optuna            | Optuna 是一个特别为机器学习设计的自动超参数优化软件框架。                                                     | [Link](https://github.com/optuna/optuna)                  |
| LightGBM          | LightGBM是一款基于决策树算法的分布式梯度提升框架。                                                        | [Link](https://github.com/microsoft/LightGBM)             |
| xgboost           | XGBoost 即极端梯度提升，是可扩展的分布式梯度提升决策树(GBDT) 机器学习库。XGBoost 提供并行树提升功能，是用于回归、分类和排名问题的先进机器学习库。 | [Link](https://github.com/dmlc/xgboost)                   |
| Dask              | Dask 是一个灵活的开源库，适用于 Python 中的并行和分布式计算。                                                | [Link](https://github.com/dask/dask)                      |

### 大模型微调与适配

| 名称            | 描述                                                                                                               | 地址                                               |
| ------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| PEFT          | Parameter-Efficient Fine-Tuning，PEFT技术旨在通过最小化微调参数的数量和计算复杂度，来提高预训练模型在新任务上的性能，从而缓解大型预训练模型的训练成本。来自**Hugging Face**。 | [Link](https://github.com/huggingface/peft)      |
| TRL           | Transformer Reinforcement Learning，使用强化学习来训练transformer语言模型。来自**Hugging Face**。                                  | [Link](https://github.com/huggingface/trl)       |
| LLaMA-Factory | 微调工具:使用零代码命令行与 Web UI 轻松微调百余种大模型                                                                                 | [Link](https://github.com/hiyouga/LLaMA-Factory) |

### 模型推理

| 名称            | 描述                                                                                                          | 地址                                                |
| ------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| ONNX-TensorRT | 解析 ONNX 模型以便使用 TensorRT 执行。                                                                                 | [Link](https://github.com/onnx/onnx-tensorrt)     |
| Accelerate    | Accelerate 是 **Hugging Face** 开源的一个方便将 PyTorch 模型迁移到 GPU/multi-GPUs/TPU/fp16/bf16 模式下训练的小巧工具。               | [Link](https://github.com/huggingface/accelerate) |
| vLLM          | vLLM 是一个快速且易于使用的库，用于 LLM 推理和服务，和 HuggingFace 无缝集成。区别于 chatglm.cpp 和 llama.cpp，仅是在 GPU 上的模型推理加速，没有 CPU 上的加速。 | [Link](https://github.com/vllm-project/vllm)      |
| SGLang        | SGLang 是一个面向大型语言模型和多模态语言模型的高性能服务框架。它旨在从单个 GPU 到大型分布式集群的广泛部署中实现低延迟、高吞吐量的推理。                                  | [Link](https://github.com/sgl-project/sglang)     |

### 辅助工具库

| 名称          | 描述                                                                           | 地址                                               |
| ----------- | ---------------------------------------------------------------------------- | ------------------------------------------------ |
| Gradio      | 用于构建演示机器学习或数据科学，以及web应用程序。                                                   | [Link](https://github.com/gradio-app/gradio)     |
| Matplotlib  | Matplotlib是Python语言及其数值计算库NumPy的绘图库。                                         | [Link](https://github.com/matplotlib/matplotlib) |
| Seaborn     | Seaborn 是一个建立在 **Matplotlib** 基础之上的 Python 数据可视化库，专注于绘制各种统计图形，以便更轻松地呈现和理解数据。 | [Link](https://github.com/mwaskom/seaborn)       |
| wandb       | Weights & Biases, 为机器学习从业者打造最佳工具                                             | [Link](https://github.com/wandb)                 |
| MLflow      | Open source platform for the machine learning lifecycle。                     | [Link](https://github.com/mlflow/mlflow)         |
| ZLUDA       | CUDA on AMD GPUs                                                             | [Link](https://github.com/vosen/ZLUDA)           |
| supervision | 计算机视觉工具库                                                                     | [Link](https://github.com/roboflow/supervision)  |
| firecrawl   | 网页转LLM使用的结构化数据(**商业产品**)                                                     | [Link](https://github.com/mendableai/firecrawl)  |
|             |                                                                              |                                                  |

## 应用开发

### 智能体

| 名称              | 描述                                                                                                                                      | 地址                                                      |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| oh-my-openagent | Oh My OpenAgent（简称 OMO，也常叫 Oh My OpenCode） 是一个运行在 OpenCode（Claude Code 开源版） 之上的多智能体编排框架，把单个 AI 助手变成一支分工协作的 AI 开发团队，自动拆任务、选模型、并行执行、保证交付。 | [Link](https://github.com/code-yeongyu/oh-my-openagent) |
|                 |                                                                                                                                         |                                                         |
|                 |                                                                                                                                         |                                                         |

### AI Agent

| 名称          | 描述                             | 地址                                                |
| ----------- | ------------------------------ | ------------------------------------------------- |
| composio    | AI agent的生产工具集                 | [Link](https://github.com/ComposioHQ/composio)    |
| mem0        | The Memory layer for AI Agents | [Link](https://github.com/mem0ai/mem0)            |
| agno        | 构建multi-modal Agents的轻量化库      | [Link](https://github.com/agno-agi/agno)          |
| crewAI      | AI agent调度框架                   | [Link](https://github.com/crewAIInc/crewAI)       |
| OpenHands   | AI开发平台:软件开发Agent               | [Link](https://github.com/All-Hands-AI/OpenHands) |
| pydantic-ai | 生成级AI应用开发框架                    | [Link](https://github.com/pydantic/pydantic-ai)   |
|             |                                |                                                   |

### RAG

| 名称       | 描述                                                                | 地址                                            |
| -------- | ----------------------------------------------------------------- | --------------------------------------------- |
| RAGFlow  | RAGFlow 是一款基于深度文档理解构建的开源 RAG（Retrieval-Augmented Generation）引擎。   | [Link](https://github.com/infiniflow/ragflow) |
| graphrag | A modular graph-based Retrieval-Augmented Generation (RAG) system | [Link](https://github.com/microsoft/graphrag) |
|          |                                                                   |                                               |

### Skills

| 名称                       | 描述                                                                                                                                                                                                                                                                            | 地址                                                             |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Anthropic                | Public repository for Agent Skills                                                                                                                                                                                                                                            | [Link](https://github.com/anthropics/skills)                   |
| awesome-claude-skills    | GitHub有多个相同名字的仓库,挑选几个 :star:数比较多的:<br/>- `https://github.com/ComposioHQ/awesome-claude-skills`<br/>- `https://github.com/travisvn/awesome-claude-skills`<br/>- `https://github.com/BehiSecc/awesome-claude-skills`<br/>- `https://github.com/VoltAgent/awesome-claude-skills` | [Link](https://github.com/ComposioHQ/awesome-claude-skills)    |
| claude-scientific-skills | 这个Skills资源库比较垂直，是专门科学研究的，目前包括 138 个科学Skills，涵盖生物学、化学、医学、物理学和工程等多个领域。                                                                                                                                                                                                          | [Link](https://github.com/K-Dense-AI/claude-scientific-skills) |
| awesome-openclaw-skills  | The awesome collection of OpenClaw skills. 5,400+ skills filtered and categorized from the official OpenClaw Skills Registry.🦞                                                                                                                                               | [Link](https://github.com/VoltAgent/awesome-openclaw-skills)   |
| Product-Manager-Skills   | 产品经理Skills                                                                                                                                                                                                                                                                    | [Link](https://github.com/deanpeters/Product-Manager-Skills)   |
| baoyu-skills             | 宝玉分享的 Claude Code 技能集，提升日常工作效率。                                                                                                                                                                                                                                               | [Link](https://github.com/JimLiu/baoyu-skills)                 |
| `skills.sh`              | `https://skills.sh/trending`查看Skill的安装排名.                                                                                                                                                                                                                                     | [官网](https://skills.sh/)                                       |
| `clawhub`                | `https://clawhub.ai/`                                                                                                                                                                                                                                                         | [官网](https://clawhub.ai/)                                      |
| `skillsmp`               | `https://skillsmp.com/`                                                                                                                                                                                                                                                       | [官网](https://skillsmp.com/)                                    |
| `skiload`                | `https://skiload.com/`, 发现、筛选并安装公开的Skills.                                                                                                                                                                                                                                    | [官网](https://skiload.com/)                                     |
|                          |                                                                                                                                                                                                                                                                               |                                                                |

### MCP

| 名称          | 描述                                                                                 | 地址                                              |
| ----------- | ---------------------------------------------------------------------------------- | ----------------------------------------------- |
| blender-mcp | BlenderMCP connects Blender to Claude AI through the Model Context Protocol (MCP). | [Link](https://github.com/ahujasid/blender-mcp) |
|             |                                                                                    |                                                 |
|             |                                                                                    |                                                 |

### 网关路由

| 名称         | 描述                                                                              | 地址                                            |
| ---------- | ------------------------------------------------------------------------------- | --------------------------------------------- |
| gateway    | AI 网关:通过一个快速友好的API链接超过**多个**大型语言模型。                                             | [Link](https://github.com/Portkey-AI/gateway) |
| aisuite    | 为开发者提供统一的接口，简化多平台大型语言模型（LLM）的调用与集成。                                             | [Link](https://github.com/andrewyng/aisuite)  |
| openrouter | The unified interface for LLMs. Find the best models & prices for your prompts. | [官网](https://openrouter.ai/)                  |
| llmgateway | One API for every LLM. Any model, any provider.                                 | [官网](https://llmgateway.io/)                  |
|            |                                                                                 |                                               |
