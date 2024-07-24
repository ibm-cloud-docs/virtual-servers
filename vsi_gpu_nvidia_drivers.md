---

copyright:
  years: 2018, 2024
lastupdated: "2024-07-24"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# Installing GPU drivers and software packages
{: #installing-gpu-drivers-and-software-packages}

You need to install the following software before you can use a GPU profile with your virtual server.
* [NVIDIA drivers](https://www.nvidia.com/Download/index.aspx?lang=en-us){: external} - allows your operating system to communicate with the GPU.
* [CUDA Toolkit](https://docs.nvidia.com/cuda/){: external} - development environment for high-performance GPU-accelerated applications.
* [cuDNN](https://developer.nvidia.com/cudnn){: external} - (CUDA Deep Neural Network) library that is used for neural network applications.
* [NCCL](https://docs.nvidia.com/deeplearning/nccl/install-guide/index.html){: external} - cluster communications library for multi-GPU and or multi-system communications.
* **BLAS** (_Basic Linear Algebra Subprograms_) - routines that provide the building blocks for performing basic linear algebraic operations such as one of the following libraries:
   - [Atlas&reg;](http://math-atlas.sourceforge.net/atlas_install/){: external}
   - [cuBLAS](https://developer.nvidia.com/cublas){: external}
   - [MKL](https://www.intel.com/content/www/us/en/resources-documentation/developer.html){: external}
   - [OpenBLAS](http://www.openblas.net/){: external}

If you are installing a machine learning framework, you need to install framework software such as one of these platforms in addition to the preceding software packages.
* [Caffe](https://catalog.ngc.nvidia.com/orgs/nvidia/containers/caffe){: external} (Convolutional Architecture for Fast Feature embedding) - licensed, open source deep learning framework.
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/){: external} - provides an open source software library for numerical computation.
