---
title: "[MSSQL] 문자열 파싱 STRING_SPLIT 함수, 구분자로 행 분리"
layout: single
categories: MSSQL
tag: [MSSQL]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

# string_split 함수란?
MS-SQL의 내장함수로 SQL Server 2016 부터 STRING_SPLIT() 함수가 추가되어 컬럼 문자열의 구분자를 행으로 분리 할 수 있다.
- 문자열을 지정된 구분자 기준으로 나누어 다수의 record로 표시해 준다.
- C나 JAVA에서의 `split` 함수와 동일한 기능을 한다.
- 반환하는 단일 column 명은 `value`이다.

## 사용방법
STRING_SPLIT("문자열", "구분자")

## 예시
![images](/images/2022-11-21-mssql-string_split/string_split1.png)

## 소스코드
```sql
SELECT VALUE
FROM 
STRING_SPLIT('사과,배,포도,참외,키위,귤,바나나,오렌지', ',')
```

# 응용하기
![images](/images/2022-11-21-mssql-string_split/string_split2.png)

## 소스코드
```sql
DECLARE @TEXT NVARCHAR(100)

SET @TEXT = '
ABC - DEF
GHI - JKL
MNO - PQR
'

SET @TEXT = REPLACE(REPLACE(REPLACE(@TEXT, CHAR(13), '-'), CHAR(10), ''), ' ', '')

SELECT VALUE
FROM 
STRING_SPLIT(@TEXT, '-')
```

### 관련 포스트 링크
- [[MSSQL] 개행문자 CRLF, CHAR(13) + CHAR(10)](/mssql/mssql-crlf){:target="_blank"}