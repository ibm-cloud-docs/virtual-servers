---

copyright:
  years: 2018
lastupdated: "2018-02-12"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU-Treiber und -Softwarepakete installieren
{: #installing-gpu-drivers-and-software-packages}

Sie müssen die folgende Software installieren, bevor Sie einen virtuellen Server der GPU-Familie verwenden können.
* [NVIDIA-Treiber ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://www.nvidia.com/drivers){: new_window} – ermöglicht Ihrem Betriebssystem die Kommunikation mit der GPU.
* [CUDA-Toolkit ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://docs.nvidia.com/cuda/){: new_window} – Entwicklungsumgebung für leistungsfähige GPU-beschleunigte Anwendungen.
* [cuDNN ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.nvidia.com/cudnn){: new_window} – (CUDA Deep Neural Network) Bibliothek für Anwendungen für neuronale Netze.
* [NCCL ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html){: new_window} – Clusterkommunikationsbibliothek für Multi-GPU- und/oder Mehrsystemkommunikation.
* **BLAS** (_Basic Linear Algebra Subprograms_) - Routinen, die die Bausteine für die Durchführung einfacher linearer algebraischer Operationen bereitstellen, wie beispielsweise eine der folgenden Bibliotheken:
  - [Atlas ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://math-atlas.sourceforge.net/atlas_install/){: new_window}
  - [cuBLAS ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.nvidia.com/cublas){: new_window}
  - [MKL ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines){: new_window}
  - [OpenBLAS ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://www.openblas.net/){: new_window}

Wenn Sie ein Framework für maschinelles Lernen installieren, müssen Sie zusätzlich zu den oben genannten Softwarepaketen Framework-Software installieren, wie beispielsweise eine der folgenden Plattformen.
* [Caffe ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/){: new_window} (Convolutional Architecture for Fast Feature Embedding) – lizenziertes Open-Source-Deep-Learning-Framework.
* [Tensorflow (Tensorflow 1.2+) ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.tensorflow.org/install/){: new_window} – stellt eine Open-Source-Softwarebibliothek für numerische Berechnungen bereit.
