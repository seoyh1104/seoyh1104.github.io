---
title: "[Slack] Slash Commands 슬래시 커맨드 만들기"
excerpt: "슬래시 커맨드를 생성하고 테스트 앱에 적용해보자🙋‍♀️"
categories: Slack
tag: [Slack]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

## 슬래시 커맨드 만들기
1. 슬래시 커맨드 생성
아래의 yourTeam 부분에 본인의 워크스페이스 URL을 입력하면 슬래시 커맨드 생성 페이지로 바로 이동할 수 있다.
- Ex) https://**yourTeam**.slack.com/apps/build/custom-integration
- Ex) https://seoyuhui.slack.com/apps/build/custom-integration
  ![images](/images/2022-09-26-slash-commands/slash-commands1.png)
  - Slash Commands를 클릭한다.

2. 사용할 명령어를 입력한다.
![images](/images/2022-09-26-slash-commands/slash-commands2.png)
- 명령어 입력 후 **슬래시 명령어 통합 추가**를 클릭

3. 발신 페이로드 및 응답
![images](/images/2022-09-26-slash-commands/slash-commands3.png)
- 발신 데이터
```
token=oOKilVzEyAJKi7s9r0N6HCeq
team_id=T0001
team_domain=example
channel_id=C2147483705
channel_name=test
user_id=U2147483697
user_name=Steve
command=/weather
text=94070
response_url=https://hooks.slack.com/commands/1234/5678
```

4. Request URL 입력
- 명령어를 처리 받아서 응답값을 줄 수 있는 API 및 서버가 있다면 Request URL에 해당 값 입력
- 없다면 일단 로컬주소`http://localhost`를 등록하여 슬래시 커맨드를 추가한다. 

5. Slack에서 명령어를 입력하여 테스트
- 위에서 설정한 명령어를 입력  
  ![images](/images/2022-09-26-slash-commands/slash-commands11.png)
- Slash Commands 수신 확인  
  ![images](/images/2022-09-26-slash-commands/slash-commands12.png)