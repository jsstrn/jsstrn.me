---
title: "Set width in CSS without media queries"

tags: [css]
categories: [software engineering]
---

Let's say I'd like to set the `width` of an image to 20% of the viewport width.

```css
img {
  width: 20vw;
}
```

The problem now is that when we look at the website on mobile devices it appears way too small because the viewport is much smaller.

One solution might be to use media queries, but it's actually not necessary in this case. We can actually set the `min-width` to be a certain value so that it will not be any smaller.

```css
img {
  width: 20vw;
  min-width: 200px;
}
```

That's great! A simple solution without having to use media queries. In fact, there's a shorter way to represent this by using `max()` which takes the largest value of a list of values.

```css
img {
  width: max(20vw, 200px);
}
```

For instance, `max(100px, 200px, 300px)` will always yield `300px` since this is the largest. It becomes useful when using relative values like viewport width that can vary depending on the device.

## Reference

- [Flexible layouts without media queries](https://blog.logrocket.com/flexible-layouts-without-media-queries/)
- [`max()`](https://developer.mozilla.org/en-US/docs/Web/CSS/max()) – MDN
