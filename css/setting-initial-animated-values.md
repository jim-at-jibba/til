# Setting initial animated values

When animating elements, often you want tto start the animation with the animated properties reset. In the case below we want the `opacity` and `translateY` to be instantly set to 0 so there is not flash of content. We could set this on the element but if we are using this animation in a lot of places it is not practical. 

We can do this automatically with `animation-fill-mode: backwards`

```css
@keyframes moveInButton {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }

  100% {
    opacity: 1;
    transform: translate(0);
  }
}

.btn-animated {
  animation-name: moveInButton;
  animation-duration: 0.5s;
  animation-timing-function: ease-out;
  animation-delay: 0.75s;

  animation-fill-mode: backwards;
}

```
