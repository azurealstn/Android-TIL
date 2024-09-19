# 제어문

- 제어문이란 프로그램의 흐름을 제어하기 위해 사용하는 실행문이다.

## 반복문

```kotlin
// [+] Range Class
// IntRange, LongRange, CharRange
// 모두 클래스이다.
val numRange: IntRange = 1 .. 5
println(numRange.contains(3)) // true
println(numRange.contains(10)) // false

val charRange: CharRange = 'a' .. 'h'
println(charRange.contains('a')) // true
println(charRange.contains('i')) // false

// 1. For
for (i in numRange) {
    println(i)
}

for (i in 1 until 6) {
    println(i)
}

for (i in 5 downTo 1) {
    println(i)
}

for (i in 1 .. 10 step 2) {
    println(i)
}

// 2. While -> 조건을 먼저 체크한다.
var count = 1;
while (count < 5) {
    println("나무를 ${count}번 찍었습니다.")
    count++
}

// 2-1. do while -> do에 있는 코드가 먼저 실행되고 그 다음에 조건을 체크한다.
count = 1;
do {
    println("나무를 ${count}번 찍었습니다.")
    count++
} while (count < 5)
```

## 조건문

```kotlin
// 1. If
fun isPass(examScore: Int): Boolean {
    if (examScore >= 70) {
        return true
    } else {
        return false
    }
}

val examResult = isPass(80)
println("ExamResult: $examResult")

// 2. when
fun getGrade(score: Int): Char {
    when (score) {
        in 0..40 -> return 'D'
        in 41..70 -> return 'C'
        in 71..90 -> return 'B'
        in 91..100 -> return 'A'
        else -> return 'F'
    }
}

val myGrade = getGrade(95)
println(myGrade)
```