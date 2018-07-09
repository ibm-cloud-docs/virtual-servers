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
* [Controladores NVIDIA ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://www.nvidia.com/drivers){: new_window} - permiten a su sistema operativo comunicarse con la GPU.
* [Kit de herramientas CUDA ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://docs.nvidia.com/cuda/){: new_window} - entorno de desarrollo para aplicaciones aceleradas por GPU de alto rendimiento.
* [cuDNN ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.nvidia.com/cudnn){: new_window} - (CUDA Deep Neural Network) biblioteca que se utiliza para aplicaciones de redes neuronales.
* [NCCL ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html){: new_window} - biblioteca de comunicaciones de clúster para comunicaciones de múltiples sistemas o múltiples GPU.
* **BLAS** (_Basic Linear Algebra Subprograms_) - rutinas que proporcionan los bloques de construcción para realizar operaciones de álgebra lineal básica, como una de las siguientes bibliotecas:
  - [Atlas ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://math-atlas.sourceforge.net/atlas_install/){: new_window}
  - [cuBLAS ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.nvidia.com/cublas){: new_window}
  - [MKL ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines){: new_window}
  - [OpenBLAS ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://www.openblas.net/){: new_window}

Si está instalando en una infraestructura de aprendizaje automático, deberá instalar un software de infraestructura como una de estas plataformas, además de los paquetes de software anteriores.
* [Caffe ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/){: new_window}(Convolutional Architecture for Fast Feature Embedding) - infraestructura de deep learning de código abierto, con licencia.
* [Tensorflow (Tensorflow 1.2+) ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.tensorflow.org/install/){: new_window} - proporciona una biblioteca de software de código abierto para el cálculo numérico.

