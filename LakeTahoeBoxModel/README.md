# The CSS Box Model

This project is a small Lake Tahoe news page for exploring how the CSS box model affects layout. Open `index.html` in a browser to view the page, then inspect or edit `styles.css` to experiment with the examples.

## How the box model works

Every HTML element is laid out as a rectangular box made up of four layers:

1. **Content** — text, images, or other child elements. `width` and `height` apply to this area by default.
2. **Padding** — space between the content and the border.
3. **Border** — the line around the content and padding.
4. **Margin** — transparent space outside the border, separating the element from its neighbors.

With the default `box-sizing: content-box`, the rendered width is:

```text
total horizontal space = width + left/right padding + left/right border + left/right margin
```

The same principle applies vertically. Margins create space around an element but are not part of its visible box.

## Examples in this page

- **Banner (`#banner`)** — `width: 100%` and a `3px` border on each side. Its outer width is therefore 6px wider than its containing area under the default box model.
- **Article (`#main`)** — `width: 400px` plus `40px` of padding on both sides gives it a 480px border-box width, before margins. Its `margin: 0 auto` centers it horizontally when there is enough room.
- **Headline (`#banner .content h1`)** — `width: 400px` plus a `3px` border on each side gives it a 406px border-box width. Its `margin: 0 auto` centers it within its containing block.
- **Share bar (`.share`)** — `width: 100%` plus a `1px` border on each side makes its border-box 2px wider than its containing area.
- **Quote heading (`h2`)** — padding and margins add space around the text and affect the heading's total size.

These are useful examples of why `width: 100%` does not always mean that an element fits exactly inside its parent. Try changing the width, padding, border, or margin values in `styles.css` and observe how the layout changes.

## Using `box-sizing: border-box`

You can make declared dimensions include the padding and border by applying:

```css
* {
  box-sizing: border-box;
}
```

With `border-box`, an element set to `width: 400px` remains 400px wide including its padding and border. Compare the page before and after adding this rule to see the difference.
