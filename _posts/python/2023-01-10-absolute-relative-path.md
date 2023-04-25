---
title: "[Python] 현재 작업 디렉토리(경로) 확인 및 변경"
excerpt: "실행 파일에 대한 전체 경로를 취득하고 디렉토리명을 통해 현재 디렉토리(경로)를 변경하는 방법"
categories: Python
tag: [Python]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

## 기록
스크립트 작성 후 로컬 환경의 VS Code에서 실행할 때는 문제가 없었지만,  
다른 PC서버의 작업 스케줄러에 등록하는 작업에서 스크립트가 제대로 실행되지 않는 문제가 있는 것을 파악했다.
원인은 절대경로와 상대경로가 섞여 중간에 참조하는 폴더의 파일을 찾을 수 없는 것이 문제임을 알게되어  
유저가 자신이 원하는 폴더에서 스크립트를 실행해도 문제가 없도록, CMD 등과 리눅스(Ubuntu) 환경에서도 문제없이 실행할 수 있게
**파일이 실행되는 절대경로를 파악하여 현재 경로를 변경하고, 이후의 작업은 상대경로로 처리하는 방식으로 변경**했다.

## Python Code
```py
    def get_absolute_file_path():
        # 현재 작업 경로 확인
        # print(os.getcwd())
        # 현재 실행 파일에 대한 전체 경로를 취득하여 파일명을 제외한 디렉토리명을 취득
        program_directory = os.path.dirname(os.path.abspath(__file__))
        # 현재 디렉토리(경로) 변경
        os.chdir(program_directory)
```

## 관련 포스팅
[[OS] 절대경로(Absolute Path)와 상대경로(Relative Path)](/os/absolute-relative-path)