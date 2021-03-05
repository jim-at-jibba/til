# Handle hover events in React

When it comes to React event handlers and onHover: 
**The onHover event handler does not exist in React**.


React has provided the following event handlers for detecting the hover state for an element:

- `onMouseEnter`
- `onMouseLeave`

## Example

```jsx
import React, { useState } from 'react';
import './App.css';

function App() {
  const [isShown, setIsShown] = useState(false);

  return (
    <div className="App">
      <button
        onMouseEnter={() => setIsShown(true)}
        onMouseLeave={() => setIsShown(false)}>
        Hover over me!
      </button>
      {isShown && (
        <div>
          I'll appear when you hover over the button.
        </div>
      )}
    </div>
  );
}

export default App;
```

[Source](https://upmostly.com/tutorials/react-onhover-event-handling-with-examples)
