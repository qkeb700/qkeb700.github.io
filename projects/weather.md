---
layout: project
type: project
image: images/weathermain.png
title: open weather
permalink: projects/weather
# All dates must be YYYY-MM-DD format!
date: 2021-12-19
labels:
  - Open API
  - CSS
  - HTML
  - Javascript
  - JQuery
  - JSP
  - Ajax
summary: show temperature of location where you live around using Open API.
---

# 개인 프로젝트: Open API 날씨

## 개발환경
- ##### 개발 툴: Visual Studio Code
- ##### 깃허브 주소: https://github.com/qkeb700

## 프로젝트 요약
- ##### 배경색, 아이콘, 글자색 등으로 날씨를 표현할 수 있는 날씨웹, 앱
- ##### Open weather API 를 사용해 날씨 정보를 가져와서 현재 날씨 정보에 맞게 아이콘 및 날씨 관련단에 자동 변경
- Geolocation API 를 사용하여 사용자의 위치를 탐지하는 비동기 요청을 초기화하고, 위치 관련 하드웨어에 최신 정보를 요청
- Anchor 태그를 이용해 페이지 전환

## 프로젝트 상세 소개

### Geolocation API 사용전

<img class="ui centered huge image" src="..\images\beforeGeolocation.png">

### Geolocation API 사용후

<img class="ui centered huge image" src="..\images\weathermain.png">

### 위치 검색을 통한 날씨 정보 불러오기

<img class="ui centered huge image" src="..\images\searchfront.png">

## Project Structure

### Geolocation API 불러오기

<img class="ui centered huge image" src="..\images\geolocationapi.png">

getCurrentPosition() 메서드를 호출해서 사용자의 현재 위치를 얻을 수 있다.


### getWeather 메서드 만들기

<img class="ui centered huge image" src="..\images\getweather.png">

위에서 불러온 geolocation API 로 latitude 와 longitude 값을 받고 getWeather 메서드의 인자값으로 날씨를 위한 open API 를 위해 사용되어진다.


### Ajax 를 사용하여 통신하기

<img class="ui centered huge image" src="..\images\ajaxweather.png">

geolocation 값을 기반으로하고 url을 open API인 이미지속 주소로 하여 실시간 날씨 정보를 받아오고 데이터를 뿌려준다.


### 위치 검색에 맞게 날씨 정보 변경하기

<img class="ui centered huge image" src="..\images\searchweather.png">

검색창에 입력된 값을 getweather 메서드의 인자값중 하나로 보내서 if조건문을 이용하여 검색값이 있을때는 그 값을 기준으로 하는 지역의 날씨 정보를 ajax 통신하고 검색값이 없을 경우에는 geolocation API를 기준으로하고 ajax 를 이용하여 날씨 정보를 가져온다.


### 소스 코드 보러 가기
[링크 클릭](https://github.com/qkeb700/open_weather)
