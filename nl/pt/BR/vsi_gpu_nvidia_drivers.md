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
* [Drivers NVIDIA ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://www.nvidia.com/drivers){: new_window} - permite que o seu sistema operacional se comunique com o GPU.
* [Kit de ferramentas CUDA ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://docs.nvidia.com/cuda/){: new_window} - ambiente de desenvolvimento para aplicativos de alto desempenho acelerados por GPU.
* [cuDNN ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://developer.nvidia.com/cudnn){: new_window} (CUDA Deep Neural Network) - biblioteca que é usada para aplicativos de rede neural.
* [NCCL ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html){: new_window} - biblioteca de comunicações de cluster para comunicações de múltiplos GPUs e/ou de multissistema.
* **BLAS** (_Basic Linear Algebra Subprograms_) - rotinas que fornecem os blocos de construção para executar operações algébricas lineares básicas, como uma das bibliotecas a seguir:
  - [Atlas ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://math-atlas.sourceforge.net/atlas_install/){: new_window}
  - [cuBLAS ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://developer.nvidia.com/cublas){: new_window}
  - [MKL ![Ícone de linkexterno](../icons/launch-glyph.svg "Ícone de link externo")](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines){: new_window}

  - [OpenBLAS ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://www.openblas.net/){: new_window}

Se você estiver instalando uma estrutura de aprendizado de máquina, será necessário instalar o software de estrutura como uma dessas plataformas, além dos pacotes de software anteriores.
* [Caffe ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/){: new_window} (Convolutional Architecture for Fast Feature Embedding) - estrutura licenciada de deep learning de software livre.
* [Tensorflow (Tensorflow 1.2+) ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.tensorflow.org/install/){: new_window} - fornece uma biblioteca de software livre para cálculo numérico.

