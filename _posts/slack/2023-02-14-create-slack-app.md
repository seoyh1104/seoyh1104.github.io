---
title: "[Slack] Slack App(Bot) 생성하기"
excerpt: ""
categories: Slack
tag: [Slack]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

# Slack App 생성
1. [Slack api](https://api.slack.com/apps){:target="_blank"} 사이트로 이동하여 [Create an App] 버튼을 클릭합니다.

2. 활성화 된 팝업창에서 [From scratch]를 클릭합니다.

3. 앱 이름을 작성하고, 슬랙 작업 환경을 선택한 후에 [Create App]을 클릭합니다.

4. [Bots] 를 클릭합니다.


## 앱 관련 권한(Scope) 설정하기
1. [Review Scopes to Add]를 클릭합니다.
- Install App to Workspace는 생성한 App을 Slack 작업 환경에 설치 하는 버튼입니다. 현재 버튼이 비활성화되어 있는데, 권한(Scope) 설정을 마친 후에 활성화됩니다.
- 스크롤을 내리면 Scopes를 설정하는 부분이 나타납니다. Bot Token Scopes 부분에 있는 [Add an OAuth Scope] 버튼을 클릭하여 관련 권한을 설정하면 됩니다.
2. [Add an OAuth Scope] 버튼을 클릭하여 위 메소드들을 이용하기 위해 필요한 Scope들을 모두 등록합니다. 

3. 아래 간단한 예제를 수행하기 위해 메시지를 등록하는 `chat.postMessage` 메소드를 등록 하겠습니다.
- | 메소드명         | 기능        | 필요권한 (Scopes) |
| :--------------- | :---------- | :---------------- |
| chat.postMessage | 메시지 등록 | chat:write        |
- Slack API Methods 사이트에서 각 메소드의 필요권한을 확인할 수 있습니다.

4. Scopes 설정이 완료되면 [Install App to Workspace]를 클릭합니다.

5. Slack에 생성한 App을 게시합니다. 게시 할 채널을 선택하고 [허용]을 클릭합니다.
- Token 문자열을 복사해둡니다. Python으로 Slack API 호출 시 해당 Token 정보가 필요합니다.
  - (주의! Token이 인터넷에 공개적으로 게시되면 해당 Token은 보안을 위해 영구적으로 비활성화 됩니다. Github에 올리거나 하실 때 유의하시기 바랍니다.)

## bot 앱을 채널에 추가하기

슬랙 워크스페이스의 좌측 앱에서 bot을 누르고 채널 상단의 bot을 클릭합니다. 팝업이 뜨면 ‘이 앱을 채널에 추가’를 눌러 원하는 채널을 선택하여 추가합니다.

### Create Slack Bots
> 봇의 사용자 이름 규칙
1. 전부 소문자여야 한다.
2. 21자를 넘을 수 없다.
3. 문자, 숫자, 마침표, 하이픈, 밑줄만 포함할 수 있다.