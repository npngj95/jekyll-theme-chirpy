---
title: GitHub 블로그 만들기 (chirpy 테마)
author: Sangik-Jo
date: 2020-07-20 10:24:00 +0900
categories: [GitHub Blog]
tags: [Blog]
math: true
---


## **개요**
---
> 블로그를 만들며 막혔던 부분들을 정리하기 위해 글을 작성합니다 ^^

## **참고 사이트**


## **프로그램 설치 사이트**
---
+ Jekyll 테마 [chirpy] : <https://github.com/cotes2020/jekyll-theme-chirpy>{:target="_blank"}
+ Git 설치 : <https://git-scm.com/>{:target="_blank"}
+ Ruby 설치 : <https://rubyinstaller.org/downloads/>{:target="_blank"}


## **블로그를 만든 이유**
---
저는 공부를하면 큰 틀은 생각이 나지만 세세한 부분을 잊어버렸습니다.  
그래서 제가 공부한 것을 정리하기위해 까먹지 않기 위해 기록을 남기기위함입니다.  
`후천적 천재가 되기위해. 사랑하는 사람과 행복하게 살기위해.`  
제가 작성하는 이 글이 보는 분께 도움이 되길 바랍니다 ^^  


## **GitHub 가입 및 Git 설치**
---
+ GitHub 가입 : <https://github.com/>{:target="_blank"}
+ Git 설치 : <https://git-scm.com/>{:target="_blank"}

가장먼저 GitHub에서 블로그를 만드려면 GitHub에 가입을 해야겠죠?^^  

**GitHub에 접속 후 `Sign Up` 버튼을 클릭하여 회원가입을 합니다.**  
![GitHub_Blog_Start_1-1](/assets/img/pots/2020-07-20-github-blog/github-blog-start-1-1.png)

**Git에 접속 후 `Download` 버튼을 클릭하여 Git을 다운받습니다.**  
![GitHub_Blog_Start_1-2](/assets/img/pots/2020-07-20-github-blog/github-blog-start-1-2.png)

## **마음에 드는 jekyll 테마를 고르기**
---
저는 이 부분이 가장 많이 신경쓰였던 부분이였습니다.  
나중에 바로바로 글들을 찾아 볼 수 있어야 했기 때문입니다..  
그 중 제가 선택한 테마는 chirpy 테마였습니다.  
카테고리 별로 글을 볼 수 있었고 태그를 줘서 글을 구분 할 수 있었기 때문이였습니다.  
  
다른 테마에서는 루비 커맨드 창에서 로컬 서버를 열었던 걸 봤던거같은데  
`chirpy 테마는 gitbash로 tools 폴더에 있는 프로그램들을 사용`하여  
`로컬 서버 [localhost:4000](localhost:4000){:target="_blank"} 를 열수도 있었고 push까지 가능`했습니다.  
  
해당 글에서는 github에 있는 chirpy 테마를 기준으로 진행하겠습니다.  
다른 테마를 적용하는 방법은 다른 좋은글들을 참고하며 진행부탁드립니다. ^^  
  
### **다양한 테마가 있는 사이트**
+ <https://github.com/topics/jekyll-theme>{:target="_blank"}
+ <http://jekyllthemes.org/>{:target="_blank"}
  

## **테마 가져오기 작업**
---
### **1. 원하는 테마 저장소 가져오기**
원하는 테마의 GitHub 페이지로 가서 Fork 버튼을 눌러주면 자신의 repository에 복사? 됩니다.  
![GitHub_Blog_Start_2-1](/assets/img/pots/2020-07-20-github-blog/github-blog-start-2-1.png)
  
### **2. 테마 저장소 이름 바꾸기**
복사된 저장소를 클릭 > `Setting`버튼을 클릭 > `저장소 이름 변경`  
**저장소의 이름은 매우 중요하니 반드시 규칙을 따라 바꿔주세요.**  
**저장소 이름 : [User_Name].github.io**  

![GitHub_Blog_Start_2-2](/assets/img/pots/2020-07-20-github-blog/github-blog-start-2-2.png)
  
### **3. 저장소의 메인 페이지에서 저장소의 주소 복사**  

![GitHub_Blog_Start_2-3](/assets/img/pots/2020-07-20-github-blog/github-blog-start-2-3.png)  
  
### **4. 블로그를 관리할 폴더 설정**
블로그에대한 파일들을 관리할 폴더를 정하고 해당폴더에 오른쪽 마우스를 클릭 합니다.  
Git을 설치한 후 표시되는 `Git Bash Here` 을 클릭합니다.  
 
![GitHub_Blog_Start_2-4](/assets/img/pots/2020-07-20-github-blog/github-blog-start-2-4.png)

**GitBash가 실행 되었다면 GitHub 아이디를 설정해줍니다.**  
**마지막으로 잘 설정되었는지 반드시 확인해야되겠죠?^^**  
```
$ git config --global user.name [User_Name]
$ git config --global user.email [User_ID]@naver.com
$ git config --global --list
```
![GitHub_Blog_Start_2-5](/assets/img/pots/2020-07-20-github-blog/github-blog-start-2-5.png)

### **5. 저장소 주소를 이용한 파일 복사**
설정이 모두 완료 되었다면 복사해둔 저장소 주소를 이용해 파일을 복사해줍니다.  
신기하죠? 저도 그래요~^^  
Git Bash에서 붙여넣기 커맨드는 Shif+Ins 입니다~^^  
`$ git clone 복사한 주소`

![GitHub_Blog_Start_2-6](/assets/img/pots/2020-07-20-github-blog/github-blog-start-2-6.png)

### **6. [GemFile] 파일 수정**
GemFile을 메모장으로 열어 해당 내용을 추가해 줍니다.  
time-zone(시간)에 관한 내용 같은데 자세한 내용은 더 공부를 해야할거 같아요 ㅠㅠ  
뭔가 윈도우의 시간 체계를 사용하겠다?? 그런 느낌이 드네요..느낌만...  
```
gem 'tzinfo-data', platforms: [:mingw, :mswin]
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw]
```
![GitHub_Blog_Start_2-7](/assets/img/pots/2020-07-20-github-blog/github-blog-start-2-7.png)

## Ruby 다운 및 설정

### **1. Ruby 설치**
+ Ruby 다운 : <https://rubyinstaller.org/downloads/>  
Ruby+Devkit 2.6.6-1 (x64) 버전을 기준으로 하였습니다.  
모두 기본 값으로 설치 후 마지막의 커맨트 창(cmd창)은 닫아줍니다.  
마지막 창은 닫아주어도 된다고 하는데 무엇인지 몰라 궁금하네요 ㅠㅠ  

![GitHub_Blog_Start_3-1](/assets/img/pots/2020-07-20-github-blog/github-blog-start-3-1.png)

### **2. Ruby Command창을 이용한 gem 설치**
gem에 대해 간단히 설명하자면 `잼 = 라이브러리`라고 합니다.  
즉, 필요한 기능이 있을 때 추가해서 사용하면 된다는 뜻 입니다.  
그림과 같은 루비 프로그램을 실행해 줍니다.  

![GitHub_Blog_Start_3-2](/assets/img/pots/2020-07-20-github-blog/github-blog-start-3-2.png)

**이제 ``로컬 서버를 돌리기위해 gem을 다운``받아야 합니다.**  
**매우 중요한 부분이겠죠?!**  
아래의 명령어로 gem을 다운받아 줍니다.  
`첫번째 명령어는 기본적으로 다운받아야할 gem`을 적어 두었습니다.  
조금은 번거롭고 시간이 필요한 작업이지만 열심히 해봅시다^^  
```
gem install jekyll bundler tzinfo-data
```
<img src="/assets/img/pots/2020-07-20-github-blog/github-blog-start-3-3.png" width="700px">

`두번째 명령어는 필요한 gem을 알려주면 해당 gem을 다운`받기위한 명령어 입니다.  
로컬 서버를 열어주는 명령어인 `jekyll serve` 를 커맨드 창에 입력하면  
gem을 찾을 수 없다는 메시지가 나오게 됩니다.  
  
메시지에 나오는 gem들을 모두 다운받아 주도록 합시다^^
```
jekyll serve
gem install [필요한 gem의 이름]
```

<img src="/assets/img/pots/2020-07-20-github-blog/github-blog-start-3-4.png" width="700px">

필요한 gem들이 모두 다운로드 완료 되면 `jekyll serve`를 쳤을 때 아래 그림과 같이 나오게 됩니다.  
여기서 [localhost:4000](localhost:4000){:target="_blank"}으로 들어가게 되면 로컬 서버로 chirpy테마의 블로그가 개설된 것을 확인 할 수 있습니다.  
**!하지만 이렇게 했을 때는 카테고리기능이 작동하지 않습니다.**  

![GitHub_Blog_Start_3-5](/assets/img/pots/2020-07-20-github-blog/github-blog-start-3-5.png)


## **로컬 서버를 이용한 블로그 테스트**

이제 길고 길었던 준비가 끝났습니다~^^  
블로그 파일들이 있는 폴더로가서 다시 Git Bash를 실행하여 줍니다.  
아시다시피~~ `마우스 오른쪽 클릭 + Git Bash Here 클릭` ^^  
아래 명령어를 입력하면 블로그의 모든 기능이 잘 작동하는것을 확인할 수 있습니다.  
```
$ bash tools/run.sh
```
![GitHub_Blog_Start_4-1](/assets/img/pots/2020-07-20-github-blog/github-blog-start-4-1.png)

## **GitHub블로그 업데이트**
로컬 서버는 수정한 사항들을 확인하고 올바르게 작동 하는지 확인하기 위함 입니다.  
수정한 파일들이 있다면 자신의 블로그에 적용 시켜야 하겠죠?^^  
```
$ rm -rf .travis.yml .github _posts/* 
$ git status
$ git add .
$ git commit -m "커밋 메시지"
$ bash tools/publish.sh 
```
  
`rm -rf .travis.yml .github _posts/*` 명령어는  
필요없는 파일들을 삭제하는 명령어입니다.  
**posts 폴더안의 글은 유용한 글이니 꼭 한번 읽어 본 뒤에 삭제하세요!**
  
`git status` 명령어는 새로 만들어지거나 삭제되는 등  
상태가 변한 파일들을 한눈에 보여주는 명령어 입니다.  
  
`git add .` 명령어는 상태가 변환 파일들을 
블로그에 반영하기위해 파일들을 선택해주는 명령어 입니다.  
  
`git commit -m "커밋 메시지"` 명령어는  
선택된 파일들을 수정하겠다고 확정짓는 명렬어 입니다.  
  
`bash tools/publish.sh` 명령어는 
최종적으로 수정사항들을 블로그에 반영하는 명령어 입니다.
  
## **마지막으로**
처음으로 저의 블로그를 개설해 봤는데 조금 어려웠지만 재미있었습니다.  
혹시나 이글을 보는 분이 있다면 충분히 하실 수 있을 것입니다.  
많이 부족한 저도 했으니까요 힘냅시다^^!!  
  
다음 글에서는 게시글을 작성하는 법과 유용한 팁들을 작성해보겠습니다.  