<p align="center">
<img src="https://repository-images.githubusercontent.com/171514859/420fd400-c07d-11ea-90cb-58dfe1d8a3f3" width="500" alt="Bootstrap 5 for IE 11">
</p>

<h3 align="center">Bootstrap 5 for IE 11</h3>

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/coliff/bootstrap-ie11/main/LICENSE)
[![GitHub Super-Linter](https://github.com/coliff/bootstrap-ie11/workflows/Lint%20Code%20Base/badge.svg)](https://github.com/marketplace/actions/super-linter)
[![GitHub stars image](https://img.shields.io/github/stars/coliff/bootstrap-ie11.svg?label=github%20stars)](https://github.com/coliff/bootstrap-ie11)
[![NPM Version](https://img.shields.io/npm/v/bootstrap-ie11)](https://www.npmjs.com/package/bootstrap-ie11)
[![jsdelivr](https://data.jsdelivr.com/v1/package/npm/bootstrap-ie11/badge)](https://www.jsdelivr.com/package/npm/bootstrap-ie11)

[Bootstrap 5](https://getbootstrap.com/) drops support for Internet Explorer 11, but you can add support back by simply adding a CSS file and a few JavaScript polyfills.

## Quick start

- Download the [latest release](https://github.com/coliff/bootstrap-ie11)
- Clone the repo `git clone https://github.com/coliff/bootstrap-ie11.git`
- Install with [npm](https://www.npmjs.com/package/bootstrap-ie11) `npm install bootstrap-ie11`
- Install with [yarn](https://classic.yarnpkg.com/en/package/bootstrap-ie11) `yarn add bootstrap-ie11`
- Install with [Composer](https://packagist.org/packages/coliff/bootstrap-ie11) `composer require coliff/bootstrap-ie11`

## Usage

Just add this in the `<head>` which will load the CSS and JS - just for IE users.

```html
<script nomodule>window.MSInputMethodContext && document.documentMode && document.write('<link rel="stylesheet" href="/css/bootstrap-ie11.min.css"><script src="https://cdn.jsdelivr.net/combine/npm/bootstrap@5.0.0-beta2/dist/js/bootstrap.bundle.min.js,npm/ie11-custom-properties@4,npm/element-qsa-scope@1"><\/script><script crossorigin="anonymous" src="https://polyfill.io/v3/polyfill.min.js?features=default%2CNumber.parseInt%2CNumber.parseFloat%2CArray.prototype.find%2CArray.prototype.includes"><\/script>');</script>
```

If you'd prefer to load the bootstrap-ie11 CSS without JavaScript you could use an IE-only media query as follow:

```html
<link rel="stylesheet" href="/css/bootstrap-ie11.min.css" media="all and (-ms-high-contrast: active), (-ms-high-contrast: none)">
```

The CSS can be loaded via a CDN:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-ie11@5/css/bootstrap-ie11.min.css" media="all and (-ms-high-contrast: active), (-ms-high-contrast: none)">
```

## FAQS

### What does this fix/polyfill?

- Workaround for the SVG overflow bug
- Remove the default vertical scrollbar from `textarea`
- Correct the text-wrapping and color inheritance for `legend`
- Disable auto-hiding scrollbar to avoid overlap on `pre`
- Fixes for card image size bug
- Fixes for text color and text opacity utility classes
- Improved layout for `justify-content-evenly` flex utility
- Fixes for stacks gap spacing
- Add the correct display values for `template` and `main`
- Fixes for modals (`.modal-dialog-centered` and `.modal-dialog-scrollable`)
- Fixes for forms (inputs, checkboxes, radio buttons, switches, selects, ranges, placeholders and floating labels)
- Fix for the `btn-close-white` SVG icon color
- Fix for dark carousel previous and next SVG icon colors
- Fix for `valid-tooltip` & `invalid-tooltip` positioning
- Adds vendor prefixes for `user-select-auto` and `user-select-none` utilities
- Fix for `.visually-hidden` utility class
- Fix for vertical rule `.vr` class
- Bootstrap 5 Beta 2 is loaded via CDN (The JavaScript in Bootstrap 5 Beta 3 and later is incompatible)
- Polyfill for CSS custom properties ([ie11CustomProperties](https://github.com/nuxodin/ie11CustomProperties))
- Polyfill to fix most JavaScript components ([Polyfill.io](https://polyfill.io/v3/))
- Polyfill to fix tabs ([element-qsa-scope polyfill](https://www.npmjs.com/package/element-qsa-scope))

### Known Issues

- Internet Explorer 11 does not support vertical alignment of flex items when the flex container has a `min-height`. [See Flexbugs #3 for more details.](https://github.com/philipwalton/flexbugs#flexbug-3)
- The ie11CustomProperties polyfill currently removes the `!important` from any CSS variables with that set. See [ie11CustomProperties issue #62](https://github.com/nuxodin/ie11CustomProperties/issues/62).
- SVG images with `.img-fluid` are sometimes disproportionately sized. To fix this, add `width: 100%;` or `.w-100` where necessary. This fix improperly sizes other image formats, so this isn't applied automatically.
- There is a slight delay before the ie11CustomProperties polyfill works its magic. Consider adding `body{font-family:"Segoe UI", Arial, sans-serif;}` to your IE11-only stylesheet so there isn't a delay in the text displaying.
- View a list of known issues at [https://github.com/coliff/bootstrap-ie11/issues](https://github.com/coliff/bootstrap-ie11/issues).

### How can I test this?

- Microsoft offer free [Windows 7/8.1 VMs with IE11](https://developer.microsoft.com/microsoft-edge/tools/vms/)
- [BrowserStack](https://www.browserstack.com) also offers IE11 for testing

## Demo

See this in action at: [https://coliff.github.io/bootstrap-ie11/tests/](https://coliff.github.io/bootstrap-ie11/tests/)

## Thanks

<a href="https://www.browserstack.com/" rel="sponsor">
  <img src="https://live.browserstack.com/images/opensource/browserstack-logo.svg" alt="BrowserStack Logo" width="192" height="42">
</a>

Thanks to [BrowserStack](https://www.browserstack.com/) for providing the infrastructure that allows us to test in real browsers
