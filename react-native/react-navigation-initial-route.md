# React Navigation - Initial Route

There are situations where you need to link to a screen that is deep in a stack. If you link directly
then you that screen maybe added to the top to the stack. To load the preceding screens, amke sure you set the `initial: false` property when navigating

```typescript
navigate(Screens.CrushStack, {
  screen: Screens.CrushSession,
  initial: false, // This is the important bit
  params: {
    session,
    backScreen: Screens.Home,
  },
});

```
