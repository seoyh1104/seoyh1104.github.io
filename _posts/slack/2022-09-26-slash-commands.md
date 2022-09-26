---
title: "[Slack] Slash Commands 슬래시 커맨드 만들기"
layout : single
toc : false
toc_label: "Table of Contents"
toc_icon: "bars"
toc_sticky: true
author_profile : false
categories : Slack
tag : [Slack]
sidebar :
    nav : "docs"
---

## 슬래시 커맨드 만들기
1. 슬래시 커맨드 생성
아래의 yourTeam 부분에 본인의 워크스페이스 URL을 입력하면 슬래시 커맨드 생성 페이지로 바로 이동할 수 있다.
- Ex) https://**yourTeam**.slack.com/apps/build/custom-integration
- Ex) https://seoyuhui.slack.com/apps/build/custom-integration
  - Slash Commands를 클릭한다.
  ![images](/images/2022-09-26-slash-commands/slash-commands1.png)

2. 사용할 명령어를 입력한다.
![images](/images/2022-09-26-slash-commands/slash-commands2.png)

3. 발신 페이로드 및 응답
![images](/images/2022-09-26-slash-commands/slash-commands3.png)

4. Request URL 입력
- 명령어를 처리 받아서 응답값을 줄 수 있는 API 및 서버가 있다면 Request URL에 해당 값 입력
- 없다면 일단 로컬주소`http://localhost`를 등록하여 슬래시 커맨드를 추가한다. 

5. Slack에서 `/`를 입력하여 테스트  
  ![images](/images/2022-09-26-slash-commands/slash-commands4.png)