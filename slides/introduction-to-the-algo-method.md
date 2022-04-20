---
marp: true
theme: custom
header: 2022/04/13
footer: © 2022 RICORA Programming Team
paginate: true
size: 16:9
---
<!--_class: top-->

# アルゴ式でプログラミングを体験してみよう

## RICORA Programming Team

---
<!--_class: normal-->

# はじめに

- 本日はRICORA Programming Teamの活動にお越し頂きありがとうございます:partying_face:
- 今回は**アルゴ式**:turtle:というプログラミング学習用Webサイトを使ってプログラミングを体験してみましょう

  - [https://algo-method.com/](https://algo-method.com/)

  - Web上で完結なので環境構築は不要です
- わからないことがあったら近くの人にきいてみてね(わかる人は近くのわからない人に教えてあげてね)

---
<!--_class: normal-->

# アルゴ式
- [https://algo-method.com/](https://algo-method.com/)
- 新規登録 > Twitterアカウント:bird:かメールアドレス:email:のどちらかを選ぶ
    ![height:350px](https://user-images.githubusercontent.com/56070040/163032280-aaf18e11-a937-4e1a-8a2f-8818b996dfb9.png)

---
<!--_class: normal-->

# アルゴ式
- [https://algo-method.com/](https://algo-method.com/)
- コンテンツ一覧ページまでいければ:ok:


    ![height:350px](https://user-images.githubusercontent.com/56070040/163032286-867e9139-bb34-40bf-8a0e-ff10a3397f74.png)


---
<!--_class: normal-->

# アルゴ式

- **教科書**で解説を読んで**練習問題**で演習
- まずは「入力を受け取る」をやってみましょう:beginner:
- 次に「論理的思考力を鍛える！文章題 (beta)」をやってみましょう:seedling:
- 腕に自信のある方は「全探索」やそれ以降のコンテンツに挑戦してみましょう:muscle:
- 初心者の場合、初めに触るプログラミング言語はPython:snake:が無難だと思いますが、他に興味のあるプログラミング言語がある方はそれを使用しても構いません

---
<!--_class: normal-->

# ググり方を身につけよう

- 「言語名 + やりたい事」でGoogle検索:mag_right:
- エラーメッセージが出たらコピペしてそのままググる
  - というかまず読む
- 公式や有志の書いたドキュメントを読む
- 英弱なら英語は全部Google翻訳にぶち込む
- 調べてもわからない or 調べるワードがわからないなら質問:sos:
- 最初から完全に理解しようとしない
  - 初めのうちはよくわからないけど色々調べて試したらなんか動いたで:ok:

---
<!--_class: normal-->

# ググり方クイズ 問題

## 入力を受け取る 標準出力 1-3
> 問題文
> 27182 を 818 で割った余りを表示するプログラムを作成してください。

- **アルゴ式の教科書**や**標準出力 1-1**の問題より、Pythonでは文字の出力は`print`を使うってことはなんとなくわかったけど、割り算のあまりってどうやるんだろう…？:thinking:
- キーワードを考えて検索してみてください
---
<!--_class: normal-->

# ググり方クイズ 解答例
- 「Python 割り算 余り」でGoogle検索
- こんなサイトが出てきました
  - https://www.curict.com/item/b1/b146ef1.html

  ![height:320px](https://user-images.githubusercontent.com/56070040/163033737-777dec98-0515-4108-859a-23b939762e06.png)

---
<!--_class: normal-->

# ググり方クイズ 解答例
- 出てきた記事によると余りは`%`を使って求められるらしい
  ```python
  print(5 % 2)  # 余りを求める。結果 = 1
  ```
- 5を2で割った余りが1ってことだから、元の問題に当てはめるとこうかな？
  ```python
  print(27182 % 818)
  ```
- できましたか？
- たくさん経験を積んで、誤った情報、古い情報、わかりにくい情報などに惑わされずに必要な情報だけを得られるようになろう

---
<!--_class: normal-->

# これができるとどうなるの
- プログラミング全般で役立つ
  - 計算量の感覚、アルゴリズムとデータ構造の知識、コーディング力はあるに越したことはない
- 競技プログラミングを楽しむ
  - AtCoder, yukicoder, Codeforces, TopCoderなど
  - ICPC(国際大学対抗プログラミングコンテスト)への参加
  - Google Code Jamとか色々
- IT企業への就活対策
  - コーディングテストでこういう問題を解かされる
---
<!--_class: final-->

# ご清聴ありがとうございました