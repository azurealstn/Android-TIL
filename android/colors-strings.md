# Colors & Strings

CSS에서 color 색상이나 font 사이즈를 하드코딩으로 넣을 수도 있지만 변수로 지정해서 넣을 수도 있었다. 안드로이드도 마찬가지로 변수처럼 정의해서 재활용할 수 있다.

#### res > values 폴더

```xml
<color name="btn_start">#673AB7</color>
<color name="btn_restart">#FFEB3B</color>
```

- 위와 같이 변수를 지정해둘 수 있다.

```xml
android:backgroundTint="@color/btn_start"
android:backgroundTint="@color/btn_restart"
```

- 실제 사용은 위와같이 사용할 수 있다.