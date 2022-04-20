---
marp: true
theme: custom
header: 2022/04/20
footer: © 2022 RICORA Programming Team
paginate: true
size: 16:9
---

<!--_class: top-->

# コマンドライン入門講座

## RICORA Programming Team

---
<!--_class: normal-->

# はじめに

- 本日はRICORA Programming Teamの活動にお越し頂きありがとうございます:partying_face:

- 今回はCUIの使い方の基本を学びます📝

- 本日使用するターミナルエミュレータ
    * Mac -> Terminal
    * Windows -> PowerShell

---
<!--_class: normal-->

# 準備

## Windows

1. PowerShellを起動する
2. 以下のコマンドを入力する(理科大Wi-Fi内で)

```sh
ssh (学籍番号)@tusedls00.ed.tus.ac.jp
```

環境構築に詳しい人は、wsl2, Git Bash, Cygwinなどをインストールしてみよう。

---

# 準備

## MacOS

1. Terminalを起動する

---

<!--_class: normal-->

# ディレクトリとは

ファイルを格納する場所のことをいいます

ディレクトリ $\fallingdotseq$ フォルダ

特に、Unix系のファイルシステムでは「ディレクトリ」, Windows系のファイルシステムでは「フォルダ」といいます

---

<!--_class: normal-->

# ディレクトリの構造

ディレクトリは**ルートディレクトリ**という大本のディレクトリを**根**とした**木構造**をしています

![height: 150](https://image.itmedia.co.jp/ait/articles/1604/08/nyumon_07-zu01.png) [画像の転載元](https://atmarkit.itmedia.co.jp/ait/articles/1604/08/news019.html)


---

<!--_class: normal-->

# ディレクトリの基本知識

| 名前 | 記号 | 説明 |
| :---: | :---: | :---: |
| ルートディレクトリ | / | 基準となるディレクトリ |
| ホームディレクトリ | ~ | シェルへのログイン時のディレクトリ |
| カレントディレクトリ | . | 自分がいまいるディレクトリ |
| 親ディレクトリ | .. | カレントディレクトリの一つ*上*のディレクトリ|

---
<!--_class: normal-->

# パスってなに？

目的のファイル・ディレクトリへの*道筋*のことです

「どこから道案内をするか？」で二通りの書き方があります

## 絶対パス

**ルートディレクトリ**からの*道筋*を**絶対パス**といいます

## 相対パス

**カレントディレクトリ**からの*道筋*を**相対パス**といいます

---

<!--_class: normal-->

# コマンドってなに？

プログラムが書かれたファイルをごにょごにょすると機械語のファイルにできます（詳しくはあとで部員に聞いてね！）

そういう実行ファイルを**コマンド**といいます。

たとえば...
 - *echo* echo コマンドの後に書いたことを出力してくれる
 - *ls* いまいるディレクトリのファイルを全て表示してくれるよ 

---
<!--_class: normal-->

# コマンドの使い方

コマンドを実行するときに、*引数*というものをとってもらうことができます

``` 
$ (コマンド) (引数1) (引数2) (引数3) ...
```

例1. Cコンパイラ`gcc`でC言語ファイル`file.c`をコンパイルする `gcc file.c`

---
<!--_class: normal-->

# コマンドの使い方 つづき

特に'-'(ハイフン)がついているものを**オプション**といいます。

例2. `-v`、`--verbose`をつけるとより詳細な出力をしてくれるよ
例3. `-h`、`--help`をつけるとヘルプ画面を表示してくれます

例4. Cコンパイラ`gcc`でC言語ファイル`file.c`をコンパイルして、実行ファイル名を`ricora`にする 
    ```
    gcc file.c -o ricora
    ```

この後のコマンドでも引数やオプションを使う場面は多く出てきます

---
<!--_class: normal-->

# pwd (print working directory)

いまいるディレクトリの場所を表示してくれます

こんな感じ：
```
$ pwd
/home/ricora/guidance/shinkan
```

---
<!--_class: normal-->

# cd (change directory)

ディレクトリに移動することができます

ここで引数が重要

引数なし `cd`はホームディレクトリ
```
$ cd
$ pwd
/home/ricora
```
---
<!--_class: normal-->
# cd (change directory) つづき

引数つき`cd`はその場所があればそこへ
- 相対パスの場合 

  ```
  $ cd ../shinkan
  $ pwd
  /home/shinkan
  ```
  
  .(ドット)はいまいるディレクトリ、..(二重ドット)は一つ上のディレクトリという意味

---
<!--_class: normal-->
# cd (change directory) つづき

- 絶対パスの場合

  ```
  $ cd /home/shinkan
  $ pwd
  /home/shinkan
  ```
---
<!--_class: normal-->
# ls (list)

いまいるディレクトリにあるファイル一覧を表示してくれます

```
$ ls
a.out hi.txt shinkan.pdf
```

引数に`-l`や`-a`をつけると詳しい出力結果が得られる
```
$ ls -l

drwxr-xr-x (なんとか) (なんとか) ./
drwxr-xr-x (なんとか) (なんとか) ../
-rwxr-xr-x (なんとか) (なんとか) a.out ...
```

---
<!--_class: normal-->
# mkdir (make directory)

ディレクトリを作ります

```
$ mkdir ricora-shinkan 
$ ls
... ricora-shinkan ... 
```
---
<!--_class: normal-->

# touch (change file timestamp)

本当はファイルの作成日時を変えるコマンドだけどファイルづくりもできる

```
$ touch ricora-alg.hs
$ ls
... ricora-alg.hs ...
```

ファイルの作成日時は`ls -al`とかで確認できる

---
<!--_class: normal-->

# rm (remove)

ファイルを削除します

```
$ rm ricora-shinkan-0410.txt
```

ディレクトリを消すときは`-d`オプション、ディレクトリ内も削除するなら`-r`オプション

```
$ rm -rd ricora-shinkan-0410
```

---
<!--_class: normal-->

# man (manual)

コマンドのマニュアルを見るコマンド

```
man echo
```

マニュアルは英語だけど、ググるよりも欲しい情報が確実に載っている

/(スラッシュ)を打つと検索できる

---
<!--_class: normal-->
# やってみよう

うに

---
<!--_class: final-->

# ご清聴ありがとうございました

## h2h2h2h2h2h2h2h2
## h2h2h2h2h2h2h2h2
