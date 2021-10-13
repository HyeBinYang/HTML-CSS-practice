# HTML5의 기본 템플릿 코드에 대한 설명

## 1. DOCTYPE

```HTML
<!DOCTYPE html>
```

- `HTML 문서`임을 알려주는 특수한 태그
- 해당 문서를 브라우저가 다르게 렌더링 하지 않도록 하기 위해 사용해야함
- 항상 `최상단`에 사용해야함

<br/>

## 2. HTML

```html
<html lang="en"></html>
```

- `문서 범위 설정` 태그
- 해당 태그를 오픈한 후, 작성되어야한다.

| 속성 | 설명           | 주요 값                 |
| ---- | -------------- | ----------------------- |
| lang | 문서 언어 설정 | ko(한국어), en(영어) 등 |

<br />

## 3. HEAD, BODY

```html
<head></head>
<body></body>
```

- HTML 문서는 `<head>` 태그와 `<body>` 태그로 이루어져있다.
- head 태그 안에는 html 문서 전체를 대표하거나, html 문서 전체에서 필요한 데이터를 넣는다.
- head 태그 안에서 사용되는 주요 태그
  - title: `html 문서 제목`을 표시
  - meta: `html 문서 전체를 대표하는` 정보를 넣는데 사용

<br />

## 4. META

- html 문서에 대한 정보를 표시해줌

| 속성    | 설명                                | 주요 값                                          |
| ------- | ----------------------------------- | ------------------------------------------------ |
| charset | body 태그안에 있는 문자 인코딩 설정 | utf-8(유니코드), euc-kr(한국어) 등               |
| name    | 메타 정보 이름                      | author: 저자이름, description: HTML 문서 설명 등 |

### 주요 name 값

```html
<meta name="description" content="html 문서에 대한 설명, 구글 검색 엔진이 참고는 많이는 안한다고 알려져있다." />
<meta name="keywords" content="웹 페이지를 대표하는 검색어" />
<meta name="author" content="웹페이지 작성자" />
```

### 호환성 관련 태그

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
```

- 인터넷 익스플로러(IE) 에서 최신 표준 모드로 렌더링되도록 설정
- IE의 호환성 이슈로 기본적으로 html 문서에 포함시켜야 한다.

### 반응형 웹 관련 태그

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

#### viewpost(뷰포트) 란?

현재 브라우저 화면에 보여지고 있는 영역을 의미한다.

#### viewport 설정

| 속성          | 설명                             | 주요 값                                            |
| ------------- | -------------------------------- | -------------------------------------------------- |
| width         | 초기 뷰포트 너비                 | device-width(디바이스 너비) 또는 자연수(특정 너비) |
| user-scalable | 웹페이지 확대허용 여부           | no or yes(default)                                 |
| initial-scale | 디바이스 너비와 뷰포트 너비 비율 | 0.0 ~ 10.0 (주로 1.0을 많이 사용함)                |
| maximum-scale | 최대 확대 비율                   | 0.0 ~ 10.0 (주로 1.0을 많이 사용함)                |
| minimum-scale | 최소 확대 비율                   | 0.0 ~ 10.0 (주로 1.0을 많이 사용함)                |

<br />

## 5. LINK

```HTML
<link rel="stylesheet" href="style.css">
<link rel="icon" href="favicon.png">
```

- HTML 문서에 필요한 외부데이터를 가져오기 위해 사용
- 주로 CSS파일, 아이콘 파일을 불러오기 위해 사용

| 속성 | 설명                                    | 주요값                                     |
| ---- | --------------------------------------- | ------------------------------------------ |
| rel  | html 문서와 외부 데이터와의 관계를 표시 | stylesheet(CSS 파일), icon(아이콘 파일) 등 |
| href | 외부 데이터 파일 경로 지정              | 파일 경로                                  |

<br />

## 6. STYLE

CSS 코드를 html 문서 내에서 작성할 때 사용

```html
<style>
  p {
    font-size: 60px;
    color: red;
  }
</style>
```

<br />

## 7. SCRIPT

javascript 코드를 html 문서 내에서 작성할 때 사용

```html
<script src="js/main.js"></script>
```

| 속성 | 설명                 | 주요 값   |
| ---- | -------------------- | --------- |
| src  | javascript 파일 경로 | 파일 경로 |
