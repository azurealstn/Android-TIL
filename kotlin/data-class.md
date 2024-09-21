# 데이터 클래스

- 데이터 클래스는 말 그대로 데이터를 전달하는데 목적이 있다.
- 즉, 데이터 클래스를 생성하면 데이터를 보관하게 된다.

## 문법

```kotlin
data class Memo(val title: String, val content: String)

val memo = Memo("오늘 할 일", "코틀린 공부하기")
println(memo.title)
println(memo.content)
```

- 반드시 주 생성자를 생성하여 정의된 속성이 하나 이상 있어야 한다.