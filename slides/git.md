---
marp: true
theme: custom
header: 2022/05/18
footer: © 2022 RICORA Programming Team
paginate: true
size: 16:9
style: |
  blockquote {
    font-style: italic;
    font-weight: bold;
  },
  section img {
    text-align: center;
  }
---

<!--_class: top-->

# git / GitHub 入門講座

## RICORA Programming Team

---
<!--_class: normal-->

# はじめに

- バージョンコントロールシステムであるgitの使い方を学ぼう

- mdの使い方と二本立てで大変だと思いますが...

---

<!--_class: normal-->


# gitってなに？

>  Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. 

- 要約すると「gitは早くて効率的なオープンソース分散型バージョンコントロールシステム」

- それって実際どういうこと？

---
<!--
_class: normal
_style: |
  section {
    text-align: center;
  }
-->

# gitが作られた背景

- 最近人間味が出てきたこと`Linux`の製作者*Linus Torvalds*が作った

- メールで送られてくるパッチを早くマージしてかつトラッキングするツールがほしかったらしい

![w: 50](https://i.gzn.jp/img/2021/06/11/linus-torvalds-rages-anti-vaccine/00.jpg) Linus Torvalds (©Gigazine.net)

---

<!--_class: normal-->

# メリット

- 早い
   サーバーから拾ってくるときにそんなに時間がかからない

- ログを追える
   このファイルはどこで変更されて...みたいなことがわかる

- 複数人での開発に向く
   各人が開発した成果を持ち寄りやすい 

- 管理するファイルを選べる
   .DS_Storeとかを含まないようにできる

---
<!--_class: normal-->
# gitを用いた開発フロー

0. `clone` とか `fork` & ブランチ分ける

1. `add` & `commit` 実質的な開発

2. `push`
   リモートサーバーに現在のリポジトリの状態を通知

3. Pull Request (GitHub利用)
   main / masterに機能追加してください!と頼む

4. `merge` 機能追加

5. 0-4の繰り返し

---
<!--_class: normal-->

# clone & fork

- `clone`はその名の通りクローン＝コピーをとってくる

めっちゃ`clone`することが多い 基本構文は
```
$ git clone (repo url)
```

- `fork`はもとのリポジトリを自分のとこにコピー

そこから自分で機能追加とかできる

---
<!--_class: normal-->

# clone & fork

- これで開発の準備ができる

- 例えば`log`を見てみる（あとでこれが何をするか説明）
```
$ git log -p
```
なんかログっぽいのが出る

---
<!--_class: normal-->

# add & commit (大事！)

- `add`=gitに管理を頼む 変更を加えたファイルを選ぶ

- `commit`=現在のスナップショットを保存 
このスナップショットについてメッセージも書く(ログ)

![w:700](https://git-scm.com/book/en/v2/images/lifecycle.png) (©git-scm.com)

---
<!--_class: normal-->

# add

- どのファイルを`git`に管理してもらうかを指定できる

- 絶対に無視したいファイルもある → `.gitignore`で指定

a.  ファイル指定で`add`（推奨）
  ```
  $ git add (something)
  ```

b. ファイル全体を`add`（非推奨）
  ```
  $ git add .
  ```
---
<!--_class: normal-->

# commit

- 今の状態を保存するように頼む
- コミットログを書く=なにを変更したのかを書く

コマンドは
```
git commit -m (message)
```

- 過去のコミットはこれで追う
  ```
  git log
  ```

---
<!--_class: normal-->

# branch

これだけだとdriveとかとあんまり変わらない 特色は*Branch*

### gitのブランチ

 - ブランチ?
    別の世界線 = 別の履歴のこと ヽ(*ﾟдﾟ)ノｶｲﾊﾞｰ
    ブランチごとに`add`/`commit`する
    履歴を分離させることで機能別に開発ができる

機能ごとにBranchを分割 => master / mainに追加を繰り返す
例: `docs/readme`とか

---
<!--_class: normal-->

# branch

- 切り替え
  ```
  git switch (branch name)
  ```

- 新規作成
  ```
  git switch -c (branch name)
  ```

あとは`man git-branch`で検索

---
<!--_class: normal-->
# んにゃぴ...よくわかんないっす

それはそう

- git

   様々なブランチにコミット → mainとかに取り込んでもらう
   コミットの履歴がある

- driveとか
   
   適当にファイルを入れる → 何が変更されたのかわからない
   規模がでかくなると削除とかでぐちゃぐちゃになりがち

##### =>   git使ったほうがよさそう（と思ってほしい）

---
<!--_class: normal-->

# リモートサーバーとかの話

- もちろん当時からLinuxは複数人で開発されていた
- `git`の威力はリモートサーバーがあるからこそ発揮される

---
<!--_class: normal-->

# clone

- 再掲。リモートサーバーからリポジトリごと拾ってくる。
  ```
  git clone
  ```

---
<!--_class: normal-->

# push

- サーバーに変更分を通知
- あっち側にもbranchがあるので指定が必要（最初だけ）

a. 現在のbranchからpushしたことがない
  ```
  git push --set-upstream (remote branch name)
  ```
b. pushしたことがある
  ```
  git push
  ```
---
<!--_class: normal-->
# fetch / pull

ここらへんは名前だけ一旦覚えておく

- `fetch`
  リモートサーバーのbranchのHEADを拾ってくる。

- `pull`
  fetch & merge する。とりあえず更新するときに使うみたいなイメージ

---
<!--_class: normal-->
# 全体の総括

0. `clone` & ブランチ分ける`switch`

1. `add` & `commit` 実質的な開発

2. `push`
   リモートサーバーに現在のリポジトリの状態を通知

3. Pull Request (GitHub利用)
   main / masterに機能追加してください!と頼む

4. `merge` 機能追加

5. 0-4の繰り返し

