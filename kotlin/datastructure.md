# 자료구조

- 프로그래밍에서 자료구조는 굉장히 중요하다.
- `Int`, `Double`과 같은 자료형을 단순 자료구조라 하고, `List`, `Set`, `Map`과 같은 자료형을 복합 자료구조라 한다.

# 컬렉션

- 컬렉션은 위에서 설명한 자료구조를 쉽게 사용할 수 있도록 제공하는 클래스이다.
- 또한 컬렉션은 CRUD가 가능한 `Mutable`과 읽기만 가능한 `Immutable`이 있다.

## List 컬렉션

```kotlin
// 1. List
val fruitList = listOf("Banana", "Apple", "Melon")
println("First fruit ${fruitList[0]}")
//fruitList[0] = "Strawberry" -> listOf는 Immutable List이다.

val mutableFruitList = mutableListOf("Banana", "Apple", "Melon")
println("First fruit ${mutableFruitList[0]}")
mutableFruitList[0] = "Strawberry"
println("First fruit ${mutableFruitList[0]}")

// iterable
mutableFruitList.forEach {
    fruit -> println(fruit)
}
```

- `listOf`: Immutable List이다.
- `mutableListOf`: Mutable List이다.

## Set 컬렉션

```kotlin
// 2. Set
// Immutable Set
val immutableSet = setOf(1, 1, 2, 2, 3, 3)
println(immutableSet) // 1, 2, 3

// Mutable Set
val mutableSet = mutableSetOf(1, 1, 2, 2, 3, 3)
println(mutableSet)
mutableSet.add(4)
println(mutableSet)
```

- `setOf`: Immutable Set
- `mutableSetOf`: Mutable Set

## Map 컬렉션

```kotlin
// 3. Map
// Immutable Map
val immutableMap = mapOf("name" to "Mike", "age" to 30)
println(immutableMap)
println(immutableMap["name"])
println(immutableMap["age"])
println(immutableMap.get("name"))
println(immutableMap.get("age"))
//immutableMap["name"] = "James" Compile Error!

// Mutable Map
val mutableMap = mutableMapOf("name" to "Mike", "age" to "30")
mutableMap["age"] = "30"
println(mutableMap)

mutableMap.put("hobby", "coding")
println(mutableMap)
mutableMap.remove("name")
println(mutableMap)
```

- `mapOf`: Immutable Map
- `mutableMapOf`: Mutable Map