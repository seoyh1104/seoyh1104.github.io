---
title: "미들웨어 솔루션 명세"
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

## 미들웨어(Middleware)란?
운영체제(OS)와 해당 운영체제에서 실행되는 응용 프로그램 사이에서 운영체제가 제공하는 서비스 이외의 추가적인 서비스를 제공하는 **소프트웨어**
- **디원메트 레객와**

### DB(Database)
- 클라이언트에서 원격의 데이터베이스와 연결하기 위한 미들웨어, **2-Tier 아키텍처**
  - `ODBC(마이크로소프트)`, `IDAPI(볼랜드)`, `Glue(오라클)`

### RPC(Remote Procedure Call, 원격 프로시저 호출)
- 응용 프로그램의 프로시저를 사용하여 **원격 프로시저를 로컬 프로시저처럼 호출**하는 미들웨어
  - `Entera(이큐브시스템스)`, `ONC/RPC(OSF)`

### MOM(Message Oriented Middleware, 메시지 지향 미들웨어) ★
- **메시지 기반**의 **비동기형 메시지를 전달**하는 방식의 미들웨어
  - `MQ(IBM)`, `Message Q(오라클)`, `JMS(JCP)`

### TP-Monitor(Transaction Processing Monitor, 트랜잭션 처리 모니터) ★
- **항공기나 철도 예약 업무** 등과 같은 온라인 트랜잭션 업무에서 트랜잭션을 처리 및 감시하는 미들웨어
- 사용자 수가 증가해도** 빠른 응답 속도를 유지**해야 하는 업무에 주로 사용됨

### Legacyware(레거시웨어)
- 기존 애플리케이션에 **새로운 업데이트된 기능을 덧붙이고자** 할 때 사용되는 미들웨어

### ORB(Object Request Broker, 객체 요청 브로커) ★
- 객체 지향 미들웨어로 **코바(CORBA)** 표준 스펙을 구현한 미들웨어
  - 코바(CORBA, Common Object Request Broker Architecture) : 네트워크에서 분산 프로그램 객체를 생성, 배포, 관리하기 위한 규격을 의미
- 최근에는 TP-Monitor의 장점인 트랜잭션 처리와 모니터링 등을 추가로 구현한 제품도 있음
  - `CORBA(OMG)`, `Orbix(Micro Focus)`

### WAS(Web Application Server, 앱 애플리케이션 서버)
- 사용자의 요구에 따라 변하는 **동적인 콘텐츠를 처리**하기 위해 사용되는 미들웨어
  - Cf) 웹 서버(Web Server) : 클라이언트로부터 직접 요청을 받아 처리, 저용량의 **정적인 콘텐츠**(파일)들을 처리/제공하는 소프트웨어
- 클라이언트/서버 환경보다는 **웹 환경을 구현**하기 위한 미들웨어
- HTTP 세션 처리를 위한 웹 서버 기능뿐만 아니라 미션-크리티컬한 기업 업무까지 JAVA, EJB 컴포넌트 기반으로 구현 가능
  - `Web Logic(오라클)`, `WebSphere(IBM)`, `JEUS`, `Tomcat`