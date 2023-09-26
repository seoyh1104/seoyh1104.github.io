---
title: "[Python] Slack 자동화창고 랙(Rack) 정보 통지앱(Bot) 제작"
excerpt: "물류 자동화창고 Rack 정보 통지 스크립트 작성, MSSQL 처리, Excel파일 생성 자동화, Slack 알림봇(Bot) 구축"
categories: Project
tag: [Project]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

# 프로젝트 목적
기존 반복업무에 대한 자동화 개선으로 업무 효율성 향상

# 개요
## 프로젝트 소요시간
24시간 (일상 업무 중, 시간 날 때마다 틈틈이 작성했기에 비정확..)

## 프로젝트로 인한 개선사항
- 시스템팀 작업 소요시간 : 1일 5분
- 입고보관팀 작업 소요시간 : 1일 5분으로, 총 하루 10분 소요 
  - 일주일 (10분 X 5일(영업일)= 50분) : 50분 소요
  - 한달 (50분 X 4주= 200분) : 3시간 20분 소요
  - 일년 (200분 X 12개월= 2,400분) : 40시간 소요

## 구성
- 아이템 선정 및 팀빌딩 : 개인 프로젝트, 팀의 기존 반복업무 개선

### 기존 방식
1. MS SQL 쿼리 실행
2. 실행된 SQL 결과 복사
3. 정해진 엑셀 포맷에 붙여넣기 및 필요데이터 재가공
4. 현장의 다른 장소(물류동 1F 사무실)로 프린터 연결 및 엑셀 리스트 출력
5. Slack 자동창고 오퍼레이션 채널의 담당자에게 통지

### 개선 방식
1. Slack 통지 자동화
- 자동창고 랙 정상화 대상 정보 전송
  - 영업일 월~금요일 오전 9시 자동 통지

## 프로젝트 사용기술 및 도구
- FRONT-END
  - Slack
- BACK-END
  - Python
- DB
  - MS SQL
- TOOLS
  - Slack
  - Visual Studio Code
  - Windows Task Scheduler


## 기능구조
### UI/기능
### 프로그램 주요기능
1. MS SQL Controller 클래스
- SQL connect, Execute query, Disconnect
- Read SQL query

2. Create File 클래스
- exists_dir 함수 : 폴더 존재 확인
- save_filepath 함수 : 폴더・파일명 패스 설정
- save_csv, csv_to_excel 함수 : 쿼리 결과를 csv → excel 파일로 저장
- save_excel 함수 : 엑셀 파일의 데이터 및 시트 상세 설정

1. Slack API 클래스
- set_data 함수 : 랙 정상화 대상 데이터 취득
- post_message 함수 : 랙 정상화 대상이 없을 때, Slack으로 메시지 전송
- post_files_upload 함수 : 대상이 있을 때, 리스트 및 엑셀 파일 전송

### 클래스 다이어그램 설계(Python)


### 소스코드 라인 수
- Cloc(Count Lines of Code) 사용

### View 설계

## 주요 코드 설명
- Main 함수
- MSSQLController 클래스
- CreateFile 클래스
- SlackAPI 클래스

## 프로젝트 이슈

## 시연 및 Q&A

# 코드리뷰
1. 코드 리뷰 PPT 자료 내용 보완
- 클래스 다이어그램 설계
  - 어떤 파일의 다이어그램인지 모르겠다.
  - 보완) 소제목에 Python 추가.
- 소스코드 라인 수
  - 어떤 모듈로 소스코드를 측정했는지 공유 요망
  - Cloc(Count Lines of Code, GitHub - AlDanial) 사용, 공유 완료

2. CreateFile 클래스 함수 분리
- 엑셀 라이브러리 분리
- 명칭과 기능이 안맞음(클래스 명이 CreateFile이기에 파일을 생성하는 기능만 응집해야함.)

3. 함수 명칭 변경
- SlackAPI 클래스의 Set Data 함수가 무엇을 하는 함수인지 모르겠다.
- CommonFunc 클래스의 remove_prefix 함수, Prefix라고 사용하지 않는다.
  - Path에서 파일명만 바로 가져오도록 변경

4. 소스코드 변경
- ① CreateFile클래스의 set_column_size() 함수 변경
  - **엑셀 각 열 명칭인 'A', 'B', 'C' 등을 사용하지 않고 변수명을 설정**하여 지정할 수 있는지.
- ② CreateFile클래스의 set_sheetdata() 함수 변경
  - 21번째 열: RANK를 삭제할 때, work_sheet.delete_cols(21)과 같이 21번째 열을 삭제하도록 되어있는데, 이 경우 열이 추가・삭제・변경될 경우 소스코드를 변경해야 하기에 변수명을 지정하여 삭제하도록 변경이 가능한지.

5. csv・excel File 저장 및 Slack 전송 부분의 로그 저장
- ① 파일을 저장하거나 Slack을 전송하는 부분이 현재 터미널 로그로만 표시되고 있음.
  - 따로 **로그파일을 보존**하도록 코드 추가할 것.(로그를 각각 처리해야함)
- ② csv 파일은 데이터만 빠르게 확인하는 용도로 실제 Slack으로 전송하지는 않음
  - **디버그 모드에서만 csv파일을 만들고, 실제 동작에서는 Excel 파일만을 생성하여 전송**하도록 하는 방법도 있음.

6. 랙정상화 대상이 대량으로 발생할 경우, 리스트가 100건, 1000건 표시되는지
- 3년간 주 15건 이상 발생됐던 적이 없어서 상정하지 않음
- **만약을 위해 대상이 20건 이상일 경우, 이후의 리스트를 생략하는 방법을 검토.**