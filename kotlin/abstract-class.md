# 추상클래스

- 인스턴스화할 수 없다.
- 이유는 말 그대로 추상클래스로 상속만 가능하다.
- 즉, 추상클래스 내부에 메서드도 추상화하여 자식 클래스에서 구현하도록 한다.
- 이는 사용자에게 반드시 구현하도록 강제하는 것이다.

## 예시

```kotlin
abstract class Game {
    fun startGame() {
        println("Start Game!")
    }
    
    abstract fun printGameName() // 추상메서드는 구현하지 않는다!
}

class Overwatch: Game() {
    override fun printGameName() {
        println("This is Overwatch")
    }
}

val overwatch = Overwatch()
overwatch.startGame()
overwatch.printGameName()
```

- 추상메서드는 구현하지 않는다.
- 자식 클래스인 `Overwatch`는 추상메서드인 `printGameName` 메서드를 반드시 재정의하여 구현해야 한다.