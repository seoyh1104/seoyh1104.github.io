---
title: "[Git] 브랜치에서 작업 후 마스터로 병합하는 방법(Git merge)"
excerpt: "브랜치에서 작업한 내용을 마스터로 병합하는 과정과 Git 명령어 사용법을 설명합니다."
categories: Git
tag: [Git]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

## Git 및 Bitbucket
디자인, 퍼블리셔용 브랜치를 신규 생성하고, 담당자에게 작업 절차를 설명하였다.  
아래는 참고용 Git 코드 기반 설명이며, Bitbucket 웹 인터페이스에서 안내하였다.

### 브랜치에서 작업 후 마스터로 병합하는 방법
신규 생성한 브랜치명: `work_publisher`

1. 클론 작업  
프로젝트를 자신의 로컬에 클론한다.  
```
git clone git@bitbucket.org:프로젝트명.git
```

2. 클론된 디렉토리로 이동  
```
cd 디렉토리명
```

3. work_publisher 브랜치로 전환  
클론 후 기본적으로 master 브랜치에 있을 가능성이 높기에, work_publisher 브랜치로 전환하기 위해 아래 명령어를 입력한다.
```
git checkout work_publisher
```
이 명령어로 work_publisher 브랜치로 이동한 후 작업을 시작할 수 있다.

4. 작업 내용 수정 및 커밋  
필요한 작업을 완료한 후, 변경 사항을 저장하고 커밋한다.
```
git add .
git commit -m "작업 내용을 설명하는 메시지"
```

5. 변경 사항 푸시  
작업이 완료되면 work_publisher 브랜치에 변경 사항을 원격 저장소로 푸시한다.
```
git push origin work_publisher
```

6. work_publisher 브랜치를 master 브랜치로 병합  
작업이 완료되면 work_publisher 브랜치에서 master 브랜치로 병합할 수 있다.

- 6-1. 먼저 master 브랜치로 전환한다.
```
git checkout master
```

- 6-2. 그 다음 work_publisher 브랜치의 변경 사항을 master로 병합한다.
```
git merge work_publisher
```

- 6-3. 병합 후 원격 저장소에 푸시
병합 후 master 브랜치의 최신 상태를 원격 저장소에 푸시한다.
```
git push origin master
```

위 6번의 경우에는, 리뷰어가 진행하는 형식으로 작업자에게 5. 변경 사항 푸시 후 → Pull Request(PR)하는 방법까지를 안내하였다.  
(리뷰어가 PR을 검토한 후, 병합이 가능하면 `Merge` 버튼을 눌러 `master` 브랜치로 병합하는 형식)

