---
title: "参考記事を元に、Python実行環境Anacondaをインストールしてみた。"
emoji: "😖"
type: "tech"
topics:
  - "python"
  - "anaconda"
published: false
published_at: "2024-11-03 00:36"
---

# 参考記事を元にPython実行環境Anacondaをインストールしてみた。

>以下、参考にしたサイト
>https://www.javadrive.jp/python/install/index5.html#section1
>
>Anaconda は Python 自身と Python でよく利用される NumPy や Jupyter といったライブラリをまとめてインストールしてくれるディストリビューション(必要なソフトウェアをまとめてパッケージしたもの)です。

※ 参考サイトの手順でインストールを行っていった備忘録になります。

## 0.インストール環境
- CPU：Intel(R) Core(TM) i7-8700K CPU
- メモリ：16.0GB
- OS：Windows11

## 1.Anacondaのインストーラのダウンロード
1 まず初めにAnacondaのインストーラをダウンロードします。下記、サイトにアクセスします。
　[Anacondaダウンロードサイト](https://www.anaconda.com/)
2 「Products」⇒Anaconda Hub の下の「Distribution」をクリックする。
3 「Submit」の下に小さくある、「Skip registration」ボタンをクリックする。
　　※メール配信等希望の場合は「Email Addresss」に自身のメールアドレスを記入し、登録する。
4 「Download」ボタンをクリックします。インストーラ実行ファイルがダウンロードされます。

## 2.Anacondaインストール
1 「Anaconda3-2024.10-1-Windows-x86_64.exe」を実行します。
2 「Next >」をクリック
3 「I Agree」をクリック
4 「All Users(requires admin privileges)」を選択し、「Next >」をクリック
5 管理者権限のポップアップが表示されるため「はい」を選択
6 インストール先のフォルダ指定ポップアップが表示されるため、「Destination Folder」へ指定フォルダを設定し、「Next >」をクリック
7 「Install」をクリック。「Completed」がログ表記されたら、「Next >」をクリック。
8 「Next >」をクリック
9 「Finish」をクリック

## Python実行確認
1 CMDを起動する。
2 「python - version」と入力し、Enterを押す
3 「Python 3.9.1」等のバージョン表記が表示されればOKです。
4 「exit()」を入力し、EnterでPython実行環境から標準のコマンド環境へ戻ることができます。
5 以上です。
 
 

