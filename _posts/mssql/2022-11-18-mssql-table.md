---
title: "[MSSQL] 테이블 생성 및 삭제, 테이블 명 변경 CREATE TABLE・DROP TABLE, SP_RENAME"
layout: single
categories: MSSQL
tag: [MSSQL]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

## 테이블 생성
CREATE TABLE
```sql
CREATE TABLE dbo.Service_tb
(
    WRITER           NVARCHAR(20) NOT NULL,
    WRITING_DATETIME DATETIME2(7) NOT NULL,
    EDITOR           NVARCHAR(20) NOT NULL,
    EDITING_DATETIME DATETIME2(7) NOT NULL,
    PROGRAM          NVARCHAR(20) NOT NULL,
    IP               NVARCHAR(30) NOT NULL,
    SERVICE          NVARCHAR(30) NOT NULL,
    DOMAIN           NVARCHAR(20) NOT NULL -- PRIMARY KEY
    CONSTRAINT PK_DOMAIN PRIMARY KEY (DOMAIN) -- PK명 지정하여 생성
)
GO
```

## 테이블 삭제
DROP TABLE [테이블명]
```sql
DROP TABLE LocalDB.dbo.separate_tb​
```

## 테이블 명 변경
SP_RENAME [기존 테이블명], [변경할 테이블명]
```sql
SP_RENAME 'service', 'Service_tb'
```