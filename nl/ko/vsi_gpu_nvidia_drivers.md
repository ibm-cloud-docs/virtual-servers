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

# GPU 드라이버 및 소프트웨어 패키지 설치
GPU 제품군 가상 서버를 사용하려면 다음과 같은 소프트웨어를 설치해야 합니다.
* [NVIDIA 드라이버](http://www.nvidia.com/drivers) - 이를 사용하면 운영 체제가 GPU와 통신할 수 있습니다.
* [CUDA 툴킷](https://docs.nvidia.com/cuda/) - 고성능 GPU 가속 애플리케이션에 대한 개발 환경.
* [cuDNN](https://developer.nvidia.com/cudnn) - 신경망 애플리케이션에 사용되는 _CUDA Deep Neural Network_ 라이브러리.
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - 다중 GPU 또는 다중 시스템 통신을 위한 클러스터 통신 라이브러리.
* **BLAS**(_Basic Linear Algebra Subprograms_) - 다음 라이브러리 중 하나와 같이 기본 선형 대수 연산 수행을 위한 구성 요소를 제공하는 루틴.
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

머신 러닝 프레임워크를 설치 중인 경우, 앞의 소프트웨어 패키지뿐만 아니라 다음 플랫폼 중 하나와 같은 프레임워크 소프트웨어도 설치해야 합니다.
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/)(_Convolutional Architecture for Fast Feature Embedding_) - 라이센스가 있는 오픈 소스 딥러닝 프레임워크.
* [Tensorflow(Tensorflow 1.2+)](https://www.tensorflow.org/install/) - 수치 계산을 위한 오픈 소스 소프트웨어 라이브러리를 제공합니다.

