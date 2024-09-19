# String Template

```kotlin
val price = 10000
val tax = 10

val originalPrice = "Original Price is $price"
val finalPrice = "The tax price is ${price + price * 10 / 100}"

println(originalPrice)
println(finalPrice)
```