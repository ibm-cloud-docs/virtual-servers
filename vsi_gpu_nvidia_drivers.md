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

# Installing GPU drivers and software packages
You need to install the following software before you can use a GPU Family virtual server.
* [NVIDIA drivers](http://www.nvidia.com/drivers) - allows your operating system to communicate with the GPU.
* [CUDA Toolkit](https://docs.nvidia.com/cuda/) - development environment for high-performance GPU-accelerated applications.
* [cuDNN](https://developer.nvidia.com/cudnn) - _(CUDA Deep Neural Network)_ library that is used for neural network applications.
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - cluster communications library for multi-GPU and or multi-system communications.
* **BLAS** (_Basic Linear Algebra Subprograms_) - routines that provide the building blocks for performing basic linear algebraic operations such as one of the following libraries:
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

If you are installing a machine learning framework, you need to install framework software such as one of these platforms in addition to the preceding software packages.
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/) (_Convolutional Architecture for Fast Feature Embedding_) - licensed, open source deep learning framework.
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - provides an open source software library for numerical computation.

