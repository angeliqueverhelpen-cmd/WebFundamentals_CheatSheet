## Css flex-basis property

The `flex-basis` CSS property sets the initial base size for a flex item before any other space is distributed according to other flex properties.

## `justify-content` Property

```
/* Items based at the center of the parent container: */div {  display: flex;  justify-content: center;}/* Items based at the upper-left side of the parent container: */div {  display: flex;  justify-content: flex-start;}
```

The CSS `justify-content` flexbox property defines how the browser distributes space between and around content items along the main-axis of their container. This is when the content items do not use all available space on the major-axis (horizontally).

`justify-content` can have the values of:

- `flex-start`
- `flex-end`
- `center`
- `space-between`
- `space-around`

## `flex-grow` Property

The CSS `flex-grow` property allows flex items to grow as the parent container increases in size horizontally. This property accepts numerical values and specifies how an element should grow relative to its sibling elements based on this value.

The default value for this property is `0`.

## Css flex-wrap property

The `flex-wrap` property specifies whether flex items should wrap or not. This applies to flex items only. Once you tell your container to `flex-wrap`, wrapping become a priority over shrinking. Flex items will only begin to wrap if their combined `flex-basis` value is `greater` than the current size of their flex container.

## `flex-direction` Property

The `flex-direction` CSS property specifies how flex items are placed in the flex container - either vertically or horizontally. This property also determines whether those flex items appear in order or in reverse order.

## `align-content` Property

The `align-content` property modifies the behavior of the flex-wrap property. It determines how to space rows from top to bottom (ie. along the cross axis). Multiple rows of items are needed for this property to take effect.

## CSS `display: inline-flex` property

```
.container{  display: inline-flex;}
```

The CSS `display: inline-flex` property sets an HTML element as an inline flex container which takes only the required space for the content. Any child elements that reside within the flex container are called flex items. Flex items change their size and location in response to the size and position of their parent container.

## CSS Flexbox

```
div {  display: flex;}
```

The CSS `display: flex` property sets an HTML element as a block level flex container which takes the full width of its parent container. Any child elements that reside within the flex container are called flex items.

Flex items change their size and location in response to the size and position of their parent container.

## `flex` Property

```
/* Three properties declared on three lines: */.first-flex-item {  flex-grow: 2;  flex-shrink: 1;   flex-basis: 150px;}/* Same three properties declared on one line: */.first-flex-item {  flex: 2 1 150px;}
```

The `flex` CSS property specifies how a flex item will grow or shrink so as to fit within the space available in its `flex` container. This is a shorthand property that declares the following properties in order on a single line:

- `flex-grow`
- `flex-shrink`
- `flex-basis`

## `flex-shrink` Property

 flex-shrink: 1; The value 1 indicates that the item should shrink. flex-shrink: 2; The value 2 indicates that the item should shrink twice than the element item-a.

The CSS `flex-shrink` property determines how an element should shrink as the parent container decreases in size horizontally. This property accepts a numerical value which specifies the ratios for the shrinkage of a flex item compared to its other sibling elements within its parent container.

The default value for this property is `1`.

## `align-items` Property

Controls how flex or grid items are aligned along the cross axis(perpendicular to the main axis)
