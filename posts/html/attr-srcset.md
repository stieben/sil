# Attribute `srcset`

_#html_ _#rwd_

```html
<img
     alt="Venice side street"
  srcset="venice-side-street-1.0.jpg,
          venice-side-street-1.5.jpg 1.5x,
          venice-side-street-2.0.jpg 2x,
          venice-side-street-3.0.jpg 3x"
     src="venice-side-street-1.0.jpg" <!-- fallback -->
/>
```

This will load the picture depending on the [device pixel ratio](../js/device-pixel-ratio.md).
Fractional ratios will result in loading the next higher image (2.25 ratio → 3x image).
And it reacts to zooming while the page is being viewed and will load the appropriate image asynchronously.
