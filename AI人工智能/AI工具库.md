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

| 名称         | 描述                                                                      | 地址                                                                                       |
| ---------- | ----------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `Cursor`   | 由Anysphere实验室开发的一款AI驱动的代码编辑器。                                           | [官网](https://www.cursor.com/)                                                            |
| `Roo Code` | Roo Code（前身为 Roo Cline）是一款 VS Code 插件，它通过 AI 驱动的自动化、多模型支持和实验性功能增强了编码能力。 | [VS插件地址](https://marketplace.visualstudio.com/items?itemName=RooVeterinaryInc.roo-cline) |
| Tabby      | 自托管AI代码助手                                                               | [Link](https://github.com/TabbyML/tabby)                                                 |
|            |                                                                         |                                                                                          |
|            |                                                                         |                                                                                          |
|            |                                                                         |                                                                                          |
|            |                                                                         |                                                                                          |
|            |                                                                         |                                                                                          |
|            |                                                                         |                                                                                          |

## 学习

| 名称                      | 描述                                                                                    | 地址                                                   |
| ----------------------- | ------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| minimind                | 「大模型」3小时完全从0训练26M的小参数GPT！                                                             | [Link](https://github.com/jingyaogong/minimind)      |
| awesome-chatgpt-prompts | This repo includes ChatGPT prompt curation to use ChatGPT and other LLM tools better. | [Link](https://github.com/f/awesome-chatgpt-prompts) |
|                         |                                                                                       |                                                      |

## AI产品

| 名称               | 描述                                                                                                                                                 | 地址                                                           |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| WrenAI           | Open-source GenBI AI Agent that empowers data-driven teams to chat with their data to generate Text-to-SQL, charts, spreadsheets, reports, and BI. | [Link](https://github.com/Canner/WrenAI)                     |
| ebook2audiobook  | 电子书转有声书                                                                                                                                            | [Link](https://github.com/DrewThomasson/ebook2audiobook)     |
| khoj             | AI第二大脑(**商业产品**)                                                                                                                                   | [Link](https://github.com/khoj-ai/khoj)                      |
| Perplexica       | AI 搜索引擎                                                                                                                                            | [Link](https://github.com/ItzCrazyKns/Perplexica)            |
| firecrawl        | 网页转LLM使用的结构化数据(**商业产品**)                                                                                                                           | [Link](https://github.com/mendableai/firecrawl)              |
| PDFMathTranslate | 基于 AI 完整保留排版的 PDF 文档全文双语翻译，支持 Google/DeepL/Ollama/OpenAI 等服务。                                                                                      | [Link](https://github.com/Byaidu/PDFMathTranslate)           |
| AnimatedDrawings | 卡通图片变动画                                                                                                                                            | [Link](https://github.com/facebookresearch/AnimatedDrawings) |
| MegaParse        | 文档解析器                                                                                                                                              | [Link](https://github.com/QuivrHQ/MegaParse)                 |
|                  |                                                                                                                                                    |                                                              |

## 待处理

| 名称                 | 描述                                                                            | 地址                                                     |
| ------------------ | ----------------------------------------------------------------------------- | ------------------------------------------------------ |
| GPT-SoVITS         | 强大的少样本语音转换与语音合成Web用户界面。                                                       | [Link](https://github.com/RVC-Boss/GPT-SoVITS)         |
| ComfyUI            | ComfyUI 是一个开源的用户界面（UI）工具，旨在提供一种直观且灵活的方式来创建和定制图像生成流程。                          | [Link](https://github.com/comfyanonymous/ComfyUI)      |
| pydantic-ai        | 生成级AI应用开发框架                                                                   | [Link](https://github.com/pydantic/pydantic-ai)        |
| keep               | AIOps和告警管理平台                                                                  | [Link](https://github.com/keephq/keep)                 |
| aisuite            | AI统一调用工具                                                                      | [Link](https://github.com/andrewyng/aisuite)           |
| docling            | 文档解析工具:PDF, DOCX, XLSX, HTML, images, and more                                | [Link](https://github.com/DS4SD/docling)               |
| marker             | PDF转markdown                                                                  | [Link](https://github.com/VikParuchuri/marker)         |
| Chat2DB            | AI数据库工具                                                                       | [Link](https://github.com/CodePhiliaX/Chat2DB)         |
| coai               | 一代 AIGC 一站式商业解决方案                                                             | [Link](https://github.com/coaidev/coai)                |
| OpenHands          | AI开发平台:软件开发Agent                                                              | [Link](https://github.com/All-Hands-AI/OpenHands)      |
| surya              | 文档OCR工具包                                                                      | [Link](https://github.com/VikParuchuri/surya)          |
| deepface           | 轻量级面部识别库                                                                      | [Link](https://github.com/serengil/deepface)           |
| supervision        | 计算机视觉工具库                                                                      | [Link](https://github.com/roboflow/supervision)        |
| HivisionIDPhotos   | 一个轻量级的AI证件照制作算法。                                                              | [Link](https://github.com/Zeyi-Lin/HivisionIDPhotos)   |
| roop               | AI一键换脸 (**停止维护**)                                                             | [Link](https://github.com/s0md3v/roop)                 |
| Deep-Live-Cam      | 实时视频换脸                                                                        | [Link](https://github.com/hacksider/Deep-Live-Cam)     |
| CogVideoX          | 文生视频模型. By Tsinghua University.                                               | [Link](https://github.com/THUDM/CogVideo)              |
| composio           | AI agent的生产工具集                                                                | [Link](https://github.com/ComposioHQ/composio)         |
| MinerU             | 一站式开源高质量数据提取工具，将PDF转换成Markdown和JSON格式。                                        | [Link](https://github.com/opendatalab/MinerU)          |
| mem0               | The Memory layer for AI Agents                                                | [Link](https://github.com/mem0ai/mem0)                 |
| fish-speech        | 文本转语音                                                                         | [Link](https://github.com/fishaudio/fish-speech)       |
| ChatTTS            | 一款适用于日常对话的生成式语音模型。                                                            | [Link](https://github.com/2noise/ChatTTS)              |
| gs-quant           | 量化金融的Python包                                                                  | [Link](https://github.com/goldmansachs/gs-quant)       |
| mindsdb            | 用企业数据定制 AI问答平台,                                                               | [Link](https://github.com/mindsdb/mindsdb)             |
| aider5             | 命令行里的 AI 助理                                                                   | [Link](https://github.com/paul-gauthier/aider)         |
|                    |                                                                               |                                                        |
|                    |                                                                               |                                                        |
| agno               | 构建multi-modal Agents的轻量化库                                                     | [Link](https://github.com/agno-agi/agno)               |
| Scrapegraph-ai     | ScrapeGraphAI 是一个网络爬虫 Python 库，使用大型语言模型和直接图逻辑为网站和本地文档（XML，HTML，JSON 等）创建爬取管道。 | [Link](https://github.com/VinciGit00/Scrapegraph-ai)   |
| OpenVoice          | 声音克隆工具                                                                        | [Link](https://github.com/myshell-ai/OpenVoice)        |
| LLaMA-Factory      | 微调工具:使用零代码命令行与 Web UI 轻松微调百余种大模型                                              | [Link](https://github.com/hiyouga/LLaMA-Factory)       |
| wandb              | 全称:Weights & Biases, 为机器学习从业者打造最佳工具                                           | [Link](https://github.com/wandb)                       |
| RAGFlow            | RAGFlow 是一款基于深度文档理解构建的开源 RAG（Retrieval-Augmented Generation）引擎。               | [Link](https://github.com/infiniflow/ragflow)          |
| MoneyPrinterTurbo  | 利用AI大模型，一键生成高清短视频                                                             | [Link](https://github.com/harry0703/MoneyPrinterTurbo) |
| VoiceCraft         | 零样本语音编辑和文本转语音(**停止维护**)                                                       | [Link](https://github.com/jasonppy/VoiceCraft)         |
| gpt-pilot          | AI开发者:GPT Pilot doesn't just generate code, it builds apps!                   | [Link](https://github.com/Pythagora-io/gpt-pilot)      |
| screenshot-to-code | 图片转代码                                                                         | [Link](https://github.com/abi/screenshot-to-code)      |
| ZLUDA              | CUDA on AMD GPUs                                                              | [Link](https://github.com/vosen/ZLUDA)                 |
| facefusion         | 人脸操作平台, 即AI换脸                                                                 | [Link](https://github.com/facefusion/facefusion)       |
| fabric             | AI增强人类能力                                                                      | [Link](https://github.com/danielmiessler/fabric)       |
| LLMs-from-scratch  | 从头开始构建大型语言模型                                                                  | [Link](https://github.com/rasbt/LLMs-from-scratch)     |
| gateway            | 极速 AI 网关                                                                      | [Link](https://github.com/Portkey-AI/gateway)          |
| Jan                | 本地AI助手(离线运行LLM)                                                               | [Link](https://github.com/janhq/jan)                   |
| Umi-OCR            | 开源、免费的离线OCR软件                                                                 | [Link](https://github.com/hiroi-sora/Umi-OCR)          |
| crewAI             | AI agent调度框架                                                                  | [Link](https://github.com/crewAIInc/crewAI)            |
| GPTs               | GPT提示词漏洞集合                                                                    | [Link](https://github.com/linexjlin/GPTs)              |
|                    |                                                                               |                                                        |
|                    |                                                                               |                                                        |
|                    |                                                                               |                                                        |

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
