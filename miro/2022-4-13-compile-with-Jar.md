---
layout: single
title: Jar 파일 include 해서 컴파일 하는 법 (console에서)
date: 2022-4-13
tag: java
---

결론: 윈도우 개발 환경에서 -cp 가 제대로 안되는가 싶다. 나중에 리눅스 환경 생기면 해보자..

## User.java
```
public class User {
    private String name;
    int idx;
}
```

## Main.java
```
public class Main {

    public static void main(String[] args) {

        User user = new User();
        System.out.println(user);
    }
}
```

~/User/User.java
~/Main/Main.java

## User 컴파일 및 Jar 파일 생성
javac User.java
jar cf User.jar User.class

User.jar 파일이 만들어졌다 Main 폴더로 복사

## Main 컴파일
javac Main.java

User symbol을 못 찾겠다는 컴파일 에러 발생

javac -cp User.jar Main.java
cp로 classpath를 넣어주니 컴파일 성공 한다.

## 실행
java Main 

에러가 나온다
Exception in thread "main" java.lang.NoClassDefFoundError: User 
at Main.main (Main.java:5) 

User class 못 찾는 다는 내용으로 보여서 컴파일 때 처럼
classpath 을 넣어 주면 될것으로 생각 해서

java -cp User.jar Main
Error: Could not find or load main class Main 

여기서 막혔다..


## Stackoverflow 에...

(올린 질문 글)[https://stackoverflow.com/questions/71861212/import-jar-file-into-my-hello-world-console-application]

(Jar 파일 include 방법)[https://stackoverflow.com/questions/9395207/how-to-include-jar-files-with-java-file-and-compile-in-command-prompt#comment11870389_9395207]

나의 윈도우 개발 환경에서 -cp 에 멀 넣어도 안된다.
