# 勝手にmarginやpaddingの余白がつく場合  
- 全ての要素に対して、余白をリセットする。  
```css
html, body,
ul, ol, li,
h1, h2, h3, h4, h5, h6, p,
form, input, div {
    margin: 0;
    padding: 0;
}
```

<br>
<br>

# 要素の中央寄せ方法  
- インライン要素  (img,a,span,p,buttonなど)
  - text-align:center;  
  - 親の要素に text-align:center を記述する。  
  - 親がインライン要素だと、中央よせにならないので、ブロック要素にする。  

```html
<html>
    <head>
        <meta charset="utf-8">
        <link rel="stylesheet" type="text/css" href="sample.css">
        <title>タイトル</title>
        <style>
            .parent{
                text-align: center;
            }
        </style>
    </head>
  <body>
        <div class="parent">
            <button type="">サンプルボタン</button>
            <img src="" alt="サンプル画像">
        </div>
  </body>
</html>
```

- ブロック要素(div,h1,pなど)  
  - margin: 0 auto;  
  - widthの指定は必須(ブロック要素は基本的に横に広がっていくので」、widthの指定は必須になる)
  - 中央よせにしたい要素本体に当てる。
