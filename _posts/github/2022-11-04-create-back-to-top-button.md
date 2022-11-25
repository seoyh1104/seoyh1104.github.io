---
title: "[Github Blog] 블로그 맨 위로 가기(Go to top) 버튼 만들기"
layout: single
categories: Github
tag: [Github]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

# Create Back to Top Button
Jekyll과 같은 정적 웹사이트에서도 잘 작동하는 [🔗vanilla-back-to-top](https://github.com/vfeskov/vanilla-back-to-top){:target="_blank"}을 적용해보자

## ⚙️ 설치 방법
자신의 github.io의 repository 위치에서 cmd 터미널에 아래 명령어를 입력하여 해당 라이브러리를 설치한다.

```
npm i vanilla-back-to-top
```

## 📑 사용법
### 📃 default.html 추가
`_layouts/default.html`의 `<body>` 안에 다음을 추가한다.

```html
<script src="https://unpkg.com/vanilla-back-to-top@7.2.1/dist/vanilla-back-to-top.min.js"></script>
<script>addBackToTop({
  diameter: 56,
  backgroundColor: 'rgb(242, 19, 104)',
  textColor: '#fff'
})</script>
```

## ✨ 적용 완료

### git commit history
- [commit f3fdac6](https://github.com/seoyh1104/seoyh1104.github.io/commit/f3fdac6){:target="_blank"}

## 기타 : 간단한 RGB 추출 방법
참고로 버튼의 색상을 정하기 위해 간단하게 그림판의 색 선택 도구를 이용하여 색상을 추출하는 방법으로 위 버튼의 `backgroundColor`를 적용했다.

### RGB (Paint)
![images](/images/2022-11-04-create-back-to-top-button/rgb.png)

### RGB (Excel)
16진수의 육각 RGB 값이 필요할 때 Excel을 활용하여 값을 알아낼 수 있다.
![images](/images/2022-11-04-create-back-to-top-button/rgb-excel.png)

### RGB (Naver)
네이버에서도 '색상 팔레트'를 검색하면 색상 코드를 입력하여 16진수의 RGB값 조회가 가능하다.
![images](/images/2022-11-04-create-back-to-top-button/rgb-naver.png)