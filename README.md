# E2info HTML Coding Rule

## 目的

[株式会社イーツー・インフォ](https://www.e2info.co.jp/)のHTMLコーディングルールです
汎用性の高いHTMLを利用するために最低限の規約を設けます

## 内容

### コーディングはUTF-8

```
<meta charset="utf-8">
```

### id属性は極力利用しない

パーツを使い回す時に困ることが多いため、id属性は極力利用しないで下さい。

○
```
<body>
<div id="tel">
```

×
```
<body id="company">
<div class="tel">
```


### 長い文字列を考慮する

HTMLにサンプルテキストを入れる際に、文字列が長い場合の見え方を考慮して作成して下さい。
プログラム組み込み後に動的データを設定した際に、レイアウト崩れや文字列の見切れが発生することを防ぐためです。

### 画像、CSSなどのリソースは相対パスで指定する

リソースの指定は相対パスで指定して下さい。
確認用環境などでサブディレクトリに配置する場合があるためです。

○
```
./image/about/about.png
./image/news/title.png
```

×
```
<img src="/image/about/about.png">
<img src="https://example.com/image/news/title.png">
```

### 使い回しを意識したコーディングをおこなう

部分的に切り出して他のページに利用しても崩れないようなコーディングを意識して下さい。


### 画像、CSSなどのリソースファイルはなるべく1フォルダにまとめる

システム化する際に相対指定で問題が発生する場合があるため、
CSS,画像,その他リソースは１つのルートフォルダに統一してほしい。

○
```
image/about/about.png
image/news/title.png
```

×
```
about/image/about.png
news/image/title.png
```

### 画像、CSSなどのリソースファイルは内容を表す名称にする

ファイル名は意味がわかりやすいものにしてください。

○
```
news-title.png
company-access.png
```

×
```
image1.png
image2.png
image_3.png
image-4.png
```

### 命名規則を統一する

アンダーバー、ハイフンなどのルールは統一してください

```
hoge-box、hogeBox、hoge_box
```

### なるべくHTMLの用途に沿ったパーツを作成する

フォームのサブミットボタンをaタグで作るなど、見た目を重視して不自然なコーディングをおこなわないでください。
JavaScriptでの処理が必要になるなど、実装の手間が増えるためです。

○
```
<input type="submit">
```

×
```
<a class="submit>送信</a>
```


![イーツー・インフォロゴ](https://raw.githubusercontent.com/e2info/e2info-warehouse/master/images/logo/logo100x100_transparent.png)

