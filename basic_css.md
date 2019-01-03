### CSS基礎文法

Q.`CSS` is 何?

A.`HTML` や `XML` (方言である `SVG`, `MathML, XHTML` などを含む) で記述された文書の、体裁や見栄えを表現するために用いられます。 `CSS` は、要素が画面上で (あるいは紙や音声といった別のメディア上で) どのように表現されるのかを定義します。


#### 用語説明

- セレクタ:CSSで記述したスタイルを反映させる対象
- プロパティ:どのようなスタイルを当てるかの属性

#### 記述方法

ex1)`html`の`head`内で記述する方法

h1タグで囲まれた文章は赤くなる

```html
<head>
    <style>
        h1 {
            color: red;
        }
    </style>
</head>
```

ex2)別ファイルで管理する方法

```html
<head>
<!-- cssファイルを読み込む -->
<link rel="stylesheet" href="style.css">
</head>
```

#### 色の定義


```css
{
    /* 文字指定 */
    color:red;
    /* RGB指定 */
    color:rgb(140, 238, 42);
    /* 16進数 */
    color:#0000ff;
    /* red と green と blue で同じ記号が並ぶ場合は、もっと短く書くことができて */
    color:#00f
}
```

>※CSSでは同じセレクタに対して、同じプロパティを複数設定したら、後から書いたほうが優先されます

### CSSのBoxモデルについて

CSSは1つ1つの領域に対して、`コンテンツ境界`、`パディング境界`、`ボーダー境界 (border edge)`、`マージン境界 (margin edge)`が定義されています。
尚、対象の要素に対して領域の外に設定されている値がない場合は、隣接する要素で設定されます。

>それぞれのボックスは4つの部品 (または領域) から構成され、それぞれの辺についてコンテンツ境界 (content edge)、パディング境界 (padding edge)、ボーダー境界 (border edge)、マージン境界 (margin edge) が定義されています。


ref:[CSS 基本ボックスモデルの紹介 | MDN](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
### 参考資料


- [CSS: カスケーディングスタイルシート | MDN](https://developer.mozilla.org/ja/docs/Web/CSS)
