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

# Instalación de controladores GPU y paquetes de software
Debe instalar el siguiente software antes de utilizar un servidor virtual de la familia GPU.
* [Controladores NVIDIA](http://www.nvidia.com/drivers) - permiten a su sistema operativo comunicarse con la GPU.
* [Kit de herramientas CUDA](https://docs.nvidia.com/cuda/) - entorno de desarrollo para aplicaciones aceleradas por GPU de alto rendimiento.
* [cuDNN](https://developer.nvidia.com/cudnn) - biblioteca _(CUDA Deep Neural Network)_ que se utiliza para aplicaciones de redes neuronales.
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - biblioteca de comunicaciones de clúster para comunicaciones de múltiples sistemas o múltiples GPU.
* **BLAS** (_Basic Linear Algebra Subprograms_) - rutinas que proporcionan los bloques de construcción para realizar operaciones de álgebra lineal básica, como una de las siguientes bibliotecas:
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

Si está instalando en una infraestructura de machine learning, deberá instalar un software de infraestructura como una de estas plataformas, además de los paquetes de software anteriores.
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/) (_Convolutional Architecture for Fast Feature Embedding_) - infraestructura de deep learning de código abierto, con licencia.
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - proporciona una biblioteca de software de código abierto para el cálculo numérico.

