# 1. 安装教程以及前置知识

[📎cuda,cudnn安装配置.docx](https://www.yuque.com/attachments/yuque/0/2024/docx/35081558/1727337009343-4d6320c1-fabd-402f-909d-d398ddb34024.docx)

命令行运行 `nvcc --version`可查看版本号 `nvcc -V`

`set cuda`可以查看 cuda 设置的环境变量



【Transformer从零详细解读(可能是你见过最通俗易懂的讲解)】 https://www.bilibili.com/video/BV1Di4y1c7Zm/?share_source=copy_web&vd_source=ac70e16f2e13aa89b89a6d12ace8d801



【BERT从零详细解读，看不懂来打我】 https://www.bilibili.com/video/BV1Ey4y1874y/?share_source=copy_web&vd_source=ac70e16f2e13aa89b89a6d12ace8d801



https://zhuanlan.zhihu.com/p/703707133

# 2. 安装 transformers

 最常用的库之一，它提供了BERT模型的预训练模型和各种相关功能，可以用于文本分类、问答、文本生成等任务。  

```python
pip install transformers
```

# 3. 安装 PyTorch

- 首先在 `cmd`中执行命令：` nvidia-smi  `，查看自己的 GPU 信息，看是否支持安装 CUDA 版本的 PyTorch

我的 GPU 信息：

- **GPU 型号**: GeForce GTX 1050.
- **驱动版本**: 457.49.
- **CUDA 版本**: 11.1.

- 安装 CUDA 版本的 PyTorch（我的是  CUDA 11.1   ）

```python
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu111
```

 这个命令会安装带有 **CUDA 11.1** 支持的 PyTorch 版本，并且还会自动安装 `torchvision` 和 `torchaudio`，这些库常用于处理计算机视觉和音频任务。  

-  安装完成后，您可以通过以下命令确认 PyTorch 是否正确安装并支持 CUDA：  

```python
import torch
print(torch.cuda.is_available())  # 如果返回 True，说明 CUDA 可用
print(torch.cuda.current_device())  # 显示当前可用的 GPU
print(torch.cuda.get_device_name(0))  # 显示 GPU 名称
```

 如果返回 `True` 并且显示您的 GPU 型号（如 GTX 1050），则表示 PyTorch 成功安装并支持 CUDA。  

# 4. 安装 Tokenizers  

`tokenizers` 是 Hugging Face 提供的高效分词库，用于将输入文本转化为模型能够理解的token。

```python
pip install tokenizers
```