---
title: GitHub 블로그 만들기 - 글 작성법
author: Sangik-Jo
date: 2020-07-21 10:20:00 +0900
categories: [GitHub Blog]
tags: [Blog]
math: true
---


## **개요**
---
> 블로그를 다 만든 후 게시글을 작성하는 법에 대하여 다뤘습니다.  
  필수적인 부분들만 간추려 작성하였으므로 더 궁금하시면 인터넷 검색을 부탁드립니다.  
  
## **참고 사이트**
---
+ 마크다운(Markdown) 사용법 : <https://theorydb.github.io/envops/2019/05/22/envops-blog-how-to-use-md/>
+ 마크다운 에디터 - Prose.io : <https://prose.io/>

## **새글 쓰기**
---
### __1. 텍스트 문서 생성__
우선 블로그 파일이 있는 폴더로 가서 _pots 폴더로 들어갑니다.  
마우스 오른쪽 버튼 클릭 후 새로만들기 > 텍스트 문서 클릭   
  
![git-blog-pots-1](/assets/img/pots/2020-07-21-github-blog-pots/github-blog-pots-1.png)
  

### __2. 텍스트 문서 이름 변경__
__생성된 텍스트 문서의 이름과 확장자를 `날짜형식-영문이름.md` = `YYYY-MM-DD-파일이름명.md`로 바꿔줍니다.__  
`파일명은 꼭 영문`으로 또 `띄어쓰기 없이` 작성해 주세요!! 
  
![git-blog-pots-2](/assets/img/pots/2020-07-21-github-blog-pots/github-blog-pots-2.png)
  
### __3. 글에 대한 정보 설정__
글에 대한 정보를 설정하는 매우 중요한 부분입니다.
이 부분이 끝난 후는 Markdown이란걸 사용하여 글을 작성 합니다.
```
---
title: 글의 제목 (한글 가능)
author: Sangik-Jo
date: 2020-07-21 10:20:00 +0900
categories: [GitHub Blog]
tags: [Blog]
math: true
---
```
![git-blog-pots-3](/assets/img/pots/2020-07-21-github-blog-pots/github-blog-pots-3.png)

## **Markdown이란?**
---
> What is Markdown? (출처 - 위키백과)  
  마크다운(markdown)은 일반 텍스트 문서의 양식을 편집하는 문법이다.  
  README 파일이나 온라인 문서, 혹은 일반 텍스트 편집기로 문서 양식을 편집할 때 쓰인다.  
  마크다운을 이용해 작성된 문서는 쉽게 HTML 등 다른 문서형태로 변환이 가능하다.  
  
## **Markdown 주요 문법**
---
+ ### **헤더(h1) : 제목, 문단 구분**  
  
해당 문법을 쓰면 Chirpy 테마에서는 글 오른쪽에 헤더가 표시되고  
표시되는 헤더를 누르게되면 해당 헤더의 위치로 가게 되어있습니다.  
또한 `#` 작성후 `##` 처럼 하나 작게 쓰게 된다면 소문단으로 구분가능합니다.  
`#`은 HTML 코드인 `h1`을 의미합니다.  
  
```
# 제목 1 / h1
## 제목 2 / h2
### 제목 3 / h3
#### 제목 4 / h4
##### 제목 5 / h5
###### 제목 6 / h6
```

+ ### **수평선(hr) : 내용을 명시적으로 구분하고 싶을 때**
  
무엇인가 구분하고 싶을 때 사용하면 정리되는 느낌이 듭니다.
```
---
```

+ ### **엔터키(줄바꿈, 개행) : 라인을 바꾸고 싶을 때**  
  
바꾸고 싶은 부분에서 스페이스바 2번을 입력하면 됩니다.  
그럼 바로 이렇게 줄이 바뀐단 말이죠~  
```
글을 이렇게 작성하다.(시작)  (끝)
글 끝에 스페이스 바 두번을 치면?(시작)  (끝)
그럼 줄이 바뀝니다.

여기서는 엔터를 치면 줄이 바뀝니다.
```

+ ### **목록(List) : 요소를 나열할 때**  
  
글 앞에 동그라미나 숫자를 붙이고 싶을 때 사용합니다.  
`단! 동그라미를 사용할 때에는 스페이스바 2번으로 개행`을 해주셔야합니다.
  
1. 첫번째
1. 두번째
1. 세번째
  
+ 여러분
  - 행복해서 웃는건이 아니라
    * 웃어서 행복한 겁니다 하하하
      + 윌리엄 제임스 / 무한도전 노홍철
  
```
1. 첫번째
1. 두번째
1. 세번째

+ 여러분
  - 행복해서 웃는것이 아니라
    * 웃어서 행복한겁니다. 하하하하
      + 윌리엄 제임스 / 무한도전 노홍철
```

+ ### **강조 : 강조하고 싶은 단어를 표시할 때**  
  
__Bold(진하게)__  
**Bold(진하게)**  
_Italic(기울임)_  
~~취소선~~  
<u>밑줄</u>  
__진하면서*기울어지게도하고*~~취소선도~~<u>중복</u>가능합니다.__
  
```
__Bold(진하게)__
**Bold(진하게)**
_Italic(기울임)_
~~취소선~~
<u>밑줄</u>
__진하면서*기울어지게도하고*~~취소선도~~<u>중복</u>가능합니다.__
```

+ ### **인용구 : 인용할 경우 또는 분위기 전환시에 사용가능**
  
> 위키백과?
>> 무한도전 검색
>>> "레전드 예능 다시보고 싶다"
  
```
> 위키백과?
>> 무한도전 검색
>>> "레전드 예능 다시보고 싶다"
```

+ ### **링크(Link) : 하이퍼링크를 사용, 클릭하면 해당 페이지로 이동**  
TIP!! `{:target="_blank"}` 를 링크 뒤에 작성하면 새로운 탭에서 URL이 열립니다.
  
1. 단어를 클릭하면 URL로 이동) : [NPNGJ95 블로그](https://npngj95.github.io/ "마우스를 올리면 태그에 대한 설명"){:target="_blank"}
2. URL을 보여주고 URL로 이동 : <https://npngj95.github.io/>{:target="_blank"}
3. 동일 파일 내 `문단이동` : [동일 파일 내 문단이동](#인용구--인용할-경우-또는-분위기-전환시에-사용가능)

```
1. 단어를 클릭하면 URL로 이동) : [NPNGJ95 블로그](https://npngj95.github.io/ "마우스를 올리면 태그에 대한 설명"){:target="_blank"}
2. URL을 보여주고 URL로 이동 : <https://npngj95.github.io/>{:target="_blank"}
3. 동일 글(파일) 내 `문단이동` : [동일 글(파일) 내 문단이동 - 인용구](#인용구--인용할-경우-또는-분위기-전환시에-사용가능)
```
  
>유형3 문단 매칭방법 : 제목(header)를 복사 붙여넣기 후  
1) `특수문자제거`  
2) `스페이스`를 갯수만큼 `-로 변경`  
3) 대문자->`소문자`로 변경  
예) “인용구 : 인용할 경우 또는 분위기 전환시에 사용가능”  
 -> “#인용구--인용할-경우-또는-분위기-전환시에-사용가능”   
  

+ ### **이미지(image) : 이미지 삽입**  
    
```
1. 자동(원본) 사이즈 조절
- ![이미지 설명](이미지 주소)
- ![무도 이미지](/assets/img/pots/2020-07-21-github-blog-pots/infinity-challenge.png)

2. 이미지 사이즈 조절 (HTML 태그)
- <img src="이미지 주소" width="이미지 URL">
- <img src="/assets/img/pots/2020-07-21-github-blog-pots/infinity-challenge.png" width="111px">

3. 이미지에 링크 걸기
- [![이미지 설명](이미지 주소)](이동할 URL)
- [![무도 이미지](/assets/img/pots/2020-07-21-github-blog-pots/infinity-challenge.png)](http://www.imbc.com/broad/tv/ent/challenge/main.html){:target="_blank"}

```
[출처] MBC 무한도전
  
1. 자동(원본) 사이즈 조절  
![무도 이미지](/assets/img/pots/2020-07-21-github-blog-pots/infinity-challenge.png)
  
2. 이미지 사이즈 조절 (HTML 태그)  
<img src="/assets/img/pots/2020-07-21-github-blog-pots/infinity-challenge.png" width="111px">
  
3. 이미지에 링크 걸기  
[![무도 이미지](/assets/img/pots/2020-07-21-github-blog-pots/infinity-challenge.png)](http://www.imbc.com/broad/tv/ent/challenge/main.html){:target="_blank"}
  
## **Markdown 부가기능**  
---
+ ### **표 그리기**
  
`|`(파이프 기호) 백 스페이스 뒤에 있습니다. Shif+\  
열으로 구분하여 작성합니다. 아무렇게나 그려도 상관없습니다.  
`---` 헤더(머리글)를 분리할 경우 사용합니다.  
`:` 정렬에 관해 사용합니다.  
`:---` 해당 열을 좌측 정렬한다고 명시하는 것입니다.  
`---:` 해당 열을 우측 정렬한다고 명시하는 것입니다.  
`:---:` 해당 열을 중앙 정렬한다고 명시하는 것입니다.  
  
```
|	|예능	|평가	|
|:---	| ---:	| :---:	|
|좌측정렬	|우측정렬	|중앙정렬	|
|무한	|도전	|최고야	|
```
  
|	|예능	|평가	|
|:---	| ---:	| :---:	|
|좌측정렬	|우측정렬	|중앙정렬	|
|무한	|도전	|최고야	|
  
+ ### **코드 블록(Code Block)**  
__~~~__ 혹은 __```__  
소스코드를 작성할때 사용합니다.  
  
~~~
```java
int i = 10;
String str = "헬로우"
```
~~~

```java
int i = 10;
String str = "헬로우"
```