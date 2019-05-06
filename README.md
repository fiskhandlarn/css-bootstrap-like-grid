# CSS Bootstrap-like grid

![css-bootstrap-like-grid](https://user-images.githubusercontent.com/680264/57221368-449d1680-6fff-11e9-8b21-185fe7f9ad74.png)

Native CSS grid classes and SCSS mixins with (nearly) the same syntax as [Bootstrap grid](https://getbootstrap.com/docs/4.3/layout/grid/).

[![StyleCI](https://github.styleci.io/repos/185174054/shield)](https://github.styleci.io/repos/185174054)
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
- `.col-start-*-*`/`make-col-start` (used instead of `offset-*-*`/`make-col-offset`)
- `order-*-first`, `order-*-last`, `order-*-*`,

## Unsupported Bootstrap features
- [Auto width columns](https://getbootstrap.com/docs/4.3/layout/grid/#auto-layout-columns) (`col`, `col-auto`, `col-*-auto`)
- [Vertical alignment](https://getbootstrap.com/docs/4.3/layout/grid/#vertical-alignment) and [horizontal alignment](https://getbootstrap.com/docs/4.3/layout/grid/#horizontal-alignment) (since we don't have rows) (`align-items-*`, `align-self-*`, `justify-content-*`)
- [Offset classes](https://getbootstrap.com/docs/4.3/layout/grid/#offset-classes) (use `start-*` instead)
- [Margin utilities](https://getbootstrap.com/docs/4.3/layout/grid/#margin-utilities) (`m*-auto`)
- [Nested](https://getbootstrap.com/docs/4.3/layout/grid/#nesting) content other than other columns
