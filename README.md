# データの特徴を調べるコマンド集
![test](https://github.com/Nacky002/robosys2022/actions/workflows/test.yml/badge.svg)

* **plus**
  * 標準入力から数字を読み込み、その「総和」を出力するコマンド
* **avg**
  * 標準入力から数字を読み込み、その「平均」を出力するコマンド
* **vari**
  * 標準入力から数字を読み込み、その「分散」を出力するコマンド
* **stan**
  * 標準入力から数字を読み込み、その「標準偏差」を出力するコマンド


## 動作確認済みの環境
* Ubuntu 20.04.5 LTS


## 動作確認済みのソフトウェア
* Python 3.7 ~ 3.10


## コマンドの使用方法

### インストール

* 任意のディレクトリでクローン

    ```
    $ git clone git@github.com:Nacky002/robosys2022.git
    $ cd robosys2022
    ```

### コマンドの実行

1. ファイルを作成 ( テキストエディタは何でもいい )

    ```
    $ vim example
    ```

1. ファイルに一行づつ数字を書く

    * 記入例

    ```
    5
    10
    25
    0.6
    1.4
    ```

    > * 数字と少数点以外の文字は書かない
    > * 空白 (スペース) や、空の行はいれない

1. ex.1, ex.2 のように、plus に数字を読み込ませて実行

    * ex.1

    ```
    $ ./plus < example
    ```

    * ex.2

    ```
    $ echo 1 2 3.14 4 5.06 | tr ' ' '\n' | ./plus
    ```

    > * ex.2 のようなファイルを作らない方法も可能

1. 標準出力された実行結果を確認

    * ex.1 の実行結果

    ```
    42.0
    ```

    * ex.2 の実行結果

    ```
    15.2
    ```

    > **Note**
    > * 数字と小数点以外の文字が入力されていると、エラーが出る
    > * avg, vari, stan も plus と同じ方法で使用可能


## コマンドの動作確認方法

* **test.bash**
  * plus, avg, vari, stan の動作確認用コマンド

1. test.bash を実行

    ```
    $ ./test.bash
    ```

1. 標準出力された実行結果を確認

    * 成功の場合 ( 終了ステータスは `0` )
    ```
    TEST IS SUCCESS !!
    ```

    * 失敗の場合 ( 終了ステータスは `1` )
    ```
    NG at LINE 17    TEST IS FAILED
    ```

    > **Note**
    > * NG at LINE 17 の 17 には、test.bash 内で問題が起きた行番号が入る


## ライセンス

* このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布および使用が許可されます。

© 2022 NAGAKI Yuki
