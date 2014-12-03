# Sample CCA app using Polymer Web components

Experimenting with Hybrid apps using Polymer Web components

## Plugin to add WKWebView

This plugin switches to using WKWebView as the WebView. Fixes bug when loading local files.

```bash
$ cca plugin add https://github.com/EddyVerbruggen/cordova-plugin-wkwebview
$ cca prepare
```

## Install/Setup

```bash
cd www/todomvc
bower install
```

Installs polymer *0.8-preview* which should be much lighter and help boost performance significantly.


## Configure entry point

Can be done in `background.js`. Here we configure it to boot
using the `index.html` of the `todomvc` :)

```js
chrome.app.runtime.onLaunched.addListener(function() {
  chrome.app.window.create('todomvc/index.html', {
    width: 244,
    height: 380,
  });
});
```

## Enjoy!

Yeah :)
