# position : static vs relative vs absolute vs fixed vs sticky

| position | 특징                                                                                                                                                                    |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| static   | html 파일에 쓰여져있는 순서대로 배치<br />default position                                                                                                              |
| relative | 원래 위치해야하는 곳 기준으로 이동시켜서 배치                                                                                                                           |
| absolute | - static 속성을 가지고 있지 않은 조상을 기준으로 움직인다.<br />- 만약 조상 중에 포지션이 relative, absolute, fixed인 태그가 없다면 가장 위의 태그(body)가 기준이 된다. |
| fixed    | 윈도우 창 기준으로 움직이고, 스크롤을 해도 그 위치가 유지가 된다.                                                                                                       |
| sticky   | 스크롤을 하지않으면 static 처럼 배치되지만 스크롤하면 fixed 처럼 배치된다.                                                                                              |
