# moon-age

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A web component that displays the current moon age and phase.

## Demo
https://code4fukui.github.io/moon-age/

## Features
- Displays the current moon age and phase as a visual component
- Supports setting the moon age date
- Customizable size

## Usage
To use the `moon-age` web component, include the JavaScript file and add the `<moon-age>` element to your HTML:

```html
<script type="module" src="https://code4fukui.github.io/moon-age/moon-age.js"></script>
<moon-age></moon-age>
```

You can also set the `value` attribute to display the moon age for a specific date:

```html
<script type="module" src="https://code4fukui.github.io/moon-age/moon-age.js"></script>
<moon-age value="2030-01-01"></moon-age>
```

And the `size` attribute to customize the size of the component:

```html
<script type="module" src="https://code4fukui.github.io/moon-age/moon-age.js"></script>
<moon-age size="300"></moon-age>
```

## License
MIT License — see [LICENSE](LICENSE).