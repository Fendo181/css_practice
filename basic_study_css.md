## CSS基礎文法

Q.`CSS` is 何?

A.`HTML` や `XML` (方言である `SVG`, `MathML, XHTML` などを含む) で記述された文書の、体裁や見栄えを表現するために用いられます。 `CSS` は、要素が画面上で (あるいは紙や音声といった別のメディア上で) どのように表現されるのかを定義します。


### 用語説明

- セレクタ:CSSで記述したスタイルを反映させる対象を指す
- プロパティ:どのようなスタイルを当てるかの設定値を指す

### 記述方法

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

### 色の定義


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

### セレクタの適用範囲を限定する

半角空白で区切ると、`header`内のすべての要素、という意味になる

```css
header ul {
}
```

不等号記号で区切ると、 この要素の直下にある a 要素、という意味になる

```css
header ul > a {
}
```

### marginの相殺について

>上下方向に限って発生するのですが、 margin が隣接した場合、幅の狭い方が幅の広い方に打ち消されて、幅の広い方が生き残るという仕様になっています。

3つのパターンがある

- `隣接兄弟要素`
  - 隣接兄弟要素のマージンは相殺されます
- `親要素と先頭・末尾の子要素`
  - ブロックが、その `margin-top` とその先頭の子要素の `margin-top` を分けられるような、ボーダー、パディング、インラインコンテンツ、フロートの解除 (clear) のいずれも持たない場合、もしくは、ブロックがその margin-bottom とその末尾の子要素の `margin-bottom` を分けられるような、ボーダー、パディング、インラインコンテンツ、高さ (height)、高さの最小値 (min-height) のいずれも持たない場合、マージンは相殺されます。
- `空のブロック`
  - ブロックが、その `margin-top` と `margin-bottom` を分けられるような、ボーダー、パディング、インラインコンテンツ、高さ (height)、高さの最小値 (min-height) のどれをも持たない場合、top と bottom のマージンは相殺されます。

この概念めちゃ難しすぎる...が、つまりはmargingが相殺されて余計な余白が出来てしまっている事なんだとうだと解釈した。

ref:[マージンの相殺 | MDN](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing)

### divを中央揃えにする方法

- 左右のmarginを均等に割り振って中央揃えにするという手法をよく使います。

```css
margin-left: auto;
margin-right: auto;
```

### 参考資料

- [CSS: カスケーディングスタイルシート | MDN](https://developer.mozilla.org/ja/docs/Web/CSS)
