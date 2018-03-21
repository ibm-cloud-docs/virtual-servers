---



copyright:
  years: 2018
lastupdated: "2018-02-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 安装 GPU 驱动程序和软件包
您需要安装以下软件后，才能使用 GPU 系列虚拟服务器。
* [NVIDIA 驱动程序](http://www.nvidia.com/drivers) - 支持操作系统与 GPU 通信。
* [CUDA 工具箱](https://docs.nvidia.com/cuda/) - 用于高性能 GPU 加速应用程序的开发环境。
* [cuDNN](https://developer.nvidia.com/cudnn)（_CUDA 深度神经网络_）- 用于神经网络应用程序的库。
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - 用于多 GPU 和/或多系统通信的集群通信库。
* **BLAS**（_基本线性代数子程序_）- 提供用于执行基本线性代数运算的构建块的例程，例如以下其中一个库：
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

如果要安装机器学习框架，那么除了上面的软件包之外，还需要安装框架软件，例如以下其中一个平台。
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/)（_快速特征嵌入的卷积体系结构_）- 获得许可的开放式源代码深度学习框架。
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - 提供用于数值计算的开放式源代码软件库。

