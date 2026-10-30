# Checkout Page

This page is an example of a checkout form using semantic HTML. The elements
and attributes below make the content clearer to browsers, assistive
technologies, and users.

## `figure` and `figcaption`

Use `<figure>` for self-contained content such as a product image, illustration,
or diagram. Add a caption that belongs to that content with `<figcaption>`.

```html
<figure>
  <img src="sneaker_afb.jpg" alt="Sneaker" />
  <figcaption>Ultra-run 5000</figcaption>
</figure>
```

In this checkout, `<figure>` groups the image and product name. A caption is
optional; use one when the image needs additional context. The `alt` text is
still important: it describes the image to people who cannot see it.

## ARIA labels

`aria-labelledby` connects an element to a visible heading, giving the element
an accessible name. This helps assistive technologies such as screen readers
identify and navigate page sections.

```html
<section aria-labelledby="payment-heading">
  <h2 id="payment-heading">Payment Information</h2>
</section>
```

Prefer using an existing visible heading. `aria-label` can provide a name when
there is no visible text, but use it only when a suitable visible label is not
available. ARIA does not change the visual appearance and does not replace
regular HTML labels for form fields.

## `autocomplete`

`autocomplete` tells the browser what kind of information an input expects.
The browser can then offer previously saved information to help fill in the
form.

```html
<input autocomplete="cc-name" />
<input autocomplete="cc-number" />
<input autocomplete="cc-exp" />
<input autocomplete="cc-csc" />
```

These values identify the cardholder name, card number, expiration date, and
security code respectively. Use the value that matches the field. The browser
decides whether and how to show a suggestion.

## `inputmode="numeric"`

`inputmode` is a hint for the virtual keyboard on devices such as phones.
Setting `inputmode="numeric"` may show a numeric keyboard:

```html
<input type="text" inputmode="numeric" />
```

This attribute does not validate the input or change its type. It is useful for
values made of digits that should remain text, such as card numbers and CVV
codes. A card number, for example, may contain leading zeroes and is not a
number used for calculations. Use `required`, appropriate validation, and clear
error messages to check the input.