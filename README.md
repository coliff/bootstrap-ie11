[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/coliff/bootstrap-ie11/master/LICENSE)
[![github-stars-image](https://img.shields.io/github/stars/coliff/bootstrap-ie11.svg?label=github%20stars)](https://github.com/coliff/bootstrap-ie11)

# Bootstrap 5 for IE 11

Bootstrap 5 ([currently in Alpha](https://v5.getbootstrap.com/)) drops support for Internet Explorer 11, but you can add support back by simply adding a CSS file and including jQuery, Bootstrap 4.5 JS and a CSS variables polyfill.

## Usage

Just add this in the `<head>` which will load the CSS and JS - just for IE users.

`<script>window.MSInputMethodContext && document.documentMode && document.write('<link rel="stylesheet" href="/css/bootstrap-ie11.min.css"><script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"><\/script><script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js"><\/script><script src="https://cdn.jsdelivr.net/gh/nuxodin/ie11CustomProperties@4.1.0/ie11CustomProperties.min.js"><\/script>');</script>`

## FAQS

**Q. What does this fix/polyfill?**

A.

- Polyfill for CSS variables courtesy of [ie11CustomProperties](https://github.com/nuxodin/ie11CustomProperties)
- Workaround for the SVG overflow bug
- Remove the default vertical scrollbar from `textarea`
- Fixes for cards, modals and navbars

**Q. Any other things to look out for?**

- Internet Explorer 11 does not support vertical alignment of flex items when the flex container has a `min-height`. [See Flexbugs #3 for more details.](https://github.com/philipwalton/flexbugs#flexbug-3)

## Known Issues

- View a list of known issues at [https://github.com/coliff/bootstrap-ie11/issues](https://github.com/coliff/bootstrap-ie11/issues)
- Issues with Toasts, Tooltips, form controls

## Demo

See this in action at: [https://v5-bootstrap.christianoliff.com/](https://v5-bootstrap.christianoliff.com/)

## Thanks

<a href="https://www.browserstack.com/">
  <img src="https://live.browserstack.com/images/opensource/browserstack-logo.svg" alt="BrowserStack Logo" width="192" height="42">
</a>

Thanks to [BrowserStack](https://www.browserstack.com/) for providing the infrastructure that allows us to test in real browsers
