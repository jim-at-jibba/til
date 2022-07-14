# Setting margin/padding based on index

Sometimes you have a button or pill group that you need to set margin/padding on different sides based on the position in the group

```typescript
const getButtonStyle: RadioButtonProps["buttonStyle"] = (index, selected) => {
    return {
      borderRadius: 4,
      borderWidth: 1,
      borderLeftWidth: 1,
      borderStyle: "solid",
      borderColor: colors.grey400,
      overflow: "hidden",
      ...(index === 0 ? { marginRight: 4 } : {}), // <- this
      ...(selected ? { borderColor: colors.yellow400 } : {}),
    };
  };
 ```
