---
title: "VSCode로 WSL에 접속하기"
categories: blog
tags:
 - VSCode
 - WSL
---
## 블로그 환경
윈도우10환경에서 VScode를 쓰니 터미널 사용에 불편함이 있어 WSL을 통한 연결을 해주었다.
* Windows 10
* Visual Studio Code
* WSL2

## WSL2 설정
1. 제어판 - 프로그램 - 프로그램 및 기능 - Windows 기능 켜기/끄기  
   Linux용 윈도우 하위시스템 체크
  ![Image Alt 텍스트]({{site.url}}/assets/img/1-1.png )
2. Microsoft Store에서 Ubuntu 설치후 실행(실행하지 않으면 우분투를 인식하지 못한다.)
3. 제어판 - 프로그램 - 프로그램 및 기능 - Windows 기능 켜기/끄기  
   가상 머신 플랫폼 체크
4. wsl의 커널을 업데이트한다.  
    ```wsl --update``` 
5. wsl의 버전을 확인한다.  
    ```wsl -l -v``` 
6.  wsl2 버전으로 변경한다.  
    ```wsl --set-default-version 2```

## VSCode로 접속
VSCode의 원격접속 기능을 활용해서 로컬에 설치된 리눅스로 접속하는 방식이다.
1. WSL의 원격접속을 위해 해당 플러그인을 설치해준다.
- ![Image Alt 텍스트]({{site.url}}/assets/img/1-2.png )
2. 설치 후 명령어 팔레트에서 "New WSL Window" 메뉴를 통해 접속이 가능하다.
3. 왼쪽 하단의 아이콘(WSL: Ubuntu-xx.xx) 버튼을 누른 후 "Close Remote Connection" 메뉴를 통해 연결을 종료할 수 있다.