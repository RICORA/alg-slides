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

# gitを使った開発フロー

1. `add`=gitに管理を頼む

2. `commit`=現在のスナップショットを保存

![auto](https://git-scm.com/book/en/v2/images/lifecycle.png) (©git-scm.com)

---
<!--_class: normal-->

# gitを使った開発フロー2

ぶっちゃけこれだけだとwordをdriveとかで管理するのとあんまり変わらない 特色はBranch

### gitのBranch

 - Branchの役割

機能ごとにBranchを分割 => テストとかしてmaster / mainに追加


---

<!--_class: normal-->
# んにゃぴ...よくわかんないっす

それはそうなので比べてみよう

- git

様々なブランチが

- wordとか

直線型の履歴 = 

