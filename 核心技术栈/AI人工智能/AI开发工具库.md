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

### 推理和部署

| 名称            | 描述                                                                                                          | 地址                                                |
| ------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| ONNX-TensorRT | 解析 ONNX 模型以便使用 TensorRT 执行。                                                                                 | [Link](https://github.com/onnx/onnx-tensorrt)     |
| Accelerate    | Accelerate 是 **Hugging Face** 开源的一个方便将 PyTorch 模型迁移到 GPU/multi-GPUs/TPU/fp16/bf16 模式下训练的小巧工具。               | [Link](https://github.com/huggingface/accelerate) |
| vLLM          | vLLM 是一个快速且易于使用的库，用于 LLM 推理和服务，和 HuggingFace 无缝集成。区别于 chatglm.cpp 和 llama.cpp，仅是在 GPU 上的模型推理加速，没有 CPU 上的加速。 | [Link](https://github.com/vllm-project/vllm)      |

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

### 知识学习

| 名称                      | 描述                                                     | 地址                                                   |
| ----------------------- | ------------------------------------------------------ | ---------------------------------------------------- |
| MiniMind                | 「大模型」3小时完全从0训练26M的小参数GPT！                              | [Link](https://github.com/jingyaogong/minimind)      |
| awesome-chatgpt-prompts | 提供高质量、即用型提示词模板，帮助用户更高效地与大语言模型（如 ChatGPT、DeepSeek 等）交互。 | [Link](https://github.com/f/awesome-chatgpt-prompts) |
| GPTs                    | GPT提示词漏洞集合                                             | [Link](https://github.com/linexjlin/GPTs)            |
| fabric                  | 通过结构化 AI 提示（Patterns）​ 解决人工智能集成难题，而非单纯追求模型能力。          | [Link](https://github.com/danielmiessler/fabric)     |
|                         |                                                        |                                                      |
|                         |                                                        |                                                      |
