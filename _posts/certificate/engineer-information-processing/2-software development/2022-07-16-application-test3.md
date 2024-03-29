---
title: "[정보처리기사] 개발 단계에 따른 애플리케이션 테스트"
layout: single
categories: Certificate
tag: [정보처리기사]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

- **단통시인**

## 단위 테스트(Unit Test)
- 코딩 직후 최소 단위인 **모듈이나 컴포넌트에 초점을 맞춰 테스트** 하는 것
- 사용자의 요구사항을 기반으로 한 기능성 테스트를 최우선으로 수행
- 명세 기반 테스트, 구조 기반 테스트 중 **주로 구조 기반 테스트를 시행**함

## 통합 테스트(Integration Test)
- 단위 테스트가 완료된 모듈들을 **결합**하여 하나의 시스템으로 완성시키는 과정에서의 테스트를 의미
- 모듈 간 또는 **통합된 컴포넌트** 간의 상호 작용 오류 검사
  - 빅뱅 테스트, 상향식 테스트(클러스터, Cluster/드라이버, Driver), 하향식 테스트(스텁, Stub)

## 시스템 테스트(System Test)
- 개발된 소프트웨어가 **컴퓨터 시스템에서 완벽하게 수행되는가**를 점검하는 테스트
- 실제 사용 환경과 유사하게 만든 테스트 환경에서 테스트 수행해야 함
- 기능적 요구사항(블랙박스 테스트), 비기능적 요구사항(화이트박스 테스트) 구분

## 인수 테스트(Acceptance Test) ★
- 개발한 소프트웨어가 **사용자의 요구사항을 충족하는지에 중점**을 두는 테스트
- 알파 테스트 : **통제된 환경**에서 **사용자가 개발자와 함께** 확인하면서 행하는 테스트 기법
- 베타 테스트 : **통제되지 않은 환경**에서 **여러 명의 사용자가 행하는** 테스트 기법
(게임 베타 테스터)