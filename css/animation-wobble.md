# Stopping animation wobble

At the end of some css animations there is a slight shift up. No one really knows why it happens but it can be fixed with:

```css
.parent-element-animation {
  backface-visibility: hidden;
}
```
