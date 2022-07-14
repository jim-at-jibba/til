# Disable gestures in React Navigation v6

## Single route

```javascript
<AuthStack.Screen
   name="Login"
   component={Login}
   options={{gestureEnabled: false}}
/>
```

## Whole stack

```javascript
<AuthStack.Navigator screenOptions={{gestureEnabled: false}}>
  ...
</AuthStack.Navigator>
```
