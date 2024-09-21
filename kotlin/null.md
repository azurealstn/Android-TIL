# Null 처리

- null이란 값이 아직 없는(할당되지 않은) 상태를 말한다.
    - 참고로 javascript에서는 `undefined`라는 것이 있다.

## 예시

```kotlin
// Nullable vs Non-Nullable (Default)
val myName: String = "Mike"
//val myName: String = null; Compile Error!
println(myName.reversed())

// Nullable
//val nullableMyName:String? = null
//println(nullableMyName.reversed()) Compile Error!

val nullableMyName:String? = "Hello"
//println(nullableMyName.reversed()) Compile Error!
println(nullableMyName?.reversed())

// ?:
val nullStr:String? = null
val person = nullStr?.reversed() ?: "Anonymous"
println("Person $person")

// !!
println(nullStr!!.reversed()) // 이는 남용하지 않는 것이 좋다.
```

- nullable인 경우 null인 경우가 올 수도 있기 때문에 항상 compile error를 발생시킨다.
- 이처럼 compile error는 사전에 에러를 방지할 수 있기 때문에 실행시점인 runtime error보다 훨씬 안전하다.