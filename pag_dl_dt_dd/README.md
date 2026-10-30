# Description Lists Cheat Sheet (`dl`, `dt`, `dd`)

This folder shows a list of web browsers built with an HTML description list.
See [index.html](./index.html) for the full example.

## The elements

| Element | Purpose |
| --- | --- |
| `<dl>` | Wraps the whole description list. |
| `<dt>` | A term, name, or label (the "key"). |
| `<dd>` | The description or value that belongs to a term. |
| `<div>` | Optional wrapper that groups a `<dt>` with its `<dd>` elements. |

## Basic structure

```html
<dl>
  <dt>Firefox</dt>
  <dd>
    A free web browser developed by the Mozilla Corporation and first created in
    2004.
  </dd>

  <dt>Safari</dt>
  <dd>The default browser for iPhone, iPad and Mac devices.</dd>
</dl>
```

Each `<dt>` is followed by one or more `<dd>` elements that describe it.

## When to use a description list

Use `<dl>` whenever content is made of name-value pairs, such as:

- A glossary of terms and definitions.
- Metadata (author, date, category).
- Product details (size, color, material).
- FAQs (question and answer).

Use `<ul>` or `<ol>` for plain lists of items, and `<table>` when the data has
multiple columns.

## Multiple terms or descriptions

A term can have several descriptions, and several terms can share one
description.

```html
<dl>
  <dt>Chrome</dt>
  <dd>Developed by Google.</dd>
  <dd>First released in 2008.</dd>

  <dt>Brave</dt>
  <dt>Arc</dt>
  <dd>Both are based on the Chromium web browser.</dd>
</dl>
```

## Grouping with `<div>`

HTML allows wrapping each `<dt>`/`<dd>` group in a `<div>`. This is useful for
styling, for example with CSS grid or flexbox, without changing the meaning.

```html
<dl>
  <div>
    <dt>Arc</dt>
    <dd>A Chromium-based browser first released in 2023.</dd>
  </div>
  <div>
    <dt>Brave</dt>
    <dd>A browser first released in 2016.</dd>
  </div>
</dl>
```

Only `<div>` elements may be direct children of `<dl>` besides `<dt>`, `<dd>`,
`<script>`, and `<template>`.

## Accessibility

- Screen readers can announce the list and its terms and descriptions as
  related, so users understand which description belongs to which term.
- Keep the order strict: terms come first, followed by their descriptions.
- Do not use `<dl>` just to get indentation. Use CSS for layout.

## Default styling and CSS

Browsers show `<dd>` with an indent on the left. You can change this with CSS:

```css
dt {
  font-weight: bold;
}

dd {
  margin-left: 0;
}
```

## Tips

- Use `<dt>` for the term only; put the explanation in `<dd>`.
- Do not place headings or other block structure inside `<dt>`.
- Keep descriptions inside `<dd>`; it can contain paragraphs, lists, and links.
- Comments such as `<!-- Definition term -->` are fine for learning, but not
  needed in production code.
