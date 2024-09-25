# 레이아웃(Layout)

| 레이아웃이란

레이아웃은 뷰 그룹의 일종으로 뷰를 배치하는 역할을 한다.

| 레이아웃 종류

![layout](./images/layout.png)

- **리니어(Linear)**: 수직방향(위->아래) 혹은 수평방향(왼쪽->오른쪽) 차례로 주어진 뷰를 정렬한다.
- **상대적(Relative)**: 말 그대로 다른 뷰들로부터 위치를 지정하거나 부모 레이아웃을 기준으로 위치를 정하는 등 상대 기준으로 정렬한다.
- **컨스트레인트(Contraint)**: 뷰 사이에 수평, 수직 방향의 제약을 주어 뷰들을 위치시킨다.
- **테이블(Table)**: 뷰를 행과 열로 구성하여 테이블 형태로 정렬한다.
- **프레임(Frame)**: 뷰들을 액자처럼 쌓는다. 여러 뷰들을 추가하더라도 가장 나중에 추가한 뷰가 가장 위에 위치하게 된다. (CSS의 index 속성과 비슷하다.) 레이아웃 내에 여러 뷰들을 배치시키는데에 적합하지 않고, 주로 화면에 표시될 하나의 뷰를 바꿔가며 표시하는데 적합하다.

## 리니어 레이아웃

리니어 레이아웃의 속성들을 알아보자.

| **orientation (필수 속성)**

orientation 속성은 세로 방향인지 가로 방향인지 결정하는 속성이다.

- vertical (수직)
- horizental (수평)

![linear-layout1.png](./images/linear-layout1.png)

| **layout_gravity**

layout_gravity 속성은 orientation 값이 수직 방향으로 정렬하는데, 수평 방향으로 뷰들을 조정하고 싶을 때 사용한다.

- orientation 값이 vertical일 때, 수평 방향으로 조정
- orientation 값이 horizental일 때, 수직 방향으로 조정

| **layout_weight**

layout_weight 속성은 각 뷰의 비중을 지정할 수 있다.

- weightSum: 리니어 레이아웃 속의 layout_weight을 다 더한 값
- layout_weight: 뷰들의 비중

![layout-weight](./images/layout-weight.png)

- 위 리니어 레이아웃의 속성값
    - orientation : horizontal
    - weightSum : 4
    - 레이아웃 속 각 버튼의 속성값
        - layout_weight : 각각 차례로 1,2,1
        - layout_width: 0dp (각 버튼의 속성에 더 이상 가로 크기를 명시적으로 지정해주지 않기 때문)

## 상대적 레이아웃

| 부모 레이아웃을 기준으로 배치할 때 사용할 수 있는 속성

![relative-layout1](./images/relative-layout1.png)

- 부모 레이아웃을 어떤 기준으로 배치할지 지정한다.
- 생략하면 항상 Left, Top을 기준으로 배치하게 된다.

| 뷰를 기준으로 배치할 때 사용할 수 있는 속성

![relative-layout2](./images/relative-layout2.png)

- 기준이 되는 뷰는 반드시 `id` 속성값이 있어야 한다.

<br>
<br>
<br>

## References

- [[2023 코틀린 강의 무료제공] 기초에서 수익 창출까지, 안드로이드 프로그래밍 A-Z](https://www.inflearn.com/course/%EC%8C%A9%EC%B4%88%EB%B3%B4-%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D-%EC%88%98%EC%9D%B5)