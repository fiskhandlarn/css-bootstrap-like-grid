# CSS Bootstrap-like grid

Native CSS grid classes and mixins with (nearly) the same syntax as [Bootstrap grid](https://getbootstrap.com/docs/4.3/layout/grid/).

This library uses the same variables as Bootstrap (`$grid-columns`, `$grid-gutter-width`, `$grid-breakpoints`, `$container-max-widths`).

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
- [Vertical alignment](https://getbootstrap.com/docs/4.3/layout/grid/#vertical-alignment) and [Horizontal alignment](https://getbootstrap.com/docs/4.3/layout/grid/#horizontal-alignment) (since we don't have rows) (`align-items-*`, `align-self-*`, `justify-content-*`)
- [Offset classes](https://getbootstrap.com/docs/4.3/layout/grid/#offset-classes) (use `start-*` instead)
- [Margin utilities](https://getbootstrap.com/docs/4.3/layout/grid/#margin-utilities) (`m*-auto`)
- [Nested](https://getbootstrap.com/docs/4.3/layout/grid/#nesting) content other than other columns
