# 자료형

- 자료형을 사용하는 이유는 메모리를 효율적으로 사용하기 위해

## 자료형 종류

```kotlin
// 1. Numbers
// 1-1. Byte -> -128 ~ 127 (1Byte)
var mByte: Byte = 100
// 1-2. Short -> -2^15 ~ 2^15 - 1 (2Byte)
var mShort: Short = 1000
// 1-3. Int -2^31 ~ 2^31 - 1 (4Byte)
var mInt: Int = 1000000
// 1-4. Long -> -2^63 ~ 2^63 - 1 (8Byte)
var mLong: Long = 10000000000000L // 끝에 L을 붙여야 한다.

// 1-5. Float
var mFloat: Float = 1.5f // 끝에 f를 붙여야 한다.
// 1-6. Double
var mDouble: Double = 1.43544543

// 2. Character
var mChar: Char = 'B'

// 3. String
var mString: String = "Hello Kotlin!"

// 4. Boolean
var mFalse: Boolean = false
var mTrue: Boolean = true

// 5. Array
var mArray: Array<String> = arrayOf("Kotlin","Is","Fun")
println(mArray[0])
println(mArray.get(1))
println(mArray.size)
```

- `Int`와 `Long`, `Float`, `Double`, `Char`, `String`, `Boolean`은 타입 생략이 가능하다.
    - 이는 코틀린 언어가 변수 타입을 생략하면 알아서 타입을 추론한다.
- 반면에 `Byte`, `Short`, `Array`는 생략이 불가능하다.