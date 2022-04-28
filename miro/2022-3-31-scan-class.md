---
layout: single
title: Scan class, 줄입력이 안될때..
date: 2022-03-31 13:21:04
tag: java
---

scan class 을 사용 해서 숫자, 문자열을 여러번 입력 받는 코드 짤때 주의 할 부분이 있다.

nextInteger() 호출 하고 nextLine() 호출 해줘야 된다.

nextInteger는 입력 버퍼에서 carriage return 바로 전까지만 입력 받아서 그렇단다.

버퍼에 carriage return 이 남아서 다음 입력 함수에 이게 영향을 준다. (바로 스킵 된다.)
