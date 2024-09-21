# Object & Companion Object

- 싱글톤 패턴은 클래스의 인스턴스가 오직 하나만 생성되는 것을 말한다.
- Object 문법을 사용하면 싱글톤 패턴처럼 사용할 수 있다.

```kotlin
object MyFirstObject {
    val number = 1;

    fun sayHello() {
        println("Hello!")
    }
}

println(MyFirstObject.number)
println(MyFirstObject.sayHello())
```

- Companion Object는 클래스 안에 정의된 Object이다.

```kotlin
object MyFirstObject {
    val number = 1;

    fun sayHello() {
        println("Hello!")
    }
}

println(MyFirstObject.number)
println(MyFirstObject.sayHello())
```