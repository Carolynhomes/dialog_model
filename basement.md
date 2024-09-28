# 基本介绍

## 1.  cuDNN

 cuDNN（CUDA Deep Neural Network library）是NVIDIA提供的用于深度神经网络加速的GPU加速库。它为深度学习框架（如TensorFlow、PyTorch等）提供了高效的实现，可以在NVIDIA的GPU上显著加速神经网络的训练和推断过程。cuDNN包含了一系列优化的卷积、池化、归一化等操作的实现，能够充分利用GPU的并行计算能力，提高深度学习模型的性能和效率。  

## 2.  CUDA  

 CUDA（Compute Unified Device Architecture）是NVIDIA推出的通用并行计算架构。它是一种基于GPU的计算平台和编程模型，允许开发者利用NVIDIA的GPU进行通用目的的并行计算。CUDA架构通过提供一套丰富的库和工具，使得开发者可以用类似于传统编程语言（如C、C++）的方式来编写并行程序，从而利用GPU的大规模并行处理能力加速各种类型的应用，包括科学计算、机器学习、深度学习等。  

cuDNN 其实就是 CUDA 的一个补丁而已，专为深度学习运算进行优化的