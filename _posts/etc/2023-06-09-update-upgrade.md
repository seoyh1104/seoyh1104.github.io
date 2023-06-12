---
title: "[ETC] 업데이트 & 업그레이드 관련 기록"
excerpt: "리눅스(Linux) 우분투(Ubuntu) 및 도커(Docker), 윈도우 파워셸(Windows PowerShell) 업데이트 및 업그레이드(Update & Upgrade)"
categories: ETC
tag: [ETC]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

# 리눅스(Linux)
## 우분투(Ubuntu) 업데이트
1. 우분투 업데이트&업그레이드
```
sudo apt update -y && sudo apt full-upgrade -y && sudo apt autoremove -y && antigen update
```
![images](/images/2023-06-09-update/update1.png)

## 도커(Docker) 업데이트
1. Open in external terminal 클릭
![images](/images/2023-06-09-update/update2.png)

2. 디렉토리 경로 변경
```
cd ~
```
![images](/images/2023-06-09-update/update3.png)


2. zsh 실행
```
zsh
```
![images](/images/2023-06-09-update/update4.png)

3. 도커 업데이트&업그레이드
```
apt update -y && apt full-upgrade -y && apt autoremove -y && omz update
```
![images](/images/2023-06-09-update/update5.png)

# 윈도우(Windows)
## 파워셸(PowerShell) 업데이트
1. Windows PowerShell 관리자로 실행

2. 모듈 업데이트
```
Update-Module
```
![images](/images/2023-06-09-update/update6.png)

## 기타
- tmux
- mc(midnight commander)
- vtop
- htop
- vi
- NSSM