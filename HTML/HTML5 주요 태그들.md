# HTML5 주요 body 내의 태그

## 1. &lt;h1&gt; ~ &lt;h6&gt;

`제목`을 표시하는 태그, 태그마다 사이즈 차이가 존재함

> 현업에서는 웹브라우저 호환성을 위해, 태그에 표현 서식을 모두 삭제하고 CSS style을 별도로 적용한다.

<br/>

## 2. &lt;p&gt;

`문단`을 표시하는 태그

<br/>

## 3. &lt;a&gt;

`하이퍼링크`를 설정하는 태그

```html
<a href="https://www.naver.com" target="_blank">네이버</a>
```

| 속성   | 설명                 | 주요 값                                                                 |
| ------ | -------------------- | ----------------------------------------------------------------------- |
| href   | 하이퍼링크 URL       | URL, 전화번호(tel:010-9999-9999), 이메일(mailto:"이메일주소@gmail.com") |
| target | 링크된 URL 이동 방법 | \_self(default) : 현재 탭에 띄움<br />\_blank : 새로운 탭에 띄움        |

<br />

## 4. &lt;ol&gt;, &lt;ul&gt;, &lt;li&gt;

리스트 관련 태그로 모던 웹에서 많이 사용된다.

```html
<!-- 순서가 있는 리스트 -->
<ol>
  <!-- 리스트안에 있는 아이템 -->
  <li>사과</li>
  <li>바나나</li>
  <li>오렌지</li>
</ol>
<!-- 순서가 없는 리스트 -->
<ul>
  <!-- 리스트안에 있는 아이템 -->
  <li>아침</li>
  <li>점심</li>
  <li>저녁</li>
</ul>
```

<br />

## 5. &lt;img&gt;

이미지 삽입 태그

```html
<img src="images/image.png" alt="이미지에 대한 설명" />
```

| 속성 | 설명                    | 주요 값            |
| ---- | ----------------------- | ------------------ |
| src  | 이미지 파일 위치        | 이미지 파일 경로   |
| alt  | 이미지에 대한 대체 설명 | 이미지 대체 텍스트 |

> alt 는 웹접근성을 높이기 위해 반드시 적는 것이 좋다.

<br/>

## 6. &lt;div&gt;

- html 문서의 특정 부분을 지정하는데 사용
- 모던 웹에서 CSS 또는 javascript로 특정 부분을 제어할 때 사용

```html
<div></div>
```

<br />

## 7. &lt;table&gt;

```html
<table>
  <thead>
    <tr>
      <th>제목 1</th>
      <th>제목 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>내용1</td>
      <td>내용1</td>
    </tr>
    <tr>
      <td>내용2</td>
      <td>내용2</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>끝 부분</td>
    </tr>
  </tfoot>
</table>
```

**thead 나 tfoot 은 표에서 한 번만 나와야한다.**

- thead : 제목으로 구성된 열들을 가진 행을 표시
- th : 제목으로 구성된 각 열을 표시
- tbody : 표의 내용을 나타내는 행들을 표시
- tr : 표의 내용을 나타내는 각 행들을 표시
- td : 표의 내용을 나타내는 각 열들을 표시
- tfoot : 표의 마지막 행을 표시
  > thead, tbody, tfoot 은 html5에서 정의된 시맨틱 태그로 tr 과 td 로만 구성해도 문제는 없다.

<br />

```html
<table border="1" width="250" height="100">
  <tr>
    <td rowspan="2"></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td colspan="4"></td>
  </tr>
</table>
```

- colspan : `열` 방향으로 합칠 셀의 개수 `(자기자신 포함)`
- rowspan : `행` 방향으로 합칠 셀의 개수 `(자기자신 포함)`

<br />

## 8. &lt;form&gt;

사용자 입력을 받는 태그 `input 태그`와 같이 사욯함

<br/>

### 주요 속성

| 속성   | 설명                          | 주요 값                                                |
| ------ | ----------------------------- | ------------------------------------------------------ |
| action | 사용자 입력을 처리할 URL      | URL                                                    |
| method | HTTP method                   | post, get                                              |
| target | action에 기입된 URL 이동 방법 | \_self : 현재 탭으로 띄움<br/>\_blank : 새 탭으로 띄움 |

<br />

## 9. &lt;input&gt;

- 사용자 테이터를 입력받는 태그
- input 태그의 속성은 매우 많아서 필요할 때마다 [여기](https://www.w3schools.com/tags/tag_input.asp)를 참고한다.

```html
<form action="https://localhost:8080/login" method="get">
  <input type="text" name="userId" placeholder="아이디" />
  <input type="password" name="password" placeholder="비밀번호" />
</form>
```

## 10. Semantic Web

- 웹페이지 각 요소에 의미를 부여해서, `의미`와 `관련성`을 보다 진보된 검색 또는 서비스가 가능토록 하는 시도
- 각 테그들의 속성은 div 태그랑 차이가 없음
- 시멘틱 웹 태그로 구성하면 검색엔진에서 각 부분에 대해 잘 이해할 수 있음

<br />

| 태그    | 설명                                             |
| ------- | ------------------------------------------------ |
| header  | 헤더를 의미                                      |
| nav     | 네비게이션 바를 의미                             |
| aside   | 옆에 위치하는 부분을 의미                        |
| section | 본문의 여러 내용(article)를 포함하는 부분을 의미 |
| article | 본문의 주 내용이 들어가는 부분을 의미            |
| footer  | 하단부를 의미                                    |
