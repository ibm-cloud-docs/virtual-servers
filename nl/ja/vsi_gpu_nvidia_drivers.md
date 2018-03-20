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

# GPU ドライバーおよびソフトウェア・パッケージのインストール
GPU ファミリーの仮想サーバーを使用するには、事前に以下のソフトウェアをインストールしておく必要があります。
* [NVIDIA ドライバー](http://www.nvidia.com/drivers) - オペレーティング・システムが GPU と通信できるようにします。
* [CUDA Toolkit](https://docs.nvidia.com/cuda/) - 高性能の GPU 加速アプリケーション用の開発環境。
* [cuDNN](https://developer.nvidia.com/cudnn) - _(CUDA Deep Neural Network)_ ニューラル・ネットワーク・アプリケーションに使用されるライブラリー。
* [NCCL](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html) - マルチ GPU 通信またはマルチシステム通信用のクラスター通信ライブラリー。
* **BLAS** (_基礎線形代数サブプログラム_) - 以下のいずれかのライブラリーなど、基礎線形代数演算を実行するためのビルディング・ブロックを提供するルーチン。
  - [Atlas](http://math-atlas.sourceforge.net/atlas_install/)
  - [cuBLAS](https://developer.nvidia.com/cublas)
  - [MKL](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines)
  - [OpenBLAS](http://www.openblas.net/)

機械学習フレームワークをインストールする場合は、前述のソフトウェア・パッケージに加えて、以下のいずれかのプラットフォームなどのフレームワーク・ソフトウェアをインストールする必要があります。
* [Caffe](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/) (_Convolutional Architecture for Fast Feature Embedding_) - ライセンス交付を受けたオープン・ソースのディープ・ラーニング・フレームワーク。
* [Tensorflow (Tensorflow 1.2+)](https://www.tensorflow.org/install/) - 数値計算のためのオープン・ソースのソフトウェア・ライブラリーを提供します。

