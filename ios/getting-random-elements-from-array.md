# Getting random elements from an array in Swift

There are often times when you need to get a random element from an array. In swift there are (at least) 2 easy ways to do this:

```swift
// 2 ways to get a random element
diceImageView1.image = diceArray.randomElement()
diceImageView2.image = diceArray[Int.random(in:0...5)]
```