---
title: "[정보처리기사] 데이터 입・출력"
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

## SQL(Structured Query Language)
- 1974년 IBM 연구소에서 개발한 SEQUEL에서 유래함
- 관계대수와 관계해석을 기초로 한 혼합 데이터 언어

### 데이터 정의어(DDL; Data Define Language)
- **도스테뷰인**
- DOMAIN(도메인), SCHEMA(스키마), TABLE(테이블), VIEW(뷰), INDEX(인덱스)를 정의하거나 변경 또는 삭제할 때 사용하는 언어

### 데이터 조작어(DML; Data Manipulation Language)
- SELECT(검색), INSERT(삽입), UPDATE(갱신), DELETE(삭제)로 저장된 데이터를 실질적으로 처리하는 데 사용하는 언어 

### 데이터 제어어(DCL; Data Control Language)
- 데이터의 무결성, 보안, 회복, 병행 제어 등을 정의하는 데 사용되는 언어

## 데이터 접속(Data Mapping) 
소프트웨어의 기능 구현을 위해 프로그래밍 코드와 데이터베이스의 데이터를 연결(Mapping)하는 것을 말함

### SQL Mapping
- 프로그래밍 코드 내 SQL을 직접 입력해 DBMS의 데이터에 접속하는 기술 ★
  - `JDBC`, `ODBC`, `MyBatis`

### ORM(Object-Relational Mapping)
- 객체(Object)와 관계형데이터베이스(RDB)의 데이터를 연결(Mapping)하는 기술 ★
  - `JPA`, `Hibernate`, `Django`


## 트랜잭션(Transaction) ★★
- 데이터베이스의 상태를 변환시키는 하나의 논리적 기능을 수행하기 위한 작업의 단위
- 한꺼번에 모두 수행되어야 할 일련의 연산들

### COMMIT
트랜잭션 처리가 정상적으로 종료되어 수행한 변경 내용을 DB에 반영하는 명령어

### ROLLBACK
트랜잭션 처리가 비정상으로 종료되어 DB의 길관성이 깨졌을 때 트랜잭션이 행한 모든 변경 작업을 취소하고 이전 상태로 되돌리는 연산

### SAVEPOINT(=CHECKPOINT)
트랜잭션 내에서 ROLLBACK할 위치인 저장점을 지정하는 명령어, 여러 개의 SAVEPOINT 지정 가능

## 원리와 특징
- **ACID**
- 원자성(**A**tomicity)	: 트랜잭션 연산을 데이터베이스 모두에 반영 또는 반영하지 말아야 함(All or Nothing)
- 일관성(**C**onsistency)	트랜잭션이 실행을 성공적으로 완료할 시 일관성 있는 데이터베이스 상태를 유지
- 독립성(**I**solation, 격리성)	: 둘 이상 트랜잭션 동시 실행 시 한 개의 트랜잭션만 접근이 가능하여 간섭 불가
- 영속성(**D**urability) : 성공적으로 완료된 트랜잭션 결과는 영구적으로 반영됨