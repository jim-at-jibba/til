# Disable React Native TextInput while maintaining editablity

In some situations there is a need to have an inputfield that is disabled but still editable. 
i.e when the input is populated by a modal

```
<TouchableOpacity onPress={this.openPinKeyboard}>
  <View pointerEvents="none">
    <Input editable={false} value="1234" />
  </View>
</TouchableOpacity>

```

[Source](https://stackoverflow.com/questions/51135278/how-to-disable-keyboard-in-react-native)
