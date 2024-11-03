---
title: "参考サイトを元に、顔認証ウェブサーバ構築をやってみた"
emoji: "🍣"
type: "tech"
topics: []
published: false
---

# 参考サイトを元に、顔認証ウェブサーバ構築をやってみた

>以下、参考にしたサイト
>https://developers.gmo.jp/technology/17430/#%EF%BC%882%EF%BC%89%E3%83%91%E3%83%83%E3%82%B1%E3%83%BC%E3%82%B8%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB

※ 参考サイトの手順で作業を実施しました。

## 0.実行環境
- CPU：Intel(R) Core(TM) i7-8700K CPU
- メモリ：16.0GB
- OS：Windows11

## 1.Anacondaへの開発パッケージ追加
1 「Anaconda Prompt」を開きます。
2 コマンドにて下記を実行する

```コマンド
# pytorch, torchvision ※CPUモード
conda install pytorch torchvision cpuonly -c pytorch

# facenet-pytorch
pip install facenet-pytorch

# webサーバー関連
conda install -c conda-forge fastapi python-multipart nest-asyncio
conda install -c conda-forge uvicorn[standard]
conda install -c conda-forge websockets
conda install aiofiles jinja2

# faiss
conda install -c conda-forge faiss

# redis関連
conda install -c anaconda redis-py
```

- PyTorchはPythonの機械学習ライブラリ
- torchvisionはコンピュータビジョンのための一般的なデータセット、モデルアーキテクチャ、および一般的な画像変換から構成されています。（PyTorchのパッケージ）
-  「cpuonly」と指定しているのは、「torchivision」にGPU利用など環境によって指定が可能なため。今回はCPUのみとしている。
-  「facenet-pytorch」は顔の識別を行うライブラリ。顔画像の類似度を評価する。(-1 ～ 1 の間で値が大きいほど似ている)