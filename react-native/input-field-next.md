# How to select the next input field after pressing next on the keyboard

```javascript
import React, { useRef } from 'react'
...


const MyFormComponent = () => {

  const ref_input2 = useRef();
  const ref_input3 = useRef();

  return (
    <>
      <TextInput
        placeholder="Input1"
        autoFocus={true}
        returnKeyType="next"
        blurOnSubmit={false}
        onSubmitEditing={() => ref_input2.current.focus()}
      />
      <TextInput
        placeholder="Input2"
        returnKeyType="next"
        onSubmitEditing={() => ref_input3.current.focus()}
        ref={ref_input2}
      />
      <TextInput
        placeholder="Input3"
        ref={ref_input3}
      />
    </>
  )
}
```
