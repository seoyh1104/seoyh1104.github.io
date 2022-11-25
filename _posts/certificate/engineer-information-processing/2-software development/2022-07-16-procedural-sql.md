---
title: "[정보처리기사] 절차형 SQL"
layout: single
categories: Certificate
tag: [정보처리기사]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

## 개요
- C, JAVA 등의 프로그래밍 언어와 같이 연속적인 실행이나 분기, 반복 등의 제어가 가능한 SQL
- 일반적인 프로그래밍 언어에 비해 효율이 떨어짐
- 연속적인 작업들을 처리하는데 적합
- BEGIN ~ END 형식으로 작성되는 블록(Block) 구조로 기능별 모듈화 가능 

### 프로시저(Procedure)
호출을 통해 실행되어 미리 저장해 놓은 SQL 작업 수행, 처리 결과는 한 개 이상의 값 혹은 반환을 아예 하지 않음

### 트리거(Trigger)
입력, 갱신, 삭제 등의 이벤트가 발생할 때마다 관력 작업을 자동 수행

### 사용자 정의 함수
프로시저와 유사하게 SQL을 사용해 일련의 작업을 연속적으로 처리함, 종료 시 예약어 RETURN을 사용해 처리 결과를 단일값으로 반환


## 테스트와 디버깅
- 테스트 전 구문 오류(Syntax Error)나 참조 오류의 존재 여부 확인
- 오류 및 경고 메시지가 상세히 출력되지 않으므로 SHOW 명령어를 통해 내용 확인
- 실제로 데이터베이스에 변화를 줄 수 있는 삽입 및 변경 관련 SQL문을 주석으로 처리하고 디버깅 수행

## 쿼리 성능 최적화
- 데이터 입, 출력 애플리케이션의 성능 향상을 위해 SQL 코드를 최적화하는 것
- 성능 측정 도구 APM(Application Performance Management/Monitoring)을 사용해 최적화할 쿼리를 선정
- 최적화할 쿼리에 대해 옵티마이저(Optimizer)가 수립한 실행 계획을 검토하고 SQL 코드와 인덱스 재구성