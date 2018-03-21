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

# 安裝 GPU 驅動程式及軟體套件
您需要先安裝下列軟體，才能使用「GPU 系列」虛擬伺服器。
* [NVIDIA 驅動程式](http://www.nvidia.com/drivers) - 容許作業系統與 GPU 通訊。
* [CUDA 工具箱](https://docs.nvidia.com/cuda/) - 高效能 GPU 加速應用程式的開發環境。
* [cuDNN](https://developer.nvidia.com/cudnn) - 用於類神經網路應用程式的_（CUDA 深度類神經網路）_程式庫。
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - 多 GPU 及（或）多重系統通訊的叢集通訊程式庫。
* **BLAS**（_基本線性代數子程式_）- 常式，提供可執行基本線性代數作業（例如下列其中一個程式庫）的構成要素：
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

如果您要安裝 Machine Learning 架構，則需要安裝架構軟體，例如，先前軟體套件以外的其中一個平台。
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/) (_Convolutional Architecture for Fast Feature Embedding_) - 授權、開放程式碼深度學習架構。
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - 提供進行數值計算的開放程式碼軟體程式庫。

