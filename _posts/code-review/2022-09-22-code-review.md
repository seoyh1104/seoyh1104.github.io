---
title: "[Code Review] 쿠팡 벤더플렉스 로케이션 출력 자동화 소프트웨어 개발"
layout: single
categories: ['Code Review']
tag: [Code Review]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
author_profile: false
---

## 쿠팡 벤더플렉스 로케이션 출력 자동화 소프트웨어 개발
### 목적
### 배경
### 제한사항
### 기대효과 금액
- 작업시간(h)x시급(won)x연간가동일(247일) = 연간 얼마 절감
### 프로그램 로직
### 이벤트 리스트
1. 이벤트처리 함수 설명
2. 상태변수 설명(default ON)
3. 상수변수, 변수 설명

### 내가 한 코멘트
- 반복되는 기능에 관한 함수화 가능성
  - 현재 각 4개의 이벤트마다 셀 값 변경을 위한 시트보호 해제와 처리가 끝난 후 다시 시트보호 설정을 반복하여 진행
  - 시트보호 해제 기능, 시트보호 설정 기능을 함수화하여 적용할 수 있는지

### 배운점
1. i18n(국제화)
2. 다른 사람이 알아볼 수 있도록 자세한 설명 필요