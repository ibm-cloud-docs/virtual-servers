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

# Instalando drivers de GPU e pacotes de software
É necessário instalar o software a seguir antes de poder usar um servidor virtual da Família GPU.
* [Drivers NVIDIA](http://www.nvidia.com/drivers) - permite que o sistema operacional se comunique com a GPU.
* [CUDA Toolkit](https://docs.nvidia.com/cuda/) - ambiente de desenvolvimento para aplicativos acelerados pela GPU de alto desempenho.
* [cuDNN](https://developer.nvidia.com/cudnn) - _(CUDA Deep Neural Network)_ biblioteca usada para aplicativos de rede neural.
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - biblioteca de comunicações de cluster para comunicações de múltiplas GPUs e/ou multissistema.
* **BLAS** (_Basic Linear Algebra Subprograms_) - rotinas que fornecem os blocos de construção para executar operações algébricas lineares básicas, como uma das bibliotecas a seguir:
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

Se você estiver instalando uma estrutura de aprendizado de máquina, será necessário instalar o software de estrutura como uma dessas plataformas, além dos pacotes de software anteriores.
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/) (_Convolutional Architecture for Fast Feature Embedding_) - estrutura de aprendizado profundo licenciada, de software livre.
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - fornece uma biblioteca de software livre para cálculo numérico.

