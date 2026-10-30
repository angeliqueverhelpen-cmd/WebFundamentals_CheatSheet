# HTML Tables Cheat Sheet

This folder shows a conference schedule built with semantic HTML table
elements. See [index.html](./index.html) for the full example.

## Table elements

| Element | Purpose |
| --- | --- |
| `<table>` | Wraps the whole table. |
| `<caption>` | Gives the table a title or short description. It must be the first child of `<table>`. |
| `<thead>` | Groups the header row(s). |
| `<tbody>` | Groups the main data rows. |
| `<tfoot>` | Groups summary rows such as totals. Not used in this example. |
| `<tr>` | A table row. |
| `<th>` | A header cell. Bold and centered by default, and announced as a header by screen readers. |
| `<td>` | A regular data cell. |
| `<colgroup>` / `<col>` | Define columns so you can style or group them. Not used in this example. |

## Basic structure

```html
<table>
  <caption>
    Schedule by Track and Time
  </caption>
  <thead>
    <tr>
      <th scope="col">Time</th>
      <th scope="col">Track A</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">9:00 AM</th>
      <td>Keynote: Tech Future</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">Summary row</td>
    </tr>
  </tfoot>
</table>
```

Use tables for tabular data only, not for page layout.

## `scope="col"` and `scope="row"`

The `scope` attribute on `<th>` tells browsers and assistive technologies which
cells a header applies to.

- `scope="col"`: the header applies to the cells below it in the column.
- `scope="row"`: the header applies to the cells next to it in the row.

```html
<th scope="col">Track A</th> <!-- column header -->
<th scope="row">9:00 AM</th> <!-- row header -->
```

A screen reader can then announce "Track A, 9:00 AM, Keynote: Tech Future" for a
cell, so users know what the data means.

Other values are `colgroup` and `rowgroup`, for headers that cover a group of
columns or rows.

## `colspan`

`colspan` makes a cell stretch across several columns. In this schedule, the
break spans all three track columns:

```html
<tr>
  <th scope="row">11:00 AM</th>
  <td colspan="3">Break</td>
</tr>
```

The row still adds up to four columns: one header cell plus a cell that spans
three.

## `rowspan`

`rowspan` makes a cell stretch across several rows. It is not used in this
example, but works like this:

```html
<tr>
  <th scope="row" rowspan="2">Morning</th>
  <td>Keynote</td>
</tr>
<tr>
  <!-- The "Morning" cell already occupies the first position in this row -->
  <td>Workshop</td>
</tr>
```

Rows below a `rowspan` cell must leave out the cells that are already covered.

## `<col>` and `<colgroup>`

Use these to apply attributes or styles to whole columns without repeating them
on every cell:

```html
<table>
  <colgroup>
    <col />
    <col span="2" class="highlight" />
  </colgroup>
  ...
</table>
```

- `<col>` represents one column.
- `span` on `<col>` makes it apply to several columns.
- `<colgroup>` must come after `<caption>` and before `<thead>`.

Only a few CSS properties work on columns, such as `background`, `border`,
`width`, and `visibility`.

## Tips

- Use `<th>` for headers and `<td>` for data.
- Add a `<caption>` so the table has an accessible name.
- Keep the number of cells per row consistent, counting `colspan` and
  `rowspan`.
- Use `<thead>`, `<tbody>`, and `<tfoot>` to group rows and make styling easier.
