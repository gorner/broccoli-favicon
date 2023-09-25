# @gorner/broccoli-favicon

<!--
[![Build Status](https://travis-ci.org/davewasmer/broccoli-favicon.svg?branch=master)](https://travis-ci.org/davewasmer/broccoli-favicon)
[![Dependency Status](https://david-dm.org/davewasmer/broccoli-favicon.svg)](https://david-dm.org/davewasmer/broccoli-favicon.svg)
-->

Fork of @davewasmer's [`broccoli-favicon`](https://github.com/davewasmer/broccoli-favicon) that has been updated for `favicons` v7.

Takes a single `favicon.png` and outputs various sizes and file formats for favicons for different platforms and devices. Uses [`favicons`](https://github.com/haydenbleasel/favicons), see that project's documentation for details on the full range of support favicon generation.

## Usage

Default configuration values are show below:

```js
import Favicon from "broccoli-favicon";

const outputNode = new Favicon(nodeWithFaviconImage, {
  iconPath: "favicon.png", // The path to the source image in 'nodeWithFaviconImage'

  onSuccess(htmlArray, rawObject) {
    // this method is called once the generator finishes;
    // the first parameter is an array of strings containing
    // the appropriate HTML to use the generated icons
    // and the second argument is a raw object containing serialized html objects
  },

  // The favicons config object is passed directly to the underlying `Favicons` module
  // See https://github.com/haydenbleasel/favicons for details and defaults
  faviconsConfig: {},
});
```
