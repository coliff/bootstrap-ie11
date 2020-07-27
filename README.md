<p align="center">
<img src="https://repository-images.githubusercontent.com/171514859/420fd400-c07d-11ea-90cb-58dfe1d8a3f3" width="500" alt="Bootstrap 5 for IE 11">
</p>

<h3 align="center">Bootstrap 5 for IE 11</h3>

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/coliff/bootstrap-ie11/master/LICENSE)
[![github-stars-image](https://img.shields.io/github/stars/coliff/bootstrap-ie11.svg?label=github%20stars)](https://github.com/coliff/bootstrap-ie11)

Bootstrap 5 ([currently in Alpha](https://v5.getbootstrap.com/)) drops support for Internet Explorer 11, but you can add support back by simply adding a CSS file and a few JavaScript polyfills.

## Quick start

- Download the [latest release](https://github.com/coliff/bootstrap-ie11)
- Clone the repo git clone <https://github.com/coliff/bootstrap-ie11.git>
- Install with npm `npm install bootstrap-ie11`
- Install with yarn `yarn add bootstrap-ie11`

## Usage

Just add this in the `<head>` which will load the CSS and JS - just for IE users.

`<script>window.MSInputMethodContext && document.documentMode && document.write('<link rel="stylesheet" href="/css/bootstrap-ie11.min.css"><script src="https://cdn.jsdelivr.net/gh/nuxodin/ie11CustomProperties@4.1.0/ie11CustomProperties.min.js"><\/script><script crossorigin="anonymous" src="https://polyfill.io/v3/polyfill.min.js"><\/script><script>!function () { var e, t; ((e = document.createEvent("CustomEvent")).initEvent("Bootstrap", !0, !0), e.preventDefault(), e.defaultPrevented) || (t = Event.prototype.preventDefault, Event.prototype.preventDefault = function () { this.cancelable && (t.call(this), Object.defineProperty(this, "defaultPrevented", { get: function () { return !0 }, configurable: !0 })) }) }();<\/script>');</script>`

If you'd prefer to load the bootstrap-ie11 CSS without JavaScript you could use an IE-only media query as follow:

`<link rel="stylesheet" href="/css/bootstrap-ie11.min.css" media="all and (-ms-high-contrast: active), (-ms-high-contrast: none)">`

## FAQS

### What does this fix/polyfill

- Polyfill for CSS variables courtesy of [ie11CustomProperties](https://github.com/nuxodin/ie11CustomProperties)
- Workaround for the SVG overflow bug
- Remove the default vertical scrollbar from `textarea`
- Fixes for card image size bug
- Fixes for modals (`.modal-dialog-centered` and `.modal-dialog-scrollable`)
- Fixes for navbars (using flex for `.navbar-collapse`)
- Fixes for forms (checkboxes, switches and selects)
- Adds -ms- vendor prefixes for grid layout utilities (`.align-self-auto`, `.align-self-center` and `.align-self-stretch`)

### Any other things to look out for

- Internet Explorer 11 does not support vertical alignment of flex items when the flex container has a `min-height`. [See Flexbugs #3 for more details.](https://github.com/philipwalton/flexbugs#flexbug-3)
- The ie11CustomProperties polyfill currently removes the `!important` from any CSS variables with that set [https://github.com/nuxodin/ie11CustomProperties/issues/62](https://github.com/nuxodin/ie11CustomProperties/issues/62).
- View a list of known issues at [https://github.com/coliff/bootstrap-ie11/issues](https://github.com/coliff/bootstrap-ie11/issues)

## Demo

See this in action at: [https://v5-bootstrap.christianoliff.com/](https://v5-bootstrap.christianoliff.com/)

## Thanks

<a href="https://www.browserstack.com/" rel="sponsor">
  <img src="https://live.browserstack.com/images/opensource/browserstack-logo.svg" alt="BrowserStack Logo" width="192" height="42">
</a>

Thanks to [BrowserStack](https://www.browserstack.com/) for providing the infrastructure that allows us to test in real browsers
