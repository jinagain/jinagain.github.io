---
title: "Github Page에 Jekyll 테마를 적용한 블로그 만들기"
categories: blog
tags:
 - github
 - jekyll
---
## Github Page
Github의 Repository를 활용해 접속가능한 정적 페이지를 만드는 기능을 제공해준다.
1. Github의 Setting - Pages 에서 GitHub Pages 사용을 설정할 수 있다.
2. 새로운 Repository를 만들고 이름을 "username.github.io" 로 지으면  
   username.github.io url로 접속시 자신의 GitHub Pages로 접속할 수 있다.

## Jekyll 테마 적용
[jekyllthemes](http://jekyllthemes.org/) 사이트에서 원하는 테마를 선택하여 적용할 수 있다.  
jekylltheme는 관련 설정을 통해 로컬에서 실행시킬 수 있고, 작성한 내용은 Github와의 연동으로 업로드 할 수있다.
### Ubuntu에서 설정
1. Ruby를 필요로 하기 때문에 관련 앱을 설치한다.  
```sudo apt install ruby-full build-essential zlib1g-dev```

2. gem을 통해 설치 할 때 권한오류를 해결하기 위해 다음 작업을 한다.
```
mkdir .gems
# Install Ruby Gems to ~/gems
export GEM_HOME="$HOME/.gems"
export PATH="$HOME/.gems/bin:$PATH"
```
3. 필요한 앱을 설치해준다.  
```gem install jekyll bundler```
4. jekylltheme를 다운로드 혹은 클론하였다면 해당 폴더로 이동한 후 다음 명령어를 입력해준다.  
```bundle install```
```jekyll serve```
5. 로컬서버가 실행된 후 접속이 된다면 블로그 개발환경은 완료된다.
