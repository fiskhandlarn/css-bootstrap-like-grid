# CSS Bootstrap-like grid

![css-bootstrap-like-grid](https://user-images.githubusercontent.com/680264/57221368-449d1680-6fff-11e9-8b21-185fe7f9ad74.png)

Native CSS grid classes and SCSS mixins with (nearly) the same syntax as [Bootstrap grid](https://getbootstrap.com/docs/4.3/layout/grid/).

[![Ebert](https://ebertapp.io/github/fiskhandlarn/css-bootstrap-like-grid.svg)](https://ebertapp.io/github/fiskhandlarn/css-bootstrap-like-grid)
[![Total Downloads](https://img.shields.io/npm/dt/@fiskhandlarn/css-bootstrap-like-grid.svg)](https://www.npmjs.com/package/@fiskhandlarn/css-bootstrap-like-grid)
[![Latest Version](https://img.shields.io/npm/v/@fiskhandlarn/css-bootstrap-like-grid.svg)](https://www.npmjs.com/package/@fiskhandlarn/css-bootstrap-like-grid?activeTab=versions)
[![License](https://img.shields.io/npm/l/@fiskhandlarn/css-bootstrap-like-grid.svg)](https://www.npmjs.com/package/@fiskhandlarn/css-bootstrap-like-grid)

This library uses the same variables as Bootstrap (`$grid-columns`, `$grid-gutter-width`, `$grid-breakpoints`, `$container-max-widths`).

## Installation

Install this package, with [npm](https://www.npmjs.com/), in the root directory of your project.

```bash
$ npm install @fiskhandlarn/css-bootstrap-like-grid --save-dev
```

Import it in your SCSS:

```scss
@import '@fiskhandlarn/css-bootstrap-like-grid';
```

## Classes/mixins
- `.container`/`make-container` + `make-container-max-widths`
- `.container-fluid`/`make-container`
- `.col-*`, `col-*-*`/`make-col` (`make-col-ready` is not needed)
- `.row`/`make-row` (usually not needed, can be set on a `.col` to force that `.col` down on the next row)
- `.nest-parent`/`make-nest-parent` (must be set on a `.col` that contains other (nested) `.col`'s)
- `.col-start-*-*`/`make-col-start` (used instead of `offset-*-*`/`make-col-offset`, the start number should be where the column should start and not the offset from the preceeding column)
- `order-*-first`, `order-*-last`, `order-*-*`,

## Unsupported Bootstrap features
- [Auto width columns](https://getbootstrap.com/docs/4.3/layout/grid/#auto-layout-columns) (`col`, `col-auto`, `col-*-auto`)
- [Vertical alignment](https://getbootstrap.com/docs/4.3/layout/grid/#vertical-alignment) and [horizontal alignment](https://getbootstrap.com/docs/4.3/layout/grid/#horizontal-alignment) (since we don't have rows) (`align-items-*`, `align-self-*`, `justify-content-*`)
- [Offset classes](https://getbootstrap.com/docs/4.3/layout/grid/#offset-classes) (use `start-*` instead)
- [Margin utilities](https://getbootstrap.com/docs/4.3/layout/grid/#margin-utilities) (`m*-auto`)
- [Nested](https://getbootstrap.com/docs/4.3/layout/grid/#nesting) content other than other columns

## Browsers without grid support

If CSS grid [isn't supported](https://caniuse.com/#feat=css-grid) this library uses a flex fallback. If you need to support these browsers you need to:
- Add `fallback-row-after-*`/`fallback-row-after-*-*`/`fallback-row-after-*-disable` classes or use `make-fallback-row-after`/`make-fallback-row-after-disable` mixins on all columns preceeding columns using `.row`/`make-row`
- Add `fallback-col-offset-*`/`fallback-col-offset-*-*` classes or use `make-fallback-col-offset` mixin everywhere `.col-start-*-*`/`make-col-start` is used (please note that the offset number should be used in the same manner as in [Bootstrap](https://getbootstrap.com/docs/4.3/layout/grid/#offset-classes))

## Browsers support

| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png" alt="Safari" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Safari | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari-ios/safari-ios_48x48.png" alt="iOS Safari" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>iOS Safari |
| --------- | --------- | --------- | --------- | --------- |
| last 2 versions| last 2 versions| IE11, Edge| last 2 versions| last 2 versions

## Examples

<p class="codepen" data-height="265" data-theme-id="0" data-default-tab="html,result" data-user="fiskhandlarn" data-slug-hash="vwOOdJ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="CSS Bootstrap-like grid example">
  <span>See the Pen <a href="https://codepen.io/fiskhandlarn/pen/vwOOdJ/">
  CSS Bootstrap-like grid example</a> by fiskhandlarn (<a href="https://codepen.io/fiskhandlarn">@fiskhandlarn</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
