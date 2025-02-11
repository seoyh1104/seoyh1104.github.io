---
title: "[ETC] 파일질라(FileZilla)"
excerpt: "파일을 서버로 업로드하거나 다운로드할 때 사용하는 FTP(파일 전송 프로토콜) 클라이언트 프로그램."
categories: ETC
tag: [ETC]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

# 파일질라(FileZilla)
## FileZilla란?
FileZilla는 FTP(파일 전송 프로토콜) 클라이언트 및 서버 프로그램으로, 원격 서버와 로컬 컴퓨터 간에 파일을 주고받을 수 있도록 해주는 도구이다.

리눅스 서버에 접속할 때는 주로 **SSH(Secure Shell)**를 사용하는데, FileZilla도 **SFTP(SSH File Transfer Protocol)**를 지원하기에 리눅스 서버에 접속하고 파일 전송하는 데 사용할 수 있다.

## 주요 특징
- FTP, FTPS, SFTP 지원: 일반적인 FTP뿐만 아니라 보안이 강화된 FTPS, SSH 기반의 SFTP도 지원
- 직관적인 GUI: 드래그 앤 드롭으로 쉽게 파일 전송 가능
- 빠른 전송 속도: 다중 연결을 사용해 빠른 업로드/다운로드 지원
- 다양한 플랫폼 지원: Windows, macOS, Linux에서 사용 가능

### 다운로드
파일질라 다운로드 한글사이트
- [https://www.filezilla.kr/](https://www.filezilla.kr/){:target="_blank"}

## 📌 FileZilla로 리눅스 서버 접속하는 방법 (SFTP 사용)
1. FileZilla 실행
2. 상단의 빠른 연결(Qickconnect)에 정보 입력
  - 호스트(Host): sftp://서버_IP주소 `예: sftp://192.168.1.100`
  - 사용자명(Username): 리눅스 계정 이름 `예: ubuntu 또는 root`
  - 비밀번호(Password): 계정 비밀번호
  - 포트(Port): 보통 22 (SSH 기본 포트)
3. 빠른 연결(Quickconnect) 클릭
4. 서버 파일 탐색 및 업로드/다운로드 진행
서버에 연결되면 로컬 파일과 서버 파일을 드래그 앤 드롭으로 전송할 수 있다.

### 키 인증 방식(Private Key)으로 접속
만약 비밀번호 없이 키 인증 방식(Private Key)으로 접속하려면,  
"편집 > 설정 > SFTP" 에서 개인 키(.pem 또는 .ppk)를 추가하여 설정한다.

## 💡 참고
만약 단순 파일 전송만 필요하면 FileZilla 사용이 편리하지만, 명령어 작업이 필요하면 터미널에서 SSH 접속을 사용하는 게 더 좋다.  
리눅스 터미널 접속은 ssh 사용자명@서버_IP 명령어로 가능하다.
