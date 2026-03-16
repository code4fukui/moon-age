# moon-age

月齢と月の満ち欠けを視覚的に表示するWebコンポーネントです。

## デモ
https://code4fukui.github.io/moon-age/

## 機能
- 指定した日付の月齢と月の満ち欠けを表示
- 月の満ち欠けを円グラフで表現

## 使い方
HTMLに以下のように記述することで`<moon-age>`コンポーネントを使用できます。

```html
<script type="module" src="https://code4fukui.github.io/moon-age/moon-age.js"></script>
<moon-age></moon-age>
```

`value`属性で日付を指定することができます。

```html
<script type="module" src="https://code4fukui.github.io/moon-age/moon-age.js"></script>
<moon-age value="2030-01-01"></moon-age>
```

`size`属性でコンポーネントのサイズを変更できます。

```html
<script type="module" src="https://code4fukui.github.io/moon-age/moon-age.js"></script>
<moon-age size="300"></moon-age>
```

## ライセンス
このプロジェクトは[MITライセンス](https://github.com/code4fukui/moon-age/blob/main/LICENSE)の下で公開されています。