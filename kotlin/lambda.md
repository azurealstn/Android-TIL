# 람다 표현식

- 람다식은 마치 값처럼 다룰 수 있는 익명함수를 말한다.
- 익명함수는 함수에 이름이 없는 것을 말한다.

```kotlin
val sayHello = fun() { // 익명함수
    println("Hello!")
}
sayHello()
```

## 람다 문법

```kotlin
val squareNum1: (Int) -> (Int) = { num -> num * num }
println(squareNum1(10))

val squareNum2 = {num: Int -> num * num}
println(squareNum2(10))

val squareNum3: (Int) -> (Int) = {it * it}
println(squareNum3(10))
```

- `(Int) -> (Int)`: 왼쪽과 오른쪽 타입이 같아야 한다.
    - 왼쪽은 인수, 오른쪽은 반환 타입이다.
- `it` 키워드는 인수가 딱 하나인 경우에 사용가능하다.
- javascript 언어에 익숙하다면 그나마 squareNum2가 익숙할 것 같다.

```kotlin
fun invokeLambda(lambda: (Int) -> Boolean): Boolean {
    return lambda(5)
}

val falseValue = invokeLambda { num -> num == 10 }
println(falseValue)
val trueValue = invokeLambda { num -> num < 10 }
println(trueValue)
```

- 위 코드처럼 함수의 인수에 람다를 넣을 수도 있다.