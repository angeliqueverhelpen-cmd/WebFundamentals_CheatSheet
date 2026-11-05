# HTML Cheat Sheet: `article`, `aside`, and `embed`

A short guide to three HTML elements used in this practice page.

## `<article>` — self-contained content

Use `<article>` for content that makes sense on its own and could potentially
be shared or reused separately, such as a blog post, news story, or forum post.
An article often has its own heading.

```html
<article>
  <h2>A day in New York</h2>
  <p>New York is made up of five boroughs...</p>
</article>
```

In this page, the blog text is inside an `<article>`. The surrounding
`<section>` identifies the broader topic, while the article contains the
self-contained text.

## `<aside>` — supplementary content

Use `<aside>` for information related to the main content that can stand on its
own. Examples include a callout, tip, glossary, or list of recommendations.
Do not use it just because something appears at the side of the page; the
meaning of the content is what matters.

```html
<aside>
  <h2>Popular foods</h2>
  <ul>
    <li>Pizza</li>
    <li>Bagels</li>
  </ul>
</aside>
```

In this page, the list of popular foods provides supplementary information
about New York.

## `<embed>` — embedding external content

`<embed>` can include external content, such as a PDF or another resource
supported by the browser. Set the resource with `src` and provide dimensions
when needed.

```html
<embed src="document.pdf" type="application/pdf" width="600" height="800">
```

This practice page uses `<embed>` for `skylineNYC.jpg`. For a regular image,
`<img>` is usually the more appropriate semantic choice:

```html
<img src="skylineNYC.jpg" alt="The New York City skyline">
```

For video and audio, prefer the dedicated `<video>` and `<audio>` elements with
`controls` so visitors can use the built-in playback controls.

## Files

- `index.html` — the page
- `styles.css` — the styles
- `14682540_1080_1920_30fps.mp4` — video file
- `jonathanslattermusic-manhattan-traffic-2-new-york-city-1994-486893.mp3` — audio file
- `pexels-mateusz-17085986.jpg` and `skylineNYC.jpg` — images
