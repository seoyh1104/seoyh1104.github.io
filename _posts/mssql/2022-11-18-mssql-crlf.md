---
title: "[MSSQL] 개행문자 CRLF, CHAR(13) + CHAR(10)"
layout: single
categories: MSSQL
tag: [MSSQL]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
author_profile: false
---

# 개행문자
## CR(Carriage return)
커서를 맨 왼쪽으로 이동 = 시작위치로 복귀
- 표현식 : `\r`, `CHAR(13)`
- 아스키코드 : 13

## LF(Line feed)
커서를 한칸 아래로 이동 = 새로운 행 추가
- 표현식 : `\n`, `CHAR(10)`
- 아스키코드 : 10

# 실습
TEXT 변수 안의 문자열이 다음과 같을 때 
- 실행  
![images](/images/2022-11-18-mssql-crlf/crlf1.png)
- 결과  
![images](/images/2022-11-18-mssql-crlf/crlf3.png)

실제로 컴퓨터가 인식하는 문자로 Replace 해보면 아래와 같은 결과가 나온다.
- 실행  
![images](/images/2022-11-18-mssql-crlf/crlf4.png)
- 결과  
![images](/images/2022-11-18-mssql-crlf/crlf2.png)
  - `CHAR(13)CHAR(10)ABC - DEFCHAR(13)CHAR(10)GHI - JKLCHAR(13)CHAR(10)MNO - PQRCHAR(13)CHAR(10)`

## 소스 코드
```sql
DECLARE @TEXT NVARCHAR(100)

SET @TEXT = '
ABC - DEF
GHI - JKL
MNO - PQR
'

SET @TEXT = REPLACE(REPLACE(@TEXT, CHAR(13), 'CHAR(13)'), CHAR(10), 'CHAR(10)')

PRINT @TEXT
```

### 관련 포스트 링크
위 문자열에서 -(하이픈)을 기준으로 행 분리하기
- [[MSSQL] 문자열 파싱 STRING_SPLIT 함수, 구분자로 행 분리](/mssql/mssql-string_split){:target="_blank"}