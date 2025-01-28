## Python库

### 核心框架与模型库

| 名称           | 描述                                                                                          |     |
| ------------ | ------------------------------------------------------------------------------------------- | --- |
| PyTorch      | PyTorch是一个开源的Python机器学习库，基于Torch库，底层由C++实现，应用于人工智能领域，如计算机视觉和自然语言处理.                         | 重要  |
| TensorFlow   | TensorFlow是一个开源软件库，用于各种感知和语言理解任务的机器学习。                                                      | 重要  |
| JAX          | Google JAX，是Google开发的用于变换数值函数的Python机器学习框架。                                                 | 重要  |
| Transformers | 为 Jax、PyTorch 和 TensorFlow 打造的先进的自然语言处理。[Link](https://github.com/huggingface/transformers) | 重要  |
| Keras        | Keras 是一个用 Python 编写的高级神经网络 API，它能够以 TensorFlow, CNTK 或者 Theano 作为后端运行。                     |     |

### 数据处理与科学计算

| 名称                         | 描述                                                                                                                                                                     |     |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| NumPy                      | NumPy是Python语言的一个扩展程序库。支持高阶大规模的多维数组与矩阵运算，此外也针对数组运算提供大量的数学函数函数库。                                                                                                        | 重要  |
| Pandas                     | Pandas是用于数据操纵和分析的Python软件库。它建造在NumPy基础上，并为操纵数值表格和时间序列，提供了数据结构和运算操作。                                                                                                    | 重要  |
| PyTorch DataLoader&Dataset | PyTorch provides two data primitives: `torch.utils.data.DataLoader` and `torch.utils.data.Dataset` that allow you to use pre-loaded datasets as well as your own data. | 重要  |
| Datasets                   | 出自于**Hugging Face**。Datasets is a library for easily accessing and sharing datasets for Audio, Computer Vision, and Natural Language Processing (NLP) tasks.           |     |
| scikit-learn               | Scikit-learn（曾叫做scikits.learn与sklearn）是用于Python编程语言的自由并开源的机器学习库[2]。它包含了各种分类、回归和聚类算法，包括多层感知器、支持向量机、随机森林、梯度提升、k-平均聚类和DBSCAN，它被设计协同于Python数值库NumPy和和科学库SciPy。             | 重要  |

### 模型训练与优化

| 名称                | 描述                                                                                   |     |
| ----------------- | ------------------------------------------------------------------------------------ | --- |
| PyTorch Lightning | PyTorch Lightning 是一个开源 Python 库，它为流行的深度学习框架 PyTorch 提供了高级接口。                        | 重要  |
| DeepSpeed         | DeepSpeed 是一个深度学习优化库，可以使得分布式训练和推理变得简单、高效、有效。出自**Microsoft**                          |     |
| FairScale (Meta)  | 用于高性能和大规模训练的 PyTorch 扩展。出自**Meta**                                                   |     |
| Weights & Biases  | The AI developer platform. [link](https://github.com/wandb/wandb)                    |     |
| Optuna            | Optuna是一个开源的超参数优化(HPO)框架，用于自动执行超参数的搜索空间。                                             |     |
| LightGBM          | LightGBM是一款基于决策树算法的分布式梯度提升框架                                                         |     |
| xgboost           | XGBoost 即极端梯度提升，是可扩展的分布式梯度提升决策树(GBDT) 机器学习库。XGBoost 提供并行树提升功能，是用于回归、分类和排名问题的先进机器学习库。 |     |

### 大模型微调与适配

| 名称   | 描述                                                    |     |
| ---- | ----------------------------------------------------- | --- |
| PEFT | Parameter-Efficient Fine-Tuning，最先进的参数高效微调 (PEFT) 方法。 |     |
| TRL  | Transformer Reinforcement Learning，使用强化学习来训练变换语言模型。   |     |
|      |                                                       |     |
|      |                                                       |     |
|      |                                                       |     |

### 推理和部署

| 名称                 | 描述                                                                                     |     |
| ------------------ | -------------------------------------------------------------------------------------- | --- |
| ONNX-TensorRT      | 解析 ONNX 模型以便使用 TensorRT 执行。                                                            |     |
| Accelerate         | 来自**Hugging Face**。[Link](https://github.com/huggingface/accelerate)                   |     |
| vLLM (UC Berkeley) | Run your `*raw*` PyTorch training script on any kind of device                         |     |
| FastAPI            | FastAPI framework, high performance, easy to learn, fast to code, ready for production |     |
| Flask              | Flask是一个使用Python编写的轻量级Web应用框架。                                                                                 |     |

### 辅助工具库

| 名称         | 描述                                                                                                                 |
| ---------- | ------------------------------------------------------------------------------------------------------------------ |
| IPython    | 基于Python的交互式解释器                                                                                                    |
| Jupyter    | Interactive Computing. [Link](https://github.com/jupyter/)                                                         |
| Loguru     | Loguru is a library which aims to bring enjoyable logging in Python.                                               |
| Rich       | Rich 是一个 Python 库，可以为你在终端中提供富文本和漂亮、精美的格式。[Link]()                                                                  |
| tqdm       | A Fast, Extensible Progress Bar for Python and CLI. [Link](https://github.com/tqdm/tqdm)                           |
| MLflow     | Open source platform for the machine learning lifecycle。[Link](https://github.com/mlflow/mlflow)                   |
| Dask       | Dask 是一个灵活的开源库，适用于 Python 中的并行和分布式计算。[Link](https://github.com/dask/dask)                                          |
| Matplotlib | 画图库。Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. |
| Seaborn    | Statistical data visualization in Python。[Link](https://github.com/mwaskom/seaborn)                                |

### 其他

| 名称            | 描述                                                                                                           | 地址                                             |
| ------------- | ------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- |
| `MindSearch`  | MindSearch 是一个开源的 AI 搜索引擎框架，具有与 Perplexity.ai Pro 相同的性能。您可以轻松部署它来构建您自己的搜索引擎，可以使用闭源 LLM（如 GPT、Claude）或开源 LLM。 | [Link](https://github.com/InternLM/MindSearch) |
| `Gradio`      | 用于构建演示机器学习或数据科学，以及web应用程序。                                                                                   | [Link](https://github.com/gradio-app/gradio)   |
| `Megatron-LM` | GPU optimized techniques for training transformer models at-scale. (仅记录)                                     | [Link](https://github.com/NVIDIA/Megatron-LM)  |

## UI框架

| 名称            | 描述                                                                                                                                           | 地址                                                                                                                    |
| ------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `Lobe Chat`   | 现代化设计的开源 ChatGPT/LLMs 聊天应用与开发框架.支持语音合成、多模态、可扩展的（function call）插件系统.                                                                          | [仓库地址](https://github.com/lobehub/lobe-chat)<br/>[Ollama集成](https://lobehub.com/zh/docs/self-hosting/examples/ollama) |
| `Open WebUI`  | User-friendly AI Interface (Supports Ollama, OpenAI API, ...)                                                                                | [仓库地址](https://github.com/open-webui/open-webui)                                                                      |
| `Enchanted`   | Enchanted is **iOS and macOS** app for chatting with private self hosted language models such as Llama2, Mistral or Vicuna using **Ollama**. | [仓库地址](https://github.com/gluonfield/enchanted)                                                                       |
| `Chatbox`     | Chatbox 是一个 AI 模型桌面客户端，支持 ChatGPT、Claude、Google Gemini、Ollama 等主流模型，适用于 Windows、Mac、Linux、Web、Android 和 iOS 全平台                              | [仓库地址](https://github.com/Bin-Huang/chatbox)                                                                          |
| `Page Assist` | Use your locally running AI models to assist you in your web browsing. **Chrome插件**                                                          | [仓库地址](https://github.com/n4ze3m/page-assist)                                                                         |
| `chatgpt-web` | 仅支持`ChatGPT API`. 优秀实践: [AIchatOS](https://x.aichatos8.cn/)                                                                                  | [仓库地址](https://github.com/Chanzhaoyu/chatgpt-web)                                                                     |

## 工具产品

### Ollama

> Get up and running with Llama 3.3, DeepSeek-R1, Phi-4, Gemma 2, and other large language models. [官网](https://ollama.com/)

仓库地址: [Ollama](https://github.com/ollama/ollama)

支持丰富的集成应用, 如下图所示:

![](/Users/1993heqiang/workspace/1993heqiang/note-keeper/AI人工智能/assets/Ollama集成.png)

### Hugging Face

> [hf-mirror.com](https://hf-mirror.com/): 用于镜像 [huggingface.co](https://huggingface.co/) 域名, 致力于帮助国内AI开发者快速、稳定的下载模型、数据集

## 专业名称&简写

### SOTA

state-of-the-art model，指的是目前最好/最先进的模型。
