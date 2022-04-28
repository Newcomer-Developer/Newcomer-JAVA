---
layout: single
title: main 함수 있을때 Jar 파일 (console에서)
date: 2022-4-14
tag: java
---

## 방식1, manifest 써서
mainfest.mf 생성
Manifest-version: 1.0
Main-Class: Main
> 마지막 라인 후에 newline 있어야 한다

```
javac Main.java
jar cfm test.jar manifest.mf Main.class
java -jar test.jar
```

## 방식2, manifest 안쓰고 
```
javac Main.java User.java 
jar cfe user.jar Main  Main.class User.class
java -jar user.jar
```

## Jar 파일 확인 법
```
jar tf test.jar
```
