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

# Installation des pilotes GPU et des progiciels
Vous devez installer le logiciel suivant avant de pouvoir utiliser un serveur virtuel de la famille de GPU.
* [Pilotes NVIDIA](http://www.nvidia.com/drivers) - ils permettent au système d'exploitation de communiquer avec le GPU.
* [Kit d'outils CUDA](https://docs.nvidia.com/cuda/) - environnement de développement pour les applications haute performance accélérées par le GPU.
* [cuDNN](https://developer.nvidia.com/cudnn) - _(CUDA Deep Neural Network)_ bibliothèque utilisée pour les applications de réseaux de neurones.
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - bibliothèques de communication de cluster pour les communications à plusieurs GPU ou multi-systèmes.
* **BLAS** (_Basic Linear Algebra Subprograms_) - routines qui fournissent les blocs de construction permettant de réaliser des opérations d'algèbre linéaires de base comme l'une des bibliothèques suivantes :
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

Si vous installez une structure d'apprentissage automatique, vous devez installer un logiciel d'infrastructure comme l'une de ces plateformes en plus des progiciels précédents.
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/) (_Convolutional Architecture for Fast Feature Embedding_) - infrastructure d'apprentissage en profondeur open source sous licence.
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - offre une bibliothèque open source pour le calcul numérique.

