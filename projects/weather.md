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

# Project: Open API Weather

## Development environment
- ##### Development Tool: Visual Studio Code
- ##### GitHub: https://github.com/qkeb700

## Project summary
- ##### Weather web and app capable of representing weather conditions with background color, icons, font color, etc.
- ##### Retrieves weather information using the OpenWeather API and dynamically updates icons and weather-related elements to reflect current weather conditions.
- Utilizes the Geolocation API to asynchronously detect the user's location and request the latest weather information based on the detected location.
- Page navigation using anchor tags

## Detailed introduction to the project

### Before using the Geolocation API

<img class="ui centered huge image" src="..\images\beforeGeolocation.png">

### After using the Geolocation API

<img class="ui centered huge image" src="..\images\weathermain.png">

### Retrieving weather information through location search

<img class="ui centered huge image" src="..\images\searchfront.png">

## Project Structure

### Loading the Geolocation API

<img class="ui centered huge image" src="..\images\geolocationapi.png">

The getCurrentPosition() method is used to obtain the user's current location.


### Creating the getWeather method

<img class="ui centered huge image" src="..\images\getweather.png">

The latitude and longitude values obtained from the Geolocation API are used as arguments for the getWeather method to fetch weather data from the OpenWeather API.


### Communication using Ajax

<img class="ui centered huge image" src="..\images\ajaxweather.png">

Real-time weather information is retrieved from the OpenWeather API based on the geolocation coordinates, using the API's URL as shown in the image. The data is then processed and distributed accordingly.


### Updating weather information based on location search

<img class="ui centered huge image" src="..\images\searchweather.png">

If a search value is provided, it is used as an argument for the getWeather method, enabling communication with the API to fetch weather data for the specified location. If no search value is provided, the geolocation API is used to determine the user's location and retrieve weather information.


### View source code
[Link](https://github.com/qkeb700/open_weather)
