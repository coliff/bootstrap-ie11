<p style="align:center">
<img src="https://repository-images.githubusercontent.com/171514859/420fd400-c07d-11ea-90cb-58dfe1d8a3f3" width="500" alt="Bootstrap 5 for IE 11">
</p>

# Bootstrap 5 for IE 11

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/coliff/bootstrap-ie11/master/LICENSE)
[![github-stars-image](https://img.shields.io/github/stars/coliff/bootstrap-ie11.svg?label=github%20stars)](https://github.com/coliff/bootstrap-ie11)

Bootstrap 5 ([currently in Alpha](https://v5.getbootstrap.com/)) drops support for Internet Explorer 11, but you can add support back by simply adding a CSS file and a few JavaScript polyfills.

## Usage

Just add this in the `<head>` which will load the CSS and JS - just for IE users.

`<script>window.MSInputMethodContext && document.documentMode && document.write('<link rel="stylesheet" href="/css/bootstrap-ie11.min.css"><script src="https://cdn.jsdelivr.net/gh/nuxodin/ie11CustomProperties@4.1.0/ie11CustomProperties.min.js"><\/script><script crossorigin="anonymous" src="https://polyfill.io/v3/polyfill.min.js"><\/script><script>!function () { var e, t; ((e = document.createEvent("CustomEvent")).initEvent("Bootstrap", !0, !0), e.preventDefault(), e.defaultPrevented) || (t = Event.prototype.preventDefault, Event.prototype.preventDefault = function () { this.cancelable && (t.call(this), Object.defineProperty(this, "defaultPrevented", { get: function () { return !0 }, configurable: !0 })) }) }();<\/script>');');</script>`

## FAQS

### What does this fix/polyfill?

- Polyfill for CSS variables courtesy of [ie11CustomProperties](https://github.com/nuxodin/ie11CustomProperties)
- Workaround for the SVG overflow bug
- Remove the default vertical scrollbar from `textarea`
- Fixes for card image size bug
- Fixes for modals (`.modal-dialog-centered` and `.modal-dialog-scrollable`)
- Fixes for navbars (using flex for `.navbar-collapse`)
- Adds -ms- vendor prefixes for grid layout utilities (`.align-self-auto`, `.align-self-center` and `.align-self-stretch`)

### Any other things to look out for?

- Internet Explorer 11 does not support vertical alignment of flex items when the flex container has a `min-height`. [See Flexbugs #3 for more details.](https://github.com/philipwalton/flexbugs#flexbug-3)
- View a list of known issues at [https://github.com/coliff/bootstrap-ie11/issues](https://github.com/coliff/bootstrap-ie11/issues)

## Demo

See this in action at: [https://v5-bootstrap.christianoliff.com/](https://v5-bootstrap.christianoliff.com/)

## Thanks

<a href="https://www.browserstack.com/">
  <img src="https://live.browserstack.com/images/opensource/browserstack-logo.svg" alt="BrowserStack Logo" width="192" height="42">
</a>

Thanks to [BrowserStack](https://www.browserstack.com/) for providing the infrastructure that allows us to test in real browsers
