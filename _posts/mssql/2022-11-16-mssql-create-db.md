---
title: "[MSSQL] 데이터베이스(DB) 생성하기"
layout: single
categories: MSSQL
tag: [MSSQL]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
author_profile: false
---

# DB 생성하기
새로운 DB를 생성을 위해 연결된 서버의 **데이터베이스**를 우클릭하여 **새 데이터베이스**를 선택한 후 데이터베이스 이름을 입력하여 DB를 생성합니다.

- 새 데이터베이스 클릭  
![images](/images/2022-11-16-mssql-create-db/create-db1.png)

- 데이터베이스 이름 설정
![images](/images/2022-11-16-mssql-create-db/create-db2.png)

- DB생성 확인  
![images](/images/2022-11-16-mssql-create-db/create-db3.png)

# DB 접속권한 확인
- 보안 → 로그인 → 해당 유저 우클릭 후 **속성** 선택  
![images](/images/2022-11-16-mssql-create-db/create-db5.png)

로그인 속성의 사용자 매핑 페이지에서 이 로그인으로 매핑된 사용자를 확인할 수 있다.
- 이 로그인으로 매핑된 사용자
![images](/images/2022-11-16-mssql-create-db/create-db4.png)