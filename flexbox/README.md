## Flexboxの基礎知識

- Flexスコンテナ: 親要素
- Flexアイテム: 子要素

上記の概念は存在しますが、フレックスボックスを組み合わせた場合、特定の要素がコンテナでもあり、アイテムでもあるということはよくあるので注意。

これはFlexコンテナ(親)でフレックスアイテム(子)という関係があるが、Flexコンテナは直接の子を包むだけ。孫やひ孫との関係もありません。「親」と「直接の子」のみです。

つまり、親子関係があれば、Flexboxを使用できます。
したがって、子がその子のFlexコンテナになることもできます。ただし、それは別のFlexコンテナになります。また、祖父母のFlexプロパティは引き継がれません。

ここは[coliss](https://coliss.com/articles/build-websites/operation/css/learn-flexbox-in-30-days.html)さんの記事を参照してください

## フレックスコンテナでよく使うプロパティ

- `flex-direction: row | row-reverse | column | column-reverse;`
  - フレックスアイテムの配置方向を指定するプロパティ
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

- `flex`
  - flex プロパティですが、フレックスアイテムの幅の合計がコンテナの幅に満たなかったり、逆にコンテナの幅を超えた場合にどうするかを指定するためのプロパティです。
  - flex で 1 以上の整数値を指定された要素は、そのままの比率で縮んだり広がったりする。
  - Flexboxはデフォルトでは広がらないけど縮む、という特性があり、広がってほしい場合は、flexを auto か 1 以上の整数値にすれば良い。
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
