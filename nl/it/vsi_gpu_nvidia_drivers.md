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
* [NVIDIA drivers ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://www.nvidia.com/drivers){: new_window} - consente al tuo sistema operativo per comunicare con il GPU.
* [CUDA Toolkit ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://docs.nvidia.com/cuda/){: new_window} - ambiente di sviluppo per le applicazioni accelerate GPU di prestazioni elevate.
* [cuDNN ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://developer.nvidia.com/cudnn){: new_window} - libreria (CUDA Deep Neural Network) utilizzata per le applicazioni di rete neurale.
* [NCCL ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html){: new_window} - libreria di comunicazioni cluster per le comunicazioni a più sistemi e/o a più GPU.
* **BLAS** (_Basic Linear Algebra Subprograms_) - routine che forniscono i blocchi predefiniti per l'esecuzione di operazioni algebriche lineari di base come una delle seguenti librerie:
  - [Atlas ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://math-atlas.sourceforge.net/atlas_install/){: new_window}
  - [cuBLAS ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://developer.nvidia.com/cublas){: new_window}
  - [MKL ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines){: new_window}
  - [OpenBLAS ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://www.openblas.net/){: new_window}

Se stai installando un framework machine learning, devi installare il software del framework come ad esempio una di queste piattaforme in aggiunta ai precedenti pacchetti software.
* [Caffe ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/){: new_window} (Convolutional Architecture for Fast Feature Embedding) - con licenza, framework di apprendimento approfondito open source.
* [Tensorflow (Tensorflow 1.2+) ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.tensorflow.org/install/){: new_window} - fornisce una libreria software open source per il calcolo numerico.

