---
layout: single
title: 빌드 툴, 메이븐(Maven)와 그레이들(Gradle)
date: 2022-4-2 13:21:04
tag: java
---

## 빌드 관리 도구란
프로젝트에 필요한 xml, properties, jar 파일들을 자동으로 인식하여 빌드 해주는 도구
소스 코드를 컴파일, 테스트, 정적분석 등을 하여 실행 가능한 앱으로 빌드 해줌
프로젝트 정보 관리, 테스트 빌드, 배포 등의 작업을 진행해줌
외부 라이브러리를 참조하여 자동으로 다운로드 및 업데이트의 관리해줌

자바의 대표적인 빌드 도구: Ant, Maven, Gradle

## 메이븐 (Maven) 이란?
자바의 대표적인 관리 도구였던 Ant를 대체 하기 위해 개발됨
프로젝트의 외부 라이브러리를 쉽게 참조 할수 있게 pom.xml 파일로 명시하여 관리 (폼파일)
참조한 외부 라이브러리에 연관된 다른 라이브러리도 자동으로 관리됨

## 메이븐 (Maven)을 사용하는 이유
기존의 사용하던 Ant는 빌드의 기능만 가지고 있음
자동으로 라이브러리를 관리해주는 기능이 추가된 Maven을 사용
다운받아 사용하던 라이브러리에 변동 사항이 있으면 자동으로 업데이트 하여 적용됨

## Ant
+ XML 기반의 빌드 스크립트
+ 자유로운 빌드 단위 지정
+ 간단하고 사용하기 쉬움
+ 대규모 프로젝트에서 복잡해지는 경향이 있음
+ 라이프 사이클이 없음

## Maven
+ XML 기반의 빌드 스크립트
+ 라이프 사이클 도입
+ pom.xml로 편하게 Dependency 관리

## 메이븐(Maven) 간단 사용법
pom.xml 파일을 활용하여 빌드 및 관리
pom.xml 의 역할
modelVersion, groupId, artificatId, version, name, description, properties, dependendies, build
groupId : 통상 개발 사이트 도메인
properties : 빈번하게 사용하는 중복 상수를 정의
dependendies: 가장 중요, 해당 프로젝트의 의존성, 즉 어떤 라이브러리가 필요 한지 리스팅

## 메이븐(Maven) 실습, 예제
eclipse -> Lombok
https://mvnrepository.com/

## 그래들 (Gradle) 이란?
Groovy 스크립트를 활용한 빌드 관리 도구
안드로이드 프로젝트의 표준 빌드 시스템으로 채택
멀티 프로젝트(Multi-Project)의 빌드에 최적화 하여 설계됨
Maven에 비해 더 빠른 처리 숙도
Maven에 비해 더 간결한 구성

## 그래들 (Gradle)과 메이븐(Maven) 비교
Maven이 점유율이 더 높고 점차 Gradle이 올라가는 중
Gradle 성능이 더 좋고 특히 대규모 프로젝트
Maven: pom.xml  Gradle: build.gradle

## 그래들 대표 용어 
repositories: 라이브러리가 저장된 위치등 설정
mavenCentral: 기본 Maven Repository
dependencies: 라이브러리 사용을 위한 의존성 설정

## 대표 Repository Site
Maven Repository: https://mvnrepository.com

<hr/>
출처1: <https://www.youtube.com/watch?v=3Jp9kGDb01g>
출처2: <https://www.youtube.com/channel/UCLxPNvxa9D-3UIdocAJUxfQ>
레퍼런스: <https://kwonnam.pe.kr/wiki/gradle>
