# moon-age

依存関係のないウェブコンポーネントで、月齢と月の満ち欠けを視覚的に表示します。

## デモ

https://code4fukui.github.io/moon-age/

## 機能

- **視覚的な月の満ち欠け:** 月の満ち欠け（新月、満ちていく月、満月、欠けていく月）を表示します。
- **カスタマイズ可能な日付:** `YYYY-MM-DD`形式で任意の日付を設定し、対応する月の満ち欠けを確認できます。
- **リサイズ可能:** コンポーネントのサイズを簡単に調整できます。
- **スタンドアロン:** 軽量で自己完結型のウェブコンポーネントです。

## 使い方

### 1. コンポーネントの読み込み

CDNからJavaScriptモジュールを読み込みます。

```html
<script type="module" src="https://code4fukui.github.io/moon-age/moon-age.js"></script>
```

### 2. HTMLに追加

`<moon-age>`タグを使用します。デフォルトでは現在の日付の月の満ち欠けを表示します。

```html
<moon-age></moon-age>
```

### 3. 属性でカスタマイズ

- `value`: `YYYY-MM-DD`形式で特定の日付を設定します。
- `size`: コンポーネントの幅と高さをピクセル単位で指定します（例: `size="100"`）。

```html
<!-- 2030年1月1日の月の満ち欠けを150pxのサイズで表示 -->
<moon-age value="2030-01-01" size="150"></moon-age>
```

### 4. プログラムからの制御

JavaScriptを使用してコンポーネントを作成・制御することも可能です。

```html
<div id="moon-container"></div>
<input type="date" id="date-picker">

<script type="module">
  // プロジェクト内のローカルコピーからインポートすることを推奨します
  import { MoonAge } from "https://code4fukui.github.io/moon-age/moon-age.js";

  // 200pxのサイズで新しいインスタンスを作成
  const moon = new MoonAge(200);
  document.getElementById("moon-container").appendChild(moon);

  // 日付を動的に更新
  const datePicker = document.getElementById("date-picker");
  datePicker.onchange = () => {
    moon.setDate(datePicker.value);
  };

  // 初期値の設定
  datePicker.value = new Date().toLocaleDateString("sv");
  datePicker.onchange();
</script>
```

## クレジット

このプロジェクトは、akebi_mh氏によるオリジナルの作品をウェブコンポーネント化したものです。

- **オリジナルソース:** [月齢と月の満ち欠けを表示 #JavaScript - Qiita](https://qiita.com/akebi_mh/items/b6a9c056d9198552e7b4)

## ライセンス

[MIT](LICENSE)
