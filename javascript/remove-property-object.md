# Remove an object property

```javascript
const writer = {
  name: "James Best",
  twitterHandle: "@jimgbest",
  platform: "jamesbest.tech",
  interests: "Security, Photography, Software",
};

const { twitterHandle, ...updatedWriter } = writer;
console.log(updatedWriter);
// {name: "James Best", platform: "jamesbest.tech", interests: "Security, Photography, Software"}
```
