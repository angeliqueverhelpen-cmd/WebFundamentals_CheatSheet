# Creating Breadcrumb Navigation with CSS

Breadcrumbs show users where the current page sits in a website's hierarchy. This project creates a horizontal breadcrumb trail with arrow-shaped links using HTML and CSS.

## Project files

- `index.html` contains the breadcrumb items.
- `breadcrumb.css` styles the breadcrumb trail and creates the arrow shapes.
- `styles.css` contains the general page styles.

The HTML loads `styles.css` first and `breadcrumb.css` second. This lets the breadcrumb-specific rules override general link styles where needed.

## 1. Add the breadcrumb markup

Use a list to represent the hierarchy. Each item links to a page or section:

```html
<ul class="breadcrumb">
  <li><a href="/asia">Asia</a></li>
  <li><a href="/asia/singapore">Singapore</a></li>
  <li><a href="/asia/singapore/tourism">Tourism</a></li>
  <li><a href="/asia/singapore/tourism/hotels">Hotels</a></li>
</ul>
```

Replace the example URLs with the actual destinations in your website.

## 2. Arrange the items horizontally

The `.breadcrumb` class targets the list, and floating each list item places the links next to one another:

```css
.breadcrumb {
  text-align: left;
}

.breadcrumb li {
  float: left;
}
```

## 3. Style the links

Position each link so its pseudo-elements can be placed relative to it. The fixed height and line height vertically center the link text:

```css
.breadcrumb a {
  color: #fff;
  background: darkcyan;
  text-decoration: none;
  position: relative;
  height: 30px;
  line-height: 30px;
  text-align: center;
  margin-right: 15px;
  padding: 0 5px;
}
```

## 4. Create the arrow shapes

The `::before` and `::after` pseudo-elements use CSS borders to make triangles. The left triangle creates the notch, while the right triangle forms the arrow point:

```css
.breadcrumb a::before,
.breadcrumb a::after {
  content: "";
  position: absolute;
  border-color: darkcyan;
  border-style: solid;
  border-width: 15px 5px;
}

.breadcrumb a::before {
  left: -10px;
  border-left-color: transparent;
}

.breadcrumb a::after {
  left: 100%;
  border-color: transparent;
  border-left-color: darkcyan;
}
```

The `15px` vertical border matches half of the link's `30px` height. Adjust the border widths and link height together if you change the dimensions.

## 5. Add a hover state

Update the link and both triangles to the same color so the arrow remains visually connected when hovered:

```css
.breadcrumb a:hover {
  background-color: blue;
}

.breadcrumb a:hover::before {
  border-color: blue;
  border-left-color: transparent;
}

.breadcrumb a:hover::after {
  border-left-color: blue;
}
```

## Customize the design

- Change `darkcyan` to set the default breadcrumb color.
- Change `blue` to set the hover color.
- Adjust `height`, `line-height`, `padding`, and border widths to change the size.
- Update the link text and `href` values to match your site's hierarchy.

The complete example is in `index.html` and `breadcrumb.css`.

**pictures/project codeademy**
