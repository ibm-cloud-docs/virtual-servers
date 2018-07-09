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
Vous devez installer les logiciels suivants avant de pouvoir utiliser un serveur virtuel de la famille de GPU.
* [Pilotes NVIDIA ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://www.nvidia.com/drivers){: new_window} - permettent à votre système d'exploitation de communiquer avec le GPU.
* [Kit d'outils CUDA ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://docs.nvidia.com/cuda/){: new_window} - environnement de développement pour les applications haute performance accélérées par le GPU.
* [cuDNN ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://developer.nvidia.com/cudnn){: new_window} - (CUDA Deep Neural Network) bibliothèque utilisée pour les applications de réseaux de neurones.
* [NCCL ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html){: new_window} - bibliothèques de communication de cluster pour les communications à plusieurs GPU ou multi-systèmes.
* **BLAS** (_Basic Linear Algebra Subprograms_) - routines qui fournissent les blocs de construction permettant de réaliser des opérations d'algèbre linéaires de base comme l'une des bibliothèques suivantes :
  - [Atlas ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://math-atlas.sourceforge.net/atlas_install/){: new_window}
  - [cuBLAS ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://developer.nvidia.com/cublas){: new_window}
  - [MKL ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines){: new_window}
  - [OpenBLAS ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://www.openblas.net/){: new_window}

Si vous installez une structure d'apprentissage automatique, vous devez installer un logiciel d'infrastructure comme l'une de ces plateformes en plus des progiciels précédents.
* [Caffe ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/){: new_window} (Convolutional Architecture for Fast Feature Embedding) - infrastructure d'apprentissage en profondeur open source sous licence.
* [Tensorflow (Tensorflow 1.2+) ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.tensorflow.org/install/){: new_window} - offre une bibliothèque open source pour le calcul numérique.

