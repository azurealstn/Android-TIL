# 객체

- 서로 연관된 것을 묶어 만든 속성(필드)과 동작(메서드)이 있는 집합체

# 클래스

- 위에서 설명한 객체를 만들기 위한 설계도이다.
- 클래스를 가지고 객체를 만들게 되면 그것을 인스턴스화한다고 하고, 만든 객체를 인스턴스라고 한다. 그리고 이것을 실체가 있는 객체라 한다.

## 객체지향 프로그래밍의 장점

- 추상화: 공통성을 모아서 추출(추상화)할 수 있다.
- 상속: 부모 클래스의 기능을 재활용할 수 있다.
- 다형성: 어떤 객체의 속성이나 기능이 상황에 따라 여러가지 형태를 가질 수 있는 성질
    - 다형성의 가장 큰 장점은 유연성으로 구현체를 변경하기 용이하다.
- 캡슐화: 서로 연관있는 것들을 묶어서 외부로부터 보호
    - 적절한 제약이 있는 프로그램이 잘 만든 것이다.

## 클래스 생성, 생성자

```kotlin
class Car (val color: String)

val car = Car("Red") // 객체 생성
println(car.color)
```

- `car`: 객체 생성을 통해 만들어진 변수를 인스턴스라고 한다. 실제 참조값이 할당된다.
- `val color: String`: 클래스 이름 옆에 괄호로 둘러싸인 코드를 주 생성자라고 한다.

## Init

```kotlin
class Car (val color: String) {
    init {
        println("Init $color")
    }
}

val car = Car("Red") // 객체 생성
```

- 주 생성자 말고, 초기화 시에 필요한 작업을 하려는 경우에 사용한다.

## constructor

```kolin
class Car (val color: String, val name: String, val age: Int) {
    init {
        println("Color: $color Name: $name Age: $age")
    }

    constructor(color: String, name: String): this(color, name, 20)
}

val car1 = Car("Red", "Volvo", 12) // 주 생성자
val car2 = Car("Blue", "Tesla") // 보조 생성자
```

- 주 생성자를 보완할 수 있는 것이 보조 생성자이다.
- 주 생성자말고 여러 생성자를 생성하려고 할 때 사용한다.
- 보조 생성자를 사용할 경우 `this` 키워드를 사용하여 주 생성자에게 생성을 위임한다.