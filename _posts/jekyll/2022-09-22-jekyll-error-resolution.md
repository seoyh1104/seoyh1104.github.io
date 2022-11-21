---
title: "[Github Blog] jekyll에러 Liquid Exception invalid byte sequence in UTF-8 해결방법"
layout: single
categories: Github
tag: [Github, Jekyll]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
author_profile: false
---

## 에러
### Ruby
```ruby
Liquid Exception: Liquid error (line 13): invalid byte sequence in UTF-8 in sitemap.xml
                    ------------------------------------------------
      Jekyll 4.2.2   Please append `--trace` to the `serve` command
                     for any additional information or backtrace.
                    ------------------------------------------------
Traceback (most recent call last):
C:/Ruby27-x64/lib/ruby/gems/2.7.0/gems/addressable-2.8.0/lib/addressable/uri.rb:480:in `gsub': invalid byte sequence in UTF-8 (ArgumentError)
```

## 해결방법
파일명이 영어로 되어있는지 확인한다.

### 문제점
내 경우 아래 위치의 pdf파일을 그대로 commit하여 파일명에 한글이 포함되어 있어 에러가 발생했다.
- 이전 : `/files/2022-08-11-open-api/오픈뱅킹-개발-테스트-안내.pdf`
- 변경 : `/files/2022-08-11-open-api/OpenBanking-Development-Test-Guide.pdf`


## 해결완료
- jekyll 실행
```ruby
bundle exec jekyll serve
```

- 에러가 표시되지 않으며 정상적으로 서버가 실행된다.
```ruby
 Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
      Regenerating: 1 file(s) changed at 2022-09-22 02:08:51
                    _posts/open-api/2022-08-11-open-api.md
       Jekyll Feed: Generating feed for posts
                    ...done in 5.2125325 seconds.
```