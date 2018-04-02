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

# Installazione dei driver GPU dai pacchetti software
Devi installare il seguente software prima di poter utilizzare un server virtuale della famiglia GPU.
* [NVIDIA drivers](http://www.nvidia.com/drivers) - consente al tuo sistema operativo per comunicare con il GPU.
* [CUDA Toolkit](https://docs.nvidia.com/cuda/) - ambiente di sviluppo per le applicazioni accelerate GPU di prestazioni elevate.
* [cuDNN](https://developer.nvidia.com/cudnn) - Libreria _(CUDA Deep Neural Network)_ utilizzata per le applicazioni di rete neurale.
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - libreria di comunicazioni cluster per le comunicazioni a più sistemi e/o a più GPU.
* **BLAS** (_Basic Linear Algebra Subprograms_) - routine che forniscono i blocchi predefiniti per l'esecuzione di operazioni algebriche lineari di base come una delle seguenti librerie:
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

Se stai installando un framework machine learning, devi installare il software del framework come ad esempio una di queste piattaforme in aggiunta ai precedenti pacchetti software.
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/) (_Convolutional Architecture for Fast Feature Embedding_) - con licenza, framework di apprendimento approfondito open source.
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - fornisce una libreria software open source per il calcolo numerico.

