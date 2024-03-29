---
title: "[정보처리기사] 요구사항 확인"
layout: single
categories: Certificate
tag: [정보처리기사]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
use_math: true
---

# 요구사항
## 요구사항 개념
1. 요구공학(Requirements Engineering)의 개념
- 요구공학은 사용자의 요구가 반영된 시스템을 개발하기 위하여 사용자 요구사항에 대한 도출, 분석, 명세, 확인 및 검증하는 구조화된 활동이다.

2. 요구공학의 목적
- 이해관계자 사이에 효과적인 의사소통 수단을 제공하고 시스템 개발의 요구사항에 대한 공통된 이해를 설정한다.
- 요구사항 누락 방지 및 이해 오류로 인한 불필요한 비용을 절감하고 요구사항 변경 추적을 가능하게 한다.
- 초기 요구사항 관리로 개발 비용과 시간을 절약하고 효과적인 의사소통 수단을 제공한다.
- | 구분      | 기능적 요구사항   | 비기능적 요구사항   |
  | :-------- | :-------- ---- | :---------------- |
  | 개념      | 시스템이 제공하는 기능, 서비스에 대한 요구사항  | 시스템이 수행하는 기능 이외의 사항, 시스템 구축에 대한 제약사항에 관한 요구사항 |
  | 도출 방법 | 특정 입력에 대해 시스템이 어떻게 반응해야 하는지에 대한 기술 <br> 특정 상황에 대해 시스템이 어떻게 동작해야 하는지에 대한 기술 | 품질 속성에 관런하여   시스템이 갖춰야 할 사항에 관한 기술 <br> 시스템이 준수해야 할 제한 조건에 관한 기술 |
  | 특성      | 기능성, 완전성, 일관성 | 신뢰성, 사용성, 효율성, 유지보수성, 이식성 , 보안성 및 품질 관련 요구사항, 제약사항 |
  | 사례      | 온라인 홈페이지에서는 쇼핑카트에 주문하고자 하는 품목을 저장할 수 있는 장바구니 기능을 제공해야 함  <br> 상품의 결제수단은 신용카드, 무통장 입금,   포인트 결제가 가능해야 함 | 특정 함수의 호출시간은 3초를 넘지 않아야 함 <br> 시스템은 하루 24시간 가동되어야 하며 가동률 99.5％를 만족해야 함  <br> 시스템은   운영되는 중에 패치 및 업그레이드를 할 수 있어야 함 |

## 요구공학 프로세스
요구공학 프로세스는 요구사항 개발 단계와 요구사항 관리 단계로 구성된다.

1. 요구사항 개발 단계 구성(CMM Level 3 프로세스 영역) **도분명확**  
요구사항 개발은 요구사항 도출 , 분석 , 명세 , 확인 및 검증 단계로 구성되어 있다.
- 도출 : 이해관계자 식별, 고객 분석 
- 분석 : **분개할협분** 분류 → 개념 모델링 생성 → 할당 → 협상 → 분석 
- 명세 : 정형화된 형태로 명세 작성 
- 확인 : 요구사항 이해를 확인하고 문서가 완전한지 검증

2. 요구공학 관리 단계 구성(CMM Level 2 프로세스 영역) **협기변확**
- 협상 : 구현 가능한 기능 협상
- 기준선 설정 : 기준선(베이스라인) 설정
- 변경관리 :형상통제 위원회를 운영하여 변경 관리 
- 확인 및 검증 : 요구사항에 부합하는지 확인