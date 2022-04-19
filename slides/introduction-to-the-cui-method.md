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

- 本日使用するターミナルエミュレーター
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

# ディレクトリの構造

## ul

- li
- li

## ol

1. li
2. li

---
<!--_class: normal-->
# 数式
- MathJaxとKaTeXが使えるよ

## Gaussian distribution

$$
f(x) = \frac{1}{\sqrt{2\pi\sigma^2}}\exp{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

---
<!--_class: normal-->
# コードブロック

## Fast Fourier Transform

```python
def fft(a, inv=False):
    n = len(a)
    w = [cmath.rect(1, (-2 if inv else 2) * cmath.pi * i / n) for i in range(n >> 1)]
    rev = [0] * n
    for i in range(n):
        rev[i] = rev[i >> 1] >> 1
        if i & 1:
            rev[i] |= n >> 1
        if i < rev[i]:
            a[i], a[rev[i]] = a[rev[i]], a[i]

    step = 2
    while step <= n:
        half, diff = step >> 1, n // step
        for i in range(0, n, step):
            pw = 0
            for j in range(i, i + half):
                v = a[j + half] * w[pw]
                a[j + half] = a[j] - v
                a[j] += v
                pw += diff
        step <<= 1

    if inv:
        for i in range(n):
            a[i] /= n
```

---

<!--_class: normal-->
# インライン画像

## 幅300pxで表示
![width:300px](./common/ricora.svg)

## 高さ1cmで表示
![height:1cm](./common/ricora.svg)

## 幅300px、高さ1cmで表示
![width:300px height:1cm](./common/ricora.svg)

---
<!--_class: normal-->
# インライン画像

## 指定なし
![](./common/ricora.svg)

---
<!--_class: normal-->
# 背景画像

![bg 40%](./common/ricora.svg)
![bg 40%](./common/ricora.svg)
![bg 40%](./common/ricora.svg)

---
<!--_class: normal-->
# 背景画像

![bg vertical 30%](./common/ricora.svg)
![bg 30%](./common/ricora.svg)
![bg 30%](./common/ricora.svg)

---
<!--_class: normal-->
# 背景画像

![bg left:50% 40%](./common/ricora.svg)

---
<!--_class: normal-->
# 背景画像

![bg 30% blur:10px vertical](./common/ricora.svg)
![bg 30% drop-shadow:0,5px,10px,rgba(0,0,0,.9)](./common/ricora.svg)
![bg 30% opacity:.5](./common/ricora.svg)

---
<!--_class: normal-->

# 絵文字
:smile:
:laughing:
:blush:
:smiley:
:relaxed:
:smirk:
:heart_eyes:
:kissing_heart:
:kissing_closed_eyes:
:flushed:
:relieved:
:satisfied:
:grin:

---
<!--_class: normal-->

# h1

## h2

ページを増やしたいときはこれをコピペしてね

```html
---
<!--_class: normal-->

# h1

## h2

ページを増やしたいときはこれをコピペしてね

```

---
<!--_class: final-->

# ご清聴ありがとうございました

## h2h2h2h2h2h2h2h2