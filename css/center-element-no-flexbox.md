# Centering element when flexbox is not available

There are times when we cant reach for flexbox for our layouts but still need to center an element on the screen.

```css
/* old fixed centering */
.popup {
  position: fixed;
  left: 50%;
  top: 50%;
  transform: translateX(-50%) translateY(-50%);
}

/* new fixed centering */
.popup {
  position: fixed;
  inset: 0;
  margin: auto
}
```

The `inset` property is short hand for setting the top,right,bottom and left properties [source](https://developer.mozilla.org/en-US/docs/Web/CSS/inset)

Tip [source](https://twitter.com/eladsc/status/1412364596543905794?s=20)
