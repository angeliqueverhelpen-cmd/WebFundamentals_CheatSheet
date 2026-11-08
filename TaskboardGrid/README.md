# How to use CSS Grid

- `display`: grid
- `grid-template-columns` defines the number and sizes of the columns of the grid
- `grid-template-rows` defines the number and sizes of the rows of the grid
- `grid-template` is a shorthand for defining both grid-template-columns and grid-template-rows in one line
  vb.: grid-template: <rows> / <columns>.
- `row-gap` puts blank space between the rows of the grid
- `column-gap` puts blank space between the columns of the grid
- `gap` is a shorthand for defining both row-gap and column-gap in one line
- `grid-row-start` and `grid-row-end` makes elements span certain rows of the grid
- `grid-column-start` and `grid-column-end` makes elements span certain columns of the grid
- `grid-area` is a shorthand for grid-row-start, grid-column-start, grid-row-end, and grid-column-end, all in one line
  vb.:
  .item1 {
  grid-area: 1 / 1 / 3 / 2; /_ row-start / column-start / row-end / column-end _/
  }

- `grid-template-areas` specifies grid named grid areas
- grid layouts are two-dimensional: they have a row, or inline, axis and a column, or block, axis.
- `justify-items` specifies how individual elements should spread across the row axis
- `justify-content` specifies how groups of elements should spread across the row axis
- `justify-self` specifies how a single element should position itself with respect to the row axis
- `align-items` specifies how individual elements should spread across the column axis
- `align-content` specifies how groups of elements should spread across the column axis
- `align-self` specifies how a single element should position itself with respect to the column axis
- `grid-auto-rows` specifies the height of rows added implicitly to the grid
- `grid-auto-columns` specifies the width of columns added implicitly to the grid
- `grid-auto-flow` specifies in which direction implicit elements should be created

- 1fr 2fr = 1:2
- 200px 1fr = One fixed size column, other columns flexible.
- repeat(3, 1fr) 3 columns with even size.
- minmax(200px, 1fr) min. size 200px,but can grow.

**codeademy project**
