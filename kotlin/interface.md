# 인터페이스

- 추상클래스보다 더 강제한 것이 인터페이스이다.
- 즉, 사용자는 인터페이스의 규격에 맞게 모두 구현해야 한다. (하나라도 어기면 안된다!)
- 또한 인터페이스는 그냥 상속과 달리 다중 상속이 가능하다.

## 문법

```kotlin
interface Vehicle {
    fun drive()

    fun stop()

    fun destroy() { // default method
        println("Vehicle is destroyed")
    }
}

class Car: Vehicle {
    override fun drive() {
        println("Car is Moving")
    }

    override fun stop() {
        println("Car is Stopping..")
    }
}

val car = Car()
car.drive()
car.stop()
car.destroy()
```