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
* [NVIDIA ドライバー ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://www.nvidia.com/drivers){: new_window} - オペレーティング・システムが GPU と通信できるようにします。
* [CUDA Toolkit ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://docs.nvidia.com/cuda/){: new_window} - 高性能の GPU 加速アプリケーション用の開発環境。
* [cuDNN ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://developer.nvidia.com/cudnn){: new_window} - (CUDA Deep Neural Network) ニューラル・ネットワーク・アプリケーション用に使用されるライブラリー。
* [NCCL ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://docs.nvidia.com/deeplearning/sdk/nccl-install-guide/index.html){: new_window} - マルチ GPU 通信またはマルチシステム通信用のクラスター通信ライブラリー。
* **BLAS** (_基礎線形代数サブプログラム_) - 以下のいずれかのライブラリーなど、基礎線形代数演算を実行するためのビルディング・ブロックを提供するルーチン。
  - [Atlas ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://math-atlas.sourceforge.net/atlas_install/){: new_window}
  - [cuBLAS ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://developer.nvidia.com/cublas){: new_window}
  - [MKL ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://software.intel.com/en-us/mkl-developer-reference-c-blas-and-sparse-blas-routines){: new_window}
  - [OpenBLAS ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://www.openblas.net/){: new_window}

機械学習フレームワークをインストールする場合は、前述のソフトウェア・パッケージに加えて、以下のいずれかのプラットフォームなどのフレームワーク・ソフトウェアをインストールする必要があります。
* [Caffe ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://www.nvidia.com/en-us/data-center/gpu-accelerated-applications/caffe/){: new_window} (Convolutional Architecture for Fast Feature Embedding) - ライセンス交付を受けたオープン・ソースのディープ・ラーニング・フレームワーク。
* [Tensorflow (Tensorflow 1.2+) ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://www.tensorflow.org/install/){: new_window} - 数値計算のためのオープン・ソースのソフトウェア・ライブラリーを提供します。

