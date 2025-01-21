## Flexboxの基礎知識

- フレックスコンテナ: 親要素
- フレックスアイテム: 子要素

## フレックスコンテナでよく使うプロパティ

- `flex-direction: row | row-reverse | column | column-reverse;`
  - フレックスアイテムの配置方向を指定するプロパティ
- `flex-wrap: nowrap | wrap | wrap-reverse;`
  - フレックスアイテムが折り返すかどうかを指定するプロパティ
- `justify-content`
  - フレックスアイテムの水平方向の配置を指定するプロパティ
- `flex-wrap`
  - フレックスアイテムの垂直方向の配置を指定するプロパティ
- `gap`
  - フレックスアイテム間の間隔を指定するプロパティ
- `align-items`
  - フレックスアイテムの垂直方向の配置を指定するプロパティ
  - align とついているプロパティは交差軸に関する揃えを意味するというルールがある

などなど

### フレックスアイテムでよく使うプロパティ

- `flex-grow: <number>;`
  - フレックスアイテムの伸びる比率を指定するプロパティ
- `flex-shrink: <number>;`
  - フレックスアイテムの縮む比率を指定するプロパティ
- `flex-basis: <length> | auto;`
  - フレックスアイテムの基本サイズを指定するプロパティ
- `flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]`
  - `flex-grow`, `flex-shrink`, `flex-basis`をまとめて指定するプロパティ

## 参考

- [独学の人でも大丈夫！CSS Flexboxの使い方を基礎から学べるチュートリアル | コリス](https://coliss.com/articles/build-websites/operation/css/learn-flexbox-in-30-days.html)
- [これからのCSSレイアウトはFlexboxで決まり！ | Webクリエイターボックス](https://www.webcreatorbox.com/blog/flexbox)
- [CSS Flexbox Layout Guide | CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
