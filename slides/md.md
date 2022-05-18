---
marp: true
theme: custom
header: 2022/05/18
footer: © 2022 RICORA Programming Team
paginate: true
size: 16:9
---

<!--_class: top-->

# Markdown の使い方
## RICORA Programming Team

---

<!--_class: normal-->

# はじめに

- こんばんは。来ていただきありがとうございます。😃

- 簡単な演習もつけてます。手を動かして学んでいきましょう！🫠

---

<!--_class: normal-->

# Markdown について

- Markdown は[マークアップ言語](https://ja.wikipedia.org/wiki/%E8%BB%BD%E9%87%8F%E3%83%9E%E3%83%BC%E3%82%AF%E3%82%A2%E3%83%83%E3%83%97%E8%A8%80%E8%AA%9E)の 1 つであり、変換ツールを噛ますことにより、HTML や $\LaTeX$ などの別のマークアップ言語 / 組版言語に変換をすることができる。

- また、Pandoc や Marp、SATySFi などを用いれば高品質な PDF を生成することも可能。いろいろなツールを使うと様々なことができる。

- 最近の技術系プラットフォームでは Markdown 記法をサポートしているものが多い（GitHub, Discord, Qiita など）。そのため、Markdown はプログラミングを学ぶ上で知っておいて損はない。

---

<!--_class: normal-->

# 補足: HTMLについて

- HTMLはHyperText Markup Languageの頭文字をとったもの。

- ウェブサイトの構造を記述する言語

- でも書くのが結構面倒くさい

このスライド:
```html
<h1> 補足: HTMLについて </h1>
<ul>
  <li> HTML... </li>
  <li> ウェブサイトの... </li>
  <li> でも書くのが... 面倒 </li>
</ul>
```

---

<!--_class: normal-->

# 補足：$\LaTeX$ について

- 組版ソフトウェア。組版は文字を組んでくれるってこと。

- これも結構書くのが面倒くさい（個人的な意見ですが。。。）

- でも式がきれいに書ける＋枯れているので技術的保証がある

構文とかが気になる人は自分で見てみてね

---

<!--_class: normal-->

# Markdown のメリット

HTMLとか$\LaTeX$で表現できることはいろいろあるんだけど、書くのがめんどい
$\longrightarrow$ Markdownを使おう！

### Markdownのいいところ

- HTMLや$\LaTeX$などと比べると、とても簡単に書くことができる。

- 覚えやすい記述方式である。

- 数式や表などを入力できる。

---

<!--_class: normal-->

# Markdown の記述方法

実際にどういう書き方をするか見ていこう。

このスライドで触れるもの:

- 見出し h1...h6
- 段落・区切り線・ 箇条書き
- 表・数式
- リンク・画像・ソースコード（プログラム）の埋め込み

すべて上に表示例、下にmdで書く際の書式になっている

---

<!--_class: normal-->

# 見出し

見出しはこんな感じで書ける:

# h1

```md
# h1
```

## h2

```md
## h2
```
---

<!--_class: normal-->

# 見出し

h3とh4はレポートの中で節とかを記述するときに使う

### h3

```md
### h3
```

### h4

```md
#### h4
```
---

<!--_class: normal-->

# 見出し

h5とh6はあんまり使わないかも。

##### h5

```md
##### h5
```
###### h6

```md
###### h6
```
---

<!--_class: normal-->

# 段落
空の行を一行挿入するか、半角スペースを行末に2つ挿入すると改行できる。

東京理科大学

電子計算機  
研究会

```
東京理科大学
[空]
電子計算機__
研究会
```

---

<!--_class: normal-->

# 区切り線

３種類あるけど全部同じ区切り線になる。

```
---
あああ
___
あああ
***
あああ
```

---

<!--_class: normal-->

# 箇条書き

行頭に半角ハイフン ( - )  + スペースを入れる。
- RICORA

```
- RICORA
```

---

<!--_class: normal-->

# 引用

半角大なり ( > ) を行頭に書く。途中で ( > ) を増やすことにより 2 段引用できる。
> 大井川 波に塵なし 夏の月
>  > 松尾芭蕉

```
> 大井川 波に塵なし 夏の月
>  > 松尾芭蕉
```

---

<!--_class: normal-->

# リンク

説明とリンクをそれぞれ角括弧、丸括弧で書く

[RICORA 言語班](https://alg.tus-ricora.com/)

```
[RICORA 言語班](https://alg.tus-ricora.com/)
```

---

<!--_class: normal-->

#  画像

リンクに感嘆符をつけるだけ。かんたんだね。

```
![説明](URL)
```
![RICORA](https://avatars.githubusercontent.com/u/33452053?s=200&v=4)
```
![RICORA](https://avatars.githubusercontent.com/u/33452053)
```

---

<!--_class: normal-->


# 数式

```$$```で囲った間に $\TeX$ で書いた式を入れれば式として表示される。

$\left(\bigcap_{i=1}^\infty\bigcup_{j=i}^\infty A_j\right)=0$

```
$\left(\bigcap_{i=1}^\infty\bigcup_{j=i}^\infty A_j\right)=0$
```

---

<!--_class: normal-->

# 表

一行目に列名、二行目に揃え方、三行目以降にデータ

|指定なし|中央揃え|右揃え|左揃え|
| - | :-: | -: | :- |
|あ|い|う|え|

```
|指定なし|中央揃え|右揃え|左揃え|
| - | :-: | -: | :- |
|あ|い|う|え|
```

---

<!--_class: normal-->

# ソースコード（プログラム）　

\```で文字を囲うことによりコード記述になる。インデントでも代用可。

```C++
#include <iostream>
int main() {
    std::cout << "Hello, World!" << std::endl;
}
```

    ``` C++
    #include <iostream>
    int main() {
      std::cout << "Hello, World!" << std::endl;
    }
    ```
---

<!--_class: normal-->
# ソースコード（プログラム）　

行中の引用はバッククオートで囲うとできる。

`print('Hello, world!')`のように埋め込むことができる。

```
`print('Hello, world!')`のように埋め込むことができる。
```

---

<!--_class: normal-->

# Markdownで自己紹介

- いま学んだことを使って自己紹介を書いてみましょう。

- 注意とか

   - わからないことは悪いことではありません。上級生に聞いて🆗
   - スライドを手元においておくと書きやすいかも
   - DON'T PANIC! 周りのペースが早くても焦らずに取り組もう
   - 質問がある場合は挙手していただけると助かります🙇

---

<!--_class: normal-->

# VSCode をインストールしよう

https://alg-wiki.tus-ricora.com/vscode-tutorial/

上のリンクにアクセスして、導入方法の節の手順に従ってください。

分からない・どこかでインストール中断した場合は上級生に聞いてください。

---

<!--_class: normal-->

# Markdownを使う準備

- VS Codeを開き、File → New Text File → Select a language → Markdown と入力

- 試しに

   ```
   # example

   ## こんにちは

   はろー

   ```

などと打ち込んでCtrl + Shift + P で表示されることを確認

---
<!--_class: normal-->

# Markdownで自己紹介

それでは、Markdownで自己紹介を書いてみましょう。

### 書いてほしいこと

- 名前 or ハンドルネーム (h2)
- 学科と学年 (表)
- RICORA に入ってやりたいこと (ソースコードで)
- 各種SNS もしくは何かしらのホームページ (リンクで) 

---
<!--_class: normal-->

# フォーマット

## 自己紹介(h1)
### 名前 or ハンドルネーム (h2)

|学科|学年|
| - | :-: |
| (なんちゃら科) |$n$年|

### やりたいこと(h2)
```
(やりたいことの内容 例: Web 開発)
```

---
<!--_class: normal-->

# フォーマット - 続き

### SNS / Webサイト(h2)
[Twitter](https://twitter.com) [TUS](https://www.tus.ac.jp)

- こんな感じで(h1)、(h2)と書かれているものも含めて書いてください

- 終わったら挙手して上級生に見せてね

- SNSのアカウントの記載はもちろん任意です。嫌だったら理科大のリンクをつかってね

---

<!--_class: final-->

# ご清聴ありがとうございました
