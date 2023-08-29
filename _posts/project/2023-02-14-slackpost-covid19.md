---
title: "[Python] Slack 코로나19 통계정보 알림앱(Bot) 제작"
excerpt: ""
categories: Project
tag: [Project]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

# 프로젝트 목적
코로나19 감염자 증가로 인해 사내 코로나 감염 및 재택근무 전환자가 발생되는 시점에서, 전사원에게 일일 코로나 정보를 공유하기 위한 개인 프로젝트

# 개요
사내 메신저인 Slack에 통지 채널을 생성하고, 통계정보 BOT을 제작했습니다.
매일 오전 OpenAPI 기반 데이터를 취득하여 차트를 생성하고 해당 채널에 통지하도록 자동화 알림 앱을 구축했습니다.

## 아이디어
공공데이터 활용지원 센터의 보건복지부 코로나 19 API가 폐기됨에 따라 기존 작성한 스크립트를 전면 수정하고 대체 OpenAPI를 활용하여 스크립트를 작성했습니다.  
![images](/images/project/2023-02-14-slackpost-covid19/covid19_1.png)

## 구성
- 아이템 선정 및 팀빌딩 : 개인 프로젝트
- OpenAPI 상세 정보
  - [보건복지부_코로나19 시도 발생현황](https://www.data.go.kr/data/15098776/openapi.do){:target="_blank"}
  - 코로나19 시도 발생현황에 대한 데이터로 시도*별 코로나19 확진자, 격리현황 등 발생현황 정보 조회 기능을 제공합니다.
  - 17개 광역단위 기준 (서울, 부산, 대구, 인천, 광주, 대전, 울산, 세종, 경기, 강원, 충북, 충남, 전북, 전남, 경북, 경남, 제주)
  - 데이터 출처: [질병관리청(코로나바이러스감염증-19 홈페이지)](https://ncov.kdca.go.kr/){:target="_blank"}
  - 2023년 6월 1일~: 중앙재난안전대책본부(질병관리청)의 코로나19 위기단계 하향 및 방역 조치 전환 결정에 따라 '부터는 코로나19 시도 발생현황 데이터 업데이트가 주 단위로 전환되었습니다.

## 사용 기술 및 도구
기술 선정
- 개발언어 및 프레임워크: Python
- UI: [Slack block-kit-builder](https://app.slack.com/block-kit-builder){:target="_blank"}를 활용하여 구성
- 차트 생성: : Open Source Chart Image API [QuickChart](https://quickchart.io/documentation/reference/line-style){:target="_blank"} 활용
- 자동화: 작업 스케줄러 설정(Windows Task Scheduler python script)

## 기능구조
Slack 한국covid19정보 채널에 코로나19 통계정보를 전송하는 앱
![images](/images/project/2023-02-14-slackpost-covid19/covid19_5.png)

## UI/기능
언어 국제화
- 한국어  
![images](/images/project/2023-02-14-slackpost-covid19/covid19_3.png)
- 영어  
![images](/images/project/2023-02-14-slackpost-covid19/covid19_2.png)
- 일본어  
![images](/images/project/2023-02-14-slackpost-covid19/covid19_4.png)