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

# GPU-Treiber und -Softwarepakete installieren
Sie müssen die folgende Software installieren, bevor Sie einen virtuellen Server der GPU-Familie verwenden können.
* [NVIDIA-Treiber](http://www.nvidia.com/drivers) - ermöglicht Ihrem Betriebssystem die Kommunikation mit der GPU.
* [CUDA-Toolkit](https://docs.nvidia.com/cuda/) - Entwicklungsumgebung für leistungsfähige GPU-beschleunigte Anwendungen.
* [cuDNN](https://developer.nvidia.com/cudnn) - _(CUDA Deep Neural Network)_ Bibliothek für Anwendungen für neuronale Netze.
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - Clusterkommunikationsbibliothek für Multi-GPU- und/oder Mehrsystemkommunikation.
* **BLAS** (_Basic Linear Algebra Subprograms_) - Routinen, die die Bausteine für die Durchführung einfacher linearer algebraischer Operationen bereitstellen, wie beispielsweise eine der folgenden Bibliotheken:
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

Wenn Sie ein Framework für maschinelles Lernen installieren, müssen Sie zusätzlich zu den oben genannten Softwarepaketen Framework-Software installieren, wie beispielsweise eine der folgenden Plattformen.
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/) (_Convolutional Architecture for Fast Feature Embedding_) - lizenziertes Open-Source-Deep-Learning-Framework.
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - stellt eine Open-Source-Softwarebibliothek für numerische Berechnungen bereit.

