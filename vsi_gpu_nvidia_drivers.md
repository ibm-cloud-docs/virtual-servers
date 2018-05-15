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
* [NVIDIA drivers ![External link icon](../icons/launch-glyph.svg "External link icon")](http://www.nvidia.com/drivers){: new_window} - allows your operating system to communicate with the GPU.
* [CUDA Toolkit ![External link icon](../icons/launch-glyph.svg "External link icon")](https://docs.nvidia.com/cuda/){: new_window} - development environment for high-performance GPU-accelerated applications.
* [cuDNN ![External link icon](../icons/launch-glyph.svg "External link icon")](https://developer.nvidia.com/cudnn){: new_window} - (CUDA Deep Neural Network) library that is used for neural network applications.
* [NCCL ![External link icon](../icons/launch-glyph.svg "External link icon")](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html){: new_window} - cluster communications library for multi-GPU and or multi-system communications.
* **BLAS** (_Basic Linear Algebra Subprograms_) - routines that provide the building blocks for performing basic linear algebraic operations such as one of the following libraries:
  - [Atlas ![External link icon](../icons/launch-glyph.svg "External link icon")](http://math-atlas.sourceforge.net/atlas_install/){: new_window}
  - [cuBLAS ![External link icon](../icons/launch-glyph.svg "External link icon")](https://developer.nvidia.com/cublas){: new_window}
  - [MKL ![External link icon](../icons/launch-glyph.svg "External link icon")](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines){: new_window}
  - [OpenBLAS ![External link icon](../icons/launch-glyph.svg "External link icon")](http://www.openblas.net/){: new_window}

If you are installing a machine learning framework, you need to install framework software such as one of these platforms in addition to the preceding software packages.
* [Caffe ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/){: new_window} (Convolutional Architecture for Fast Feature Embedding) - licensed, open source deep learning framework.
* [Tensorflow (Tensorflow 1.2+) ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.tensorflow.org/install/){: new_window} - provides an open source software library for numerical computation.

