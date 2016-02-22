# Add content with `::before` and `::after`

You can easily add content to specific elements by creating the pseudo-elements `::before` and `::after` with CSS.

## Example

An easy example: Quotation marks.

### HTML

```html
<q>Let's see</q>, he said, <q>the magic of CSS</q>.
```

The _HTML_ contains the [element for inline quotation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q), `<q>`.
There is no quotation marks; we add them via _CSS_.

### CSS

```css
q::before {
  content: "»";
}

q::after {
  content: "«";
}
```

This example uses [alternative German quotation marks](https://en.wikipedia.org/wiki/Quotation_mark#Summary_table_for_various_languages).

### Output

»Let's see«, he said, »the magic of CSS«.

## More information

- Mozilla Developer Network: [`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before) and [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)
