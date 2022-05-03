---
layout: single
title: package 키워드 넣어 실행하기 (console에서)
date: 2022-4-14
tag: java
---

## package 키워드

```
package 패키지명;
```

아래 예제를 보면 
com.company.console 이 패키지 명이고 folder path 가 된다.

```
package com.company.console;

public class Main{
    public static class main(String[] args) {
        System.out.println("Hello World");
    } 
}
```

## 어떤 일을 하는가?
클래스 이름을 full name으로 변환 해 준다.
Main class 을 com.company.console.Main 로 변환 한다.
(javap 역 어셈블러 하면 변환 직접 확인 할수 있다.

# package 선언 안하면 
자바에서 기본적으로 제공 하는 곳에 한다.
'이름 없는 패키지' (unnamed package)라고 부른다.

# 컴파일
javac 파일 이름

'-d .' path에 폴더들을 만든다.

소스 파일 안에 import 있으면 경로 찾아 들어가 그 파일도 컴파일 하는 듯 하다.

# 콘솔에서 실행
이 부분에서 제일 헤맸는데..

full name을 넣어줘야 하고 실행 위치도 중요 하다.

파일 경로: c:\project\com\company\console\Main.java
컴파일을 > c:\project>java com.company.console.Main


