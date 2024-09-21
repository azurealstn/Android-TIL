# lateinit

- var 키워드를 사용한다.
- 나중에 초기화한다해서 lateinit이다.
- nullable type과 같이 사용할 수 없다.
- 만약 나중에라도 초기화를 하지 않고 사용한다면 에러가 발생한다.
- Primitive Type은 사용할 수 없다.

```kotlin
val name = "mike"

// lateinit -> var
lateinit var lunch: String
lunch = "waffle"
println(lunch)
```

# lazy

- val 키워드를 사용한다.
- 할당할 값과 `{}` 안에 초기화할 구문들을 넣어준다.
- 재사용했을 때는 초기화 구문이 다시 실행되지 않고 할당한 값만 출력된다.

```kotlin
// lazy -> val
val lazyBear: String by lazy {
    println("Bear is comming!")
    "bear"
}

println("First try :::")
println(lazyBear)
println("Second try :::")
println(lazyBear)
```