# fullscreen.js

A lightweight, zero-dependency script that adds a fullscreen toggle UI to any webpage.

## Features

- Adds "Launch Fullscreen" and "Exit Fullscreen" buttons to your page
- Cross-browser support (Chrome, Firefox, Safari, Edge, IE)
- Toggle button visibility by pressing `f`

## Installation

**Via script tag:**
```html
<script src="fullscreen.js"></script>
```

**Via npm:**
```bash
npm install fullscreen.js
```

**Via bower:**
```bash
bower install fullscreen.js
```

## Usage

Include the script in your HTML page. It will automatically initialize on `DOMContentLoaded` and inject a fixed control panel in the top-left corner of the page.

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Page</title>
</head>
<body>
  <!-- your content -->
  <script src="fullscreen.js"></script>
</body>
</html>
```

## Keyboard Shortcut

Press `f` to toggle the visibility of the fullscreen controls.

## Browser Support

The script uses vendor-prefixed APIs to support:

| Browser | API Used |
|---------|----------|
| Chrome, Firefox (modern) | `requestFullscreen` / `exitFullscreen` |
| Firefox (legacy) | `mozRequestFullScreen` / `mozCancelFullScreen` |
| Safari / Chrome (legacy) | `webkitRequestFullscreen` / `webkitExitFullscreen` |
| Internet Explorer | `msRequestFullscreen` |

## API

The script is self-contained and runs automatically. It operates on `document.documentElement` (the `<html>` element) by default.

### Internal Functions

- **`enterFullscreen()`** — Requests fullscreen mode for the page element using the appropriate vendor-prefixed API.
- **`exitFullscreen()`** — Exits fullscreen mode using the appropriate vendor-prefixed API.
- **`toggleVisible(e)`** — Toggles the visibility of the control panel when `f` (charCode 102) is pressed.
- **`init()`** — Creates and injects the control UI into the DOM; called on `DOMContentLoaded`.

## License

ISC © [Robin Willis](https://github.com/robincwillis)
