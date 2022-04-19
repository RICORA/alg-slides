---
marp: true
theme: custom
header: 2038/01/19
footer: © 2038 RICORA Programming Team
paginate: true
size: 16:9
---

<!--_class: top-->

# タイトルタイトルタイトルタイトルタイトルタイトルタイトル


## 名前とか

## 所属とか

## 云々

---
<!--_class: normal-->

# h1

## h2

### h3

#### h4

##### h5

**Marpit** /mɑːrpɪt/ is the skinny framework for creating slide deck from Markdown. It can transform Markdown and CSS theme(s) to slide deck composed of static HTML and CSS and create a web page convertible into slide PDF by printing.

---
<!--_class: normal-->

# 箇条書き

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

## 幅100pxで表示
![width:100px](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)

## 高さ1cmで表示
![height:1cm](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)

## 幅100px、高さ1cmで表示
![width:100px height:1cm](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)

---
<!--_class: normal-->
# インライン画像

## 指定なし
![](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)

---
<!--_class: normal-->
# 背景画像

![bg 40%](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)
![bg 40%](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)
![bg 40%](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)

---
<!--_class: normal-->
# 背景画像

![bg vertical 10%](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)
![bg 10%](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)
![bg 10%](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)

---
<!--_class: normal-->
# 背景画像

![bg left:50% 40%](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)

---
<!--_class: normal-->
# 背景画像

![bg 30% blur:10px vertical](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)
![bg 30% drop-shadow:0,5px,10px,rgba(0,0,0,.9)](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)
![bg 30% opacity:.5](https://raw.githubusercontent.com/RICORA/logo/main/favicon.svg)

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