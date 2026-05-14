# moon-age

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A zero-dependency web component that displays the moon age and phase visually.

## Demo

https://code4fukui.github.io/moon-age/

## Features

- **Visual Moon Phase:** Displays the moon's phase (new, waxing, full, waning).
- **Customizable Date:** Set any date in `YYYY-MM-DD` format to see the corresponding moon phase.
- **Resizable:** Easily adjust the component's size.
- **Standalone:** A lightweight, self-contained web component.

## Usage

### 1. Include the Component

Load the JavaScript module from the CDN.

```html
<script type="module" src="https://code4fukui.github.io/moon-age/moon-age.js"></script>
```

### 2. Add to HTML

Use the `<moon-age>` tag. By default, it displays the moon phase for the current date.

```html
<moon-age></moon-age>
```

### 3. Customize with Attributes

- `value`: Set a specific date in `YYYY-MM-DD` format.
- `size`: Set the component's width and height in pixels (e.g., `size="100"`).

```html
<!-- Show the moon phase for January 1, 2030, with a size of 150px -->
<moon-age value="2030-01-01" size="150"></moon-age>
```

### 4. Programmatic Control

You can also create and control the component using JavaScript.

```html
<div id="moon-container"></div>
<input type="date" id="date-picker">

<script type="module">
  // It's recommended to import from a local copy in your project
  import { MoonAge } from "https://code4fukui.github.io/moon-age/moon-age.js";

  // Create a new instance with a size of 200px
  const moon = new MoonAge(200);
  document.getElementById("moon-container").appendChild(moon);

  // Update the date dynamically
  const datePicker = document.getElementById("date-picker");
  datePicker.onchange = () => {
    moon.setDate(datePicker.value);
  };

  // Set initial value
  datePicker.value = new Date().toLocaleDateString("sv");
  datePicker.onchange();
</script>
```

## Credit

This project is a web component adaptation of the original work by akebi_mh.

- **Original Source:** [月齢と月の満ち欠けを表示 #JavaScript - Qiita](https://qiita.com/akebi_mh/items/b6a9c056d9198552e7b4)

## License

[MIT](LICENSE)