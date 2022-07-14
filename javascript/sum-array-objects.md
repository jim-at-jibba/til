# Sum an array of objects

Sometimes, you need to count the sum of property in an array of objects. For example, you may find an array of items, and you want to sum the total quantity a person must pay for the items:

```javascript
let cart = [
  {
    name: "JavaScript book",
    price: 4,
  },
  {
    name: "UGG Women's Hazel Ankle Boot",
    price: 79,
  },
  {
    name: "OXO Good Grips 11-Inch Balloon Whisk",
    price: 9,
  },
];

// When you want to sum the price of the items, you can use the reduce method of an array:
let totalPrice = cart.reduce(function (accumulator, item) {
  return accumulator + item.price;
}, 0);

```

When you call the reduce method on array of objects, you need to always specify the initial value to prevent reduce from using the first object as the initial value.

## Filter the array before reduce

Finally, you may want to filter the array to include only certain items from the cart. You can call the filter method before you call the reduce method.

Here’s how to sum only the first two objects by filtering the name values:

```javascript
let cart = [
  {
    name: "JavaScript book",
    quantity: 3,
    price: 4,
  },
  {
    name: "UGG Women's Hazel Ankle Boot",
    quantity: 2,
    price: 79,
  },
  {
    name: "OXO Good Grips 11-Inch Balloon Whisk",
    quantity: 5,
    price: 9,
  },
];

// totalPrice is 170

let totalPrice = cart
  .filter(
    (item) =>
      item.name === "JavaScript book" ||
      item.name === "UGG Women's Hazel Ankle Boot"
  )
  .reduce((accumulator, item) => {
    return accumulator + item.quantity * item.price;
  }, 0);
```

[Source](https://sebhastian.com/javascript-sum-array-objects/)
