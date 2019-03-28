---

copyright:
  years: 2018
lastupdated: "2018-02-12"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 安装 GPU 驱动程序和软件包
{: #installing-gpu-drivers-and-software-packages}

您需要安装以下软件后，才能使用 GPU 系列虚拟服务器。
* [NVIDIA 驱动程序 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://www.nvidia.com/drivers){: new_window} - 支持操作系统与 GPU 通信。
* [CUDA 工具箱 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://docs.nvidia.com/cuda/){: new_window} - 用于高性能 GPU 加速应用程序的开发环境。
* [cuDNN ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://developer.nvidia.com/cudnn){: new_window} - 用于神经网络应用程序的（CUDA 深度神经网络）库。
* [NCCL ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html){: new_window} - 用于多 GPU 和/或多系统通信的集群通信库。

* **BLAS**（_基本线性代数子程序_）- 提供用于执行基本线性代数运算的构建块的例程，例如以下其中一个库：
  - [Atlas ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://math-atlas.sourceforge.net/atlas_install/){: new_window}
  - [cuBLAS ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://developer.nvidia.com/cublas){: new_window}
  - [MKL ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines){: new_window}
  - [OpenBLAS ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://www.openblas.net/){: new_window}

如果要安装机器学习框架，那么除了上面的软件包之外，还需要安装框架软件，例如以下其中一个平台。
* [Caffe ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/){: new_window} (Convolutional Architecture for Fast Feature Embedding) - 获得许可的开放式源代码深度学习框架。
* [Tensorflow (Tensorflow 1.2+) ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.tensorflow.org/install/){: new_window} - 提供用于数值计算的开放式源代码软件库。

