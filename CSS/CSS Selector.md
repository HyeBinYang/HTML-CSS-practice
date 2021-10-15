# CSS Selector

## 1. 전체를 선택하는 CSS Selector

```CSS
* {
    margin: 0;
    padding: 0;
}
```

- `*` 로 표시하면 body 태그에 있는 모든 태그에 CSS가 적용된다.

<br/>

## 2. Tag Selector

```CSS
h1 {
    color: red;
}
```

- 태그 이름으로 표시하면 해당 태그에 있는 모든 태그에 CSS가 적용된다.

<br/>

## 3. ID Selector

```CSS
#idName {
    color: red;
}
```

- id 명으로 표시하면 해당 id를 갖고있는 태그에 CSS가 적용된다.

<br/>

## 4. Class Selector

```CSS
.className {
    color: red;
}
```

- class 명으로 표시하면 해당 class를 갖고있는 태그에 CSS가 적용된다.

<br/>
<br/>

## 5. Attribute (속성) Selector

- [속성] : 어떠한 속성을 가지고 있는 모든 태그(요소)

```CSS
[attr] {
    color: blue;
}
```

- [속성=값] : 속성값이 정확히 일치하는 태그, 대소문자 구분하지 않음

```CSS
/* attr="apple" 인 속성을 가진 태그에만 적용 */
[attr="apple"] {
    color: blue;
}
```

- [속성~=값] : 속성값을 공백으로 분리된 단어로 포함하는 모든 태그

```CSS
/* attr="apple banana" 또는 attr="apple tomato" 와 같이 공백으로 분리된 태그에만 적용 (attr="applebanana" 는 적용안됨)*/
[attr~="apple"] {
    color: blue;
}
```

- [속성|=값] : 속성값이 "apple" 이거나 "apple"로 시작하면서 `-` 문자가 바로 뒤에 따라붙는 모든 태그

```CSS
[attr|="apple"] {
    color: blue;
}
```

- [속성^=값] : 속성값이 "apple" 로 시작하는 모든 태그

```CSS
[attr^="apple"] {
    color: blue;
}
```

- [속성$=값] : 속성값이 "apple" 로 끝나는 모든 태그

```CSS
[attr$="apple"] {
    color: blue;
}
```

- [속성*=값] : 속성값이 "apple" 을 포함하는 모든 태그

```CSS
[attr*="apple"] {
    color: blue;
}
```
