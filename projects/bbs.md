---
layout: project
type: project
image: images/bbs35.png
title: Hoyeon's bbs
permalink: projects/bbs
# All dates must be YYYY-MM-DD format!
date: 2021-12-17
labels:
  - Java
  - CSS
  - HTML
  - Javascript
  - JQuery
  - MySQL
  - JSP
  - AJAX
summary: A project that shows lists of bbs.
---

# 개인 프로젝트: 게시판

## 개발환경
- #####	개발 툴: Eclipse
- #####	개발언어: JAVA JDK 1.8 64bit
- #####	서버 및 데이터베이스: Tomcat 9.0v, MySQL
- #####	디자인 API: Bootstrap 4, Font-awesome
- #####	깃허브 주소: https://github.com/qkeb700

## 프로젝트 요약
- #####	회원가입, 로그인을 하고 글을 작성, 읽기, 수정, 삭제 할 수 있습니다.
- #####	아이디/비밀번호를 찾는 기능과 글 작성시 파일을 업로드 할 수 있습니다.
- #####	관련 내용 게시물을 찾아 보여주는 검색 창이 있습니다.
- #####	한번 본 게시물의 조회수는 올라가지 않고 댓글을 달고 수정, 삭제 할 수 있습니다.
- #####	보안을 위해 권한이 허가되지 않은 경로로의 접근은 제한합니다.

## 프로젝트 상세 소개
### 프론트엔드 기술
#### 1.	회원가입
회원 약관 동의를 통해 가입을 할 수 있습니다.
 
<img class="ui centered huge image" src="..\images\bbs1.png">

 
#### 2.	로그인
회원가입을 통해 생성한 아이디와 비밀번호로 로그인을 할 수 있습니다.
 
<img class="ui centered huge image" src="..\images\bbs2.png">


#### 3.	홈
카테고리별로 생성된 게시판 목록을 조회 할 수 있습니다.
 
<img class="ui centered huge image" src="..\images\bbs3.png">


#### 4.	게시판 작성
글 작성을 통해 파일을 첨부하고 기본적인 정보를 입력 할 수 있습니다.

 <img class="ui centered huge image" src="..\images\bbs4.png">


#### 5.	게시판 보기
작성한 글의 상세 내용을 볼 수 있고 댓글도 볼 수 있습니다.
 
<img class="ui centered huge image" src="..\images\bbs5.png">


#### 6.	게시판 수정
게시판 관련 정보를 변경 할 수 있습니다.
 
<img class="ui centered huge image" src="..\images\bbs6.png">

#### 7.	게시판 삭제
게시판 생성시 입력한 비밀번호를 입력하여 삭제 할 수 있습니다.
 
<img class="ui centered huge image" src="..\images\bbs7.png">



### 백엔드 기술 
#### 1.	아이디/비밀번호 찾기
JQuery를 통하여 Ajax 통신사용

 <img class="ui centered huge image" src="..\images\bbs8.png">

비동기통신으로 데이터 교환이 이루어지고 성공적으로 값을 가져와 출력한다.

<img class="ui centered huge image" src="..\images\bbs9.png">



#### 2.	파일업로드 하기

 <img class="ui centered huge image" src="..\images\bbs10.png">

파일 업로드 기능을 위해 form 태그에 enctype 옵션을 추가한다


 <img class="ui centered huge image" src="..\images\bbs11.png">

업로드 할 파일이 저장될 장소를 dir로 저장하고 MultipartRequest로 데이터를 가져와 변수에 저장한다


 <img class="ui centered huge image" src="..\images\bbs12.png">

DB connect와 DAO 을 통하여 업로드 할 파일과 정보들을 insert 합니다.

#### 3.	조회수 올리기
Cookie와 JSTL 사용

 <img class="ui centered huge image" src="..\images\bbs13.png">

현재 게시물의 num과 cookie의 값이 같지 않을 때, cookie의 값을 현재 게시물의 num 값으로 하고 count를 1 증가시켜서 조회수를 올려줍니다.

#### 4.	페이징 구현
DTO와 DAO을 사용하여 데이터를 가져와 list.jsp에서 구현한다.

 <img class="ui centered huge image" src="..\images\bbs14.png">

페이징을 위한 기본값들을 세팅한다.


<img class="ui centered huge image" src="..\images\bbs15.png">
<img class="ui centered huge image" src="..\images\bbs16.png">
<img class="ui centered huge image" src="..\images\bbs17.png">
 
데이터베이스에서 한 번에 불러올 레코드를 제한해준다.


 <img class="ui centered huge image" src="..\images\bbs18.png">

DTO인 페이징 클래스에 현재 페이지와 총 레코드의 개수를 세팅해주고 DAO을 이용하여 필요한 값들을 list에 저장한다


<img class="ui centered huge image" src="..\images\bbs19.png">

List.jsp에 페이징을 구현한다..


#### 5.	검색으로 관련 게시물 찾기
제목, 글쓴이 또는 내용으로 관련된 게시물을 찾을 수 있다.

 <img class="ui centered huge image" src="..\images\bbs20.png">

Form 태그 안에 list.jsp 자신에게 보내는 input 값을 만든다.


 <img class="ui centered huge image" src="..\images\bbs21.png">

JQuery를 이용하여 전송할 input 값에 어떠한 방식으로 검색할지를 저장시킨다.


 <img class="ui centered huge image" src="..\images\bbs22.png">

변수 col과 val을 선언해주고 form 태그에서 보낸 colname과 values의 값들을 저장시킨다.


 
<img class="ui centered huge image" src="..\images\bbs23.png">
<img class="ui centered huge image" src="..\images\bbs24.png">
<img class="ui centered huge image" src="..\images\bbs25.png">

 
위에서 구현한 페이징 메소드에 col과 val 두 개의 매개변수를 추가하고 switch 문의 조건에 맞게 검색 내용을 데이터베이스값에서 찾는다.



<img class="ui centered huge image" src="..\images\bbs26.png">

검색 내용에 관련된 게시물의 수와 출력이 되어 페이징이 되어있는 것을 볼 수 있다.



#### 6.	댓글 기능 구현
Ajax 비동기 통신으로 값을 전달하여 댓글을 등록, 수정, 삭제 할 수 있다.

 <img class="ui centered huge image" src="..\images\bbs27.png">

form태그 안에 전송할 값들을 $form에 저장하여 통신한다. 


<img class="ui centered huge image" src="..\images\bbs28.png">
<img class="ui centered huge image" src="..\images\bbs29.png">
 
JSON 데이터를 처리하기 위한 자바 라이브러리를 Bean으로 가져온다.
댓글의 기능에 맞게 result 값을 넣어주고 JSON 객체를 문자열 데이터로 변경해준다


 <img class="ui centered huge image" src="..\images\bbs30.png">

Ajax로 받아온 input값에 따라서 댓글을 작성, 수정, 삭제 할 수 있고 각 기능을 수행 할 수 있다. 



#### 7. 답글 달기 기능
DAO를 수정하여 Parameter 로 들어오는 id 값의 유무로 DB에 insert해주는 방식을 달리한다.

<img class="ui centered huge image" src="..\images\bbs31.png">
<img class="ui centered huge image" src="..\images\bbs32.png">

Id의 값이 있을 때는 열람 중인 게시물에 대한 답글을 쓴다. 이 경우, orN은 원래 답글을 쓰고자 했던 게시물의 orN 값을 갖고 grN 과 lyN 은 원래 게시물의 값보다 1씩 증가한 값을 갖는다. 만약 원래 게시물에 다른 답변이 존재하고 있었다면 grN > ? 조건을 통해 모두 grN 을 1씩 증가시킴으로 순서에 문제가 생기지 않게 한다.
Id의 값이 없을 때는 새로운 게시물을 작성한다. 기존 게시물들과 엮이지 않는 새로운 게시물이기 때문에 orN의 Max를 찾아주고 그것에 1을 증가시켜서 새 글을 만들어 준다.



<img class="ui centered huge image" src="..\images\bbs33.png">

게시물과 게시물에 대한 답글을 순 차대로 출력하기 위해서 페이징을 위한 쿼리문을 수정해야한다. 



<img class="ui centered huge image" src="..\images\bbs34.png">

출력 시, 게시물과 게시물에 대한 답글을 구분하기 위해서 답글은 grN 이 원본의 값인 0 보다 크면 앞 쪽에 빈 공간을 주어서 구분하였다. 답글에 대한 답글은 lyN의 값으로 구분하여 답글에 주었던 공간보다 더 많은 빈 공간을 넣어서 구분한다. 게시물의 깔끔한 디자인을 위해서 답글에 대한 답글의 제한은 최대 2개로 제한한다.

<img class="ui centered huge image" src="..\images\bbs35.png">

게시물에 답글 달기 출력.


### [소스 코드 보러 가기] : (https://github.com/qkeb700/board)
