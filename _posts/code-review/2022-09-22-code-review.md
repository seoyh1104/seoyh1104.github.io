---
title: "[Code Review] 쿠팡 벤더플렉스 로케이션 출력 자동화 소프트웨어 개발"
excerpt: "로케이션 출력 자동화 소프트웨어 코드리뷰 기록"
categories: ['Code Review']
tag: [Code Review]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

# 로케이션 출력 자동화 소프트웨어 코드리뷰 기록
## 목적
쿠팡에서 관리하는 상품에 대해 바코드 스캔만으로 벤더플렉스 로케이션을 출력하는 자동화 소프트웨어를 자체적으로 개발
## 배경
1. 현장 물류팀에서 로케이션 조회 및 수기 표시에 많은 시간과 노력이 소요
2. 출고한 상품을 벤더플렉스 로케이션으로 이동할 때 로케이션의 정보가 표기된 출력물을 함께 발송하기를 요망 

## 제한사항
1. 벤더플렉스 로케이션은 현장의 사정에 의해 수시로 변경됨
2. 상품을 벤더플렉스 로케이션으로 이동할 때의 로케이션 정보가 필요
3. 기간시스템에 벤더플렉스 로케이션이 등록되어 있지 않음

## 기대효과 금액
- 작업시간(h)x시급(won)x연간가동일(247일) = 연간 ?원 절감

- 연간 9,880,000₩ 절감
  - 로케이션 조회시간 2.0h X 시급2만₩ X 연간가동일 247일

## 프로그램 로직
## 이벤트 리스트
1. 이벤트처리 함수 설명
2. 상태변수 설명(default ON)
3. 상수변수, 변수 설명

## 내가 한 코멘트
- 반복되는 기능에 관한 함수화 가능성
  - 현재 각 4개의 이벤트마다 셀 값 변경을 위한 시트보호 해제와 처리가 끝난 후 다시 시트보호 설정을 반복하여 진행
  - 시트보호 해제 기능, 시트보호 설정 기능을 함수화하여 적용할 수 있는지

## 배운점
1. i18n(국제화)
2. 다른 사람이 알아볼 수 있도록 자세한 설명 필요