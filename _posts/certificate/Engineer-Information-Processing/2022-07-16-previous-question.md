---
title: "정보처리기사 필기 기출문제 정리"
layout : single
categories : certificate
toc : true
toc_label: "Table of Contents"
toc_icon: "bars"
toc_sticky: true
author_profile : false
tag : [Engineer Information Processing, certificate, 정보처리기사]
sidebar :
    nav : "docs"
---

## 소프트웨어 아키텍처 관련
1. 파이프 필터 형태의 소프트웨어 아키텍처에 대한 설명으로 옳은 것은? (2020년09월26일 기출문제)
- ① 노드와 간선으로 구성된다.
- **② 서브시스템이 입력데이터를 받아 처리하고 결과를 다음 서브시스템으로 넘겨주는 과정을 반복한다.**
- ③ 계층 모델이라고도 한다. **→ 레이어 패턴(Layers Pattern)**
- ④ 3개의 서브시스템(모델, 뷰, 제어)으로 구성되어 있다. **→ MVC Pattern**
- 해설 (소프트웨어 아키텍처 = 소프트웨어 구조)
  - 레이어 패턴(Layers Pattern) : 시스템을 계층으로 구분하여 구성, Ex) OSI 참조 모델
  - 클라이언트-서버 패턴(Client-Server Pattern) : 하나의 서버 컴포넌트와 다수의 클라이언트 컴포넌트로 구성되는 패턴
  - 파이프-필터 패턴(Pipe-Filter Pattern) : 데이터 스트림 절차의 각 단계를 필터 컴포넌트로 캡슐화하여 파이프를 통해 데이터를 전송하는 패턴 Ex) UNIX의 쉘
  - 모델-뷰-컨트롤러 패턴(Model-View-Controller Pattern) : 서브시스템을 3개의 부분으로 구조화하는 패턴


## 객체지향 관련
1. 객체지향 분석 방법론 중 **Coad-Yourdon** 방법에 해당하는 것은? (2021년03월07일 기출문제)
- **① E-R 다이어그램을 사용하여 객체의 행위를 데이터 모델링하는데 초점을 둔 방법이다.**
- ② 객체, 동적, 기능 모델로 나누어 수행하는 방법이다.
- ③ 미시적 개발 프로세스와 거시적 개발 프로세스를 모두 사용하는 방법이다. **→ Booch(부치)**
- ④ Use-Case를 강조하여 사용하는 방법이다. **→ Jacobson(제이콥슨)**