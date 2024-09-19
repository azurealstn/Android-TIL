# 함수

- 하나의 목적을 수행하기 위해 설계된 코드의 집합
- 함수를 사용하는 이유는 코드의 중복을 줄이기 위해서
- 실제로 리팩토링을 하게 되면 private으로 함수를 만들어 숨기고, 호출해주기만 하면 되기 때문에 가독성이 훨씬 좋아진다.

## 리턴값이 없는 함수

```kotlin
fun printStudentInfo(name: String, age: Int) : Unit {
    println("My Name is " + name)
    println("My Age is " + age)
}

printStudentInfo("Mike", 29)
```

- 리턴값이 없는 함수는 코드처럼 `Unit`을 써준다. (생략도 가능하다.)

## 리턴값이 있는 함수

```kotlin
fun sum(num1:Int, num2:Int): Int {
    return num1 + num2
}

println(sum(2, 3))
```

- 리턴값이 있는 경우 함수 옆에 리턴 타입을 선언해준다.