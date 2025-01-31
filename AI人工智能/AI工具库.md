## Python库

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

### 大模型微调与适配

| 名称   | 描述                                                                                                               | 地址                                          |
| ---- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| PEFT | Parameter-Efficient Fine-Tuning，PEFT技术旨在通过最小化微调参数的数量和计算复杂度，来提高预训练模型在新任务上的性能，从而缓解大型预训练模型的训练成本。来自**Hugging Face**。 | [Link](https://github.com/huggingface/peft) |
| TRL  | Transformer Reinforcement Learning，使用强化学习来训练transformer语言模型。来自**Hugging Face**。                                  | [Link](https://github.com/huggingface/trl)  |

### 推理和部署

| 名称            | 描述                                                                                                          | 地址                                                |
| ------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| ONNX-TensorRT | 解析 ONNX 模型以便使用 TensorRT 执行。                                                                                 | [Link](https://github.com/onnx/onnx-tensorrt)     |
| Accelerate    | Accelerate 是 **Hugging Face** 开源的一个方便将 PyTorch 模型迁移到 GPU/multi-GPUs/TPU/fp16/bf16 模式下训练的小巧工具。               | [Link](https://github.com/huggingface/accelerate) |
| vLLM          | vLLM 是一个快速且易于使用的库，用于 LLM 推理和服务，和 HuggingFace 无缝集成。区别于 chatglm.cpp 和 llama.cpp，仅是在 GPU 上的模型推理加速，没有 CPU 上的加速。 | [Link](https://github.com/vllm-project/vllm)      |

### 辅助工具库

| 名称         | 描述                                                                           | 地址                                               |
| ---------- | ---------------------------------------------------------------------------- | ------------------------------------------------ |
| MLflow     | Open source platform for the machine learning lifecycle。                     | [Link](https://github.com/mlflow/mlflow)         |
| Dask       | Dask 是一个灵活的开源库，适用于 Python 中的并行和分布式计算。                                        | [Link](https://github.com/dask/dask)             |
| Matplotlib | Matplotlib是Python语言及其数值计算库NumPy的绘图库。                                         | [Link](https://github.com/matplotlib/matplotlib) |
| Seaborn    | Seaborn 是一个建立在 **Matplotlib** 基础之上的 Python 数据可视化库，专注于绘制各种统计图形，以便更轻松地呈现和理解数据。 | [Link](https://github.com/mwaskom/seaborn)       |
| `Gradio`   | 用于构建演示机器学习或数据科学，以及web应用程序。                                                   | [Link](https://github.com/gradio-app/gradio)     |

### 其他

| 名称           | 描述                                                                                                           | 地址                                             |
| ------------ | ------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- |
| `MindSearch` | MindSearch 是一个开源的 AI 搜索引擎框架，具有与 Perplexity.ai Pro 相同的性能。您可以轻松部署它来构建您自己的搜索引擎，可以使用闭源 LLM（如 GPT、Claude）或开源 LLM。 | [Link](https://github.com/InternLM/MindSearch) |

## UI框架（Web & Desktop）

| 名称              | 描述                                                                                                                                           | 地址                                                                                                                    |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `Lobe Chat`     | 现代化设计的开源 ChatGPT/LLMs 聊天应用与开发框架.支持语音合成、多模态、可扩展的（function call）插件系统.                                                                          | [仓库地址](https://github.com/lobehub/lobe-chat)<br/>[Ollama集成](https://lobehub.com/zh/docs/self-hosting/examples/ollama) |
| `Open WebUI`    | User-friendly AI Interface (Supports Ollama, OpenAI API, ...)                                                                                | [仓库地址](https://github.com/open-webui/open-webui)                                                                      |
| `Enchanted`     | Enchanted is **iOS and macOS** app for chatting with private self hosted language models such as Llama2, Mistral or Vicuna using **Ollama**. | [仓库地址](https://github.com/gluonfield/enchanted)                                                                       |
| `Chatbox`       | Chatbox 是一个 AI 模型桌面客户端，支持 ChatGPT、Claude、Google Gemini、Ollama 等主流模型，适用于 Windows、Mac、Linux、Web、Android 和 iOS 全平台                              | [仓库地址](https://github.com/Bin-Huang/chatbox)                                                                          |
| `Page Assist`   | Use your locally running AI models to assist you in your web browsing. **Chrome插件**                                                          | [仓库地址](https://github.com/n4ze3m/page-assist)                                                                         |
| `chatgpt-web`   | 仅支持`ChatGPT API`. 优秀实践: [AIchatOS](https://x.aichatos8.cn/)                                                                                  | [仓库地址](https://github.com/Chanzhaoyu/chatgpt-web)                                                                     |
| `cherry-studio` | Cherry Studio 是一款支持多个大语言模型（LLM）服务商的桌面客户端，兼容 Windows、Mac 和 Linux 系统。                                                                          | [仓库地址](https://github.com/CherryHQ/cherry-studio)                                                                     |

## 编码工具

| 名称         | 描述                                                                                                                                                              |     |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| `Cursor`   | 由Anysphere实验室开发的一款AI驱动的代码编辑器。[官网](https://www.cursor.com/)                                                                                                      |     |
| `Roo Code` | Roo Code（前身为 Roo Cline）是一款 VS Code 插件，它通过 AI 驱动的自动化、多模型支持和实验性功能增强了编码能力。[VS插件地址](https://marketplace.visualstudio.com/items?itemName=RooVeterinaryInc.roo-cline) |     |
|            |                                                                                                                                                                 |     |

## 工具产品

### Ollama

> Get up and running with Llama 3.3, DeepSeek-R1, Phi-4, Gemma 2, and other large language models. [官网](https://ollama.com/)

仓库地址: [Ollama](https://github.com/ollama/ollama)

支持丰富的集成应用, 如下图所示:

![](/Users/1993heqiang/workspace/1993heqiang/note-keeper/AI人工智能/assets/Ollama集成.png)

### Hugging Face

> [hf-mirror.com](https://hf-mirror.com/): 用于镜像 [huggingface.co](https://huggingface.co/) 域名, 致力于帮助国内AI开发者快速、稳定的下载模型、数据集

## AI公司

### Groq

Groq 成立于2016年，是一家 AI 芯片公司由前谷歌员工 Jonathan Ross 创立。其推出的LPU（Language Processing Unit）推理引擎是一种新型的端到端处理单元系统，可为具有顺序组件的计算密集型应用程序提供最快的推理，宣称做到了“地表最强推理”。[官网](https://groq.com/)

## 专业名称&简写

### SOTA

state-of-the-art model，指的是目前最好/最先进的模型。

### TTS

**文本转语音**（Text-to-Speech，TTS）   

## 书籍&资源

### 《AI系统：原理与架构》

图书：[京东图书](https://item.jd.com/10116328478876.html)

Github: [AISystem](https://github.com/chenzomi12/AISystem)、[AIFoundation](https://github.com/chenzomi12/AIFoundation/)

电子图书：[AISys](https://chenzomi12.github.io/)

### 《大模型应用开发：RAG入门与实战》

图书：[京东图书](https://item.jd.com/14291507.html)
