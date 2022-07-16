---
title: "개발 지원 도구"
layout : single
categories : certificate
toc : true
toc_label: "Table of Contents"
toc_icon: "bars"
toc_sticky: true
author_profile : false
tag : [정보처리기사]
sidebar :
    nav : "docs"
---

## 통합 개발 환경(IDE; Integrated Development Environment)
개발에 필요한 환경, 즉 편집기(Editor), 컴파일러(Compiler), 디버거(Debugger) 등의 다양한 툴을 하나의 인터페이스로 통합해 제공하는 것을 의미함
- 이클립스(Eclipse) … IBM
- 비주얼 스튜디오(Visual Studio) … Microsoft
- 엑스 코드(X Code) … Apple
- 안드로이드 스튜디오(Android Studio) … Google
- IDEA … JetBrains

## 빌드 자동화 도구
소스 코드를 소프트웨어로 변환하는 과정에 필요한 전처리(Preprocessing), 컴파일(Complie) 등의 작업들을 수행하는 소프트웨어

### Ant(Another Neat Tool)
- 아파치 소프트웨어 재단에서 개발한 소프트웨어
- 자바 프로젝트의 공식적인 빌드 자동화 도구
- XML 기반의 빌드 스크립트를 사용
- 정해진 규칙이나 표준이 없어 개발자가 모든 것을 정의
- 스크립트의 재사용이 어려움

### Maven
- 아파치 소프트웨어 재단에서 Ant의 대안으로 개발
- 규칙이나 표준이 존재해 예외 사항만 기록됨
- 컴파일과 빌드를 동시에 수행할 수 있음
- 의존성(Dependency)을 설정하여 라이브러리를 관리

### Gradle ★
- 기존의 Ant와 Maven을 보완해 개발된 빌드 자동화 도구
- 안드로이드 스튜디오(안드로이드 앱 개발)의 공식 빌드 도구
- Maven과 동일하게 의존성(Dependency) 활용
- 그루비(Groovy) 기반의 빌드 스크립트 사용
- 플러그인을 설정하면, JAVA, C/C++, Python 등의 언어도 빌드 가능
- 실행할 처리 명령들을 모아 태스크(Task)로 만든 후 태스크 단위로 실행
- 이전에 사용했던 태스크를 재사용하거나 다른 시스템의 태스크를 공유할 수 있는 빌드 캐시 기능 지원 → 빌드의 속도 향상

### Jenkins ★
- JAVA 기반의 오픈 소스 형태로 가장 많이 사용되는 빌드 자동화 도구
- 서블릿 컨테이너에서 실행되는 서버 기반 도구
- SVN, Git 등 대부분의 형상 관리 도구와 연동 가능
- 친숙한 Web GUI 제공
- 여러 대의 컴퓨터를 이용한 분산 빌드나 테스트 가능

## 기타 협업 도구(Groupware, 그룹웨어)
### 일정 관리 도구
- 구글 캘린더

### 프로젝트 관리 도구
- 트렐로(Trello), 지라(Jira)

### 정보 공유 및 커뮤니케이션 도구
- 슬랙(Slack), 잔디(Jandi), 태스크월드(Task world)

### 디자인 도구
- 스케치(Sketch), 제플린(Zeplin)

### 아이디어 공유 도구
- 에버노트(Evernote)

### 형상 관리 도구
- 깃허브(GitHub)