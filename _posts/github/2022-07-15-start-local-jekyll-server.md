---
title: "[Github Blog] Jekyll 로컬 서버 실행하기"
layout: single
categories: Github
tag: [Github, Jekyll]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

## Local server 실행
- `Start Command Prompt with Ruby` 또는 `cmd`를 실행합니다.
  ![images](/images/2022-07-15-start-local-jekyll-server/ruby.png)

## Ruby
1. 자신의 github.io 경로로 이동합니다.
```ruby
cd 경로
```

2. jekyll 서버 실행 명령어를 입력합니다.
```ruby
bundle exec jekyll serve
```

## 로컬 서버 연결
- 자신의 로컬 서버 주소로 연결
  - [http://localhost:4000/](http://localhost:4000/){:target="_blank"}

## 자동 시작 배치파일 만들기
매일 해당 경로까지 들어가서 `bundle exec jekyll serve`를 실행해 주는 것이 매우 귀찮았기 때문에  
배치 파일을 활용하여 클릭 한번으로 로컬 서버가 실행되도록 만들 수 있습니다.

아래 명령어를 메모장에 입력 후 확장자를 `bat`로 하여 저장하면 됩니다.

### cmd
```ruby
cd 경로
bundle exec jekyll serve
```

- `파일명.bat`
  ![images](/images/2022-07-15-start-local-jekyll-server/bat.png)