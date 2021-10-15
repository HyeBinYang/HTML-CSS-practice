# CSS 크기 단위

1. px

   - 픽셀 단위 디스플레이 해상도에 따라 상대적인 크기를 가진다.

2. % (퍼센트)
   - `부모 태그`의 크기 기준으로 백분율 단위의 상대 단위이다.
3. em
   - `부모 태그`의 크기 기준으로 배수로 계산된 크기를 가진다.
   - 만약 부모의 크기가 32px이면, 2em 값은 64px이 된다.
4. rem
   - `루트 태그(html 태그)`의 크기 기준으로 배수로 계산된 크기를 가진다.
   - 만약 부모의 크기가 32px이고 루트의 크기가 16px이면, 2rem 값은 32px이 된다.

<br />

## Viewport (브라우저에서 웹페이지가 표시되는 영역) 단위

1. vw : viewport 너비의 1/100 (1%)
2. vh : viewport 높이의 1/100 (1%)
3. vmin : viewport 너비 또는 높이 중 작은 값의 1/100 (1%)
4. vmax : viewport 너비 또는 높이 중 큰 값의 1/100 (1%)

<br />

## 색상 표현 단위

1. 색상 이름으로 표기하는 방법 : [참고]("https://www.w3schools.com/colors/colors_names.asp)
2. 16 진수 표기 방법 : #RRGGBB
3. RGB 표기 방법 : rgb(0 ~ 255, 0 ~ 255, 0 ~ 255)
4. RGBA (투명도(alpha) 추가) : rgba(0 ~ 255, 0 ~ 255, 0 ~ 255, 0 ~ 1)
   - 투명도 값은 0.0 이 완전 투명, 1.0이 완전 불투명 이다. (크기가 작을수록 투명해짐)

> 색상 고를 때 꿀 사이트 <br /> <br /> [Google Material Design](https://material.io/design/color/the-color-system.html#tools-for-picking-colors) <br /> <br /> [Adobe Color](https://color.adobe.com/)

<br />

### RGBA vs opacity

- opacity 프로퍼티는 자식 요소에 투명도 값이 상속된다.
- rgba는 상속되지 않는다.
