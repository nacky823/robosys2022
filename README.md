# robosys2022 コマンド
![test](https://github.com/Nacky002/robosys2022/actions/workflows/test.yml/badge.svg)

* plus
  * 標準入力から数字を読み込み、その総和を出力するコマンド
* plus.bash
  * plus コマンドの動作確認用コマンド
  * 問題がない場合、終了ステータスとして 0 を出力

* avg
  * 標準入力から数字を読み込み、その平均を出力するコマンド
* avg.bash
  * avg コマンドの動作確認用コマンド
  * 問題がない場合、終了ステータスとして 0 を出力

* vari
  * 標準入力から数字を読み込み、その分散を出力するコマンド
* vari.bash
  * vari コマンドの動作確認用コマンド
  * 問題がない場合、終了ステータスとして 0 を出力

* stan
  * 標準入力から数字を読み込み、その標準偏差を出力するコマンド
* stan.bash
  * stan コマンドの動作確認用コマンド
  * 問題がない場合、終了ステータスとして 0 を出力

## 使い方
1. "SSH" の URL をクローン
2. ex.1, ex2 のように標準入力から数字を読み込む
    * ex.1  
    ```
    seq 5 | ./plus
    ```
    * ex.2  
    ```
    echo 1 2 3 4 5 | tr ' ' '\n' | ./plus
    ```
    > **Note**
    >* 改行により、複数の数字を識別している
    >* 数字以外の文字を入力すると、エラーになる

## 必要なソフトウェア
* Python
  * テスト済のバージョン : 3.7 ~ 3.10

## テスト環境
* Ubuntu 20.04.5 LTS

## 権利関係
* このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布および使用が許可されます。

© 2022 NAGAKI Yuki
