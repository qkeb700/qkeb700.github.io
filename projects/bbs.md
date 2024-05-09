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

# Project: Forum

## Development environment
- #####	Development tool: Eclipse
- #####	Development language: JAVA JDK 1.8 64bit
- #####	Server and database: Tomcat 9.0v, MySQL
- #####	Design API: Design API: Bootstrap 4, Font-awesome
- #####	GitHub : https://github.com/qkeb700

## Project summary
- #####	Users can sign up, log in, and perform CRUD operations on posts.
- #####	Users can retrieve their ID/password and upload files when creating a post.
- #####	There is a search feature that finds and displays related content posts.
- #####	Viewing a post does not increase the view count, and users can comment on, edit, or delete posts.
- #####	Access to unauthorized routes is restricted for security purposes.

## Detailed introduction to the project
### Front-end technology
#### 1.	Sign up
Users can sign up by agreeing to the membership terms and conditions.

<img class="ui centered huge image" src="..\images\bbs1.png">

 
#### 2.	Login
Users can log in with the ID and password they created during membership registration.
 
<img class="ui centered huge image" src="..\images\bbs2.png">


#### 3.	Home
Users can view a categorized list of forum.
 
<img class="ui centered huge image" src="..\images\bbs3.png">


#### 4.	Create a forum
By writing a post, users can attach files and enter basic information.

 <img class="ui centered huge image" src="..\images\bbs4.png">


#### 5.	View forum
Users can view the details of the articles they wrote and also view comments.
 
<img class="ui centered huge image" src="..\images\bbs5.png">


#### 6.	Forum modification
Users can change information related to the forum.
 
<img class="ui centered huge image" src="..\images\bbs6.png">

#### 7.	Delete forum
Users can delete a forum by entering the password they used when creating it.
 
<img class="ui centered huge image" src="..\images\bbs7.png">



### Backend technology
#### 1.	Find ID/Password
Implemented using Ajax communication through JQuery

 <img class="ui centered huge image" src="..\images\bbs8.png">

Data is exchanged through asynchronous communication, and the value is successfully retrieved and output.

<img class="ui centered huge image" src="..\images\bbs9.png">



#### 2.	Upload files

 <img class="ui centered huge image" src="..\images\bbs10.png">

Added enctype option to form tag for file upload function.


 <img class="ui centered huge image" src="..\images\bbs11.png">

Saved the location where the file to be uploaded is stored as dir, retrieved the data using MultipartRequest, and saved it in a variable.


 <img class="ui centered huge image" src="..\images\bbs12.png">

Inserted files and information to be uploaded through DB connection and DAO.

#### 3.	 Increase views
Used Cookies and JSTL

 <img class="ui centered huge image" src="..\images\bbs13.png">

When the num and cookie values ​​of the current post are not the same, the cookie value is set to the num value of the current post and the count is increased by 1 to increase the number of views.

#### 4.	 Paging implementation
Used DTO and DAO to retrieve data and implemented it in list.jsp.

 <img class="ui centered huge image" src="..\images\bbs14.png">

Set default values ​​for paging.


<img class="ui centered huge image" src="..\images\bbs15.png">
<img class="ui centered huge image" src="..\images\bbs16.png">
<img class="ui centered huge image" src="..\images\bbs17.png">
 
Limited the number of records to be loaded from the database at one time.


 <img class="ui centered huge image" src="..\images\bbs18.png">

Set the current page and total number of records in the paging class, which is a DTO, and used DAO to store the necessary values ​​in a list.


<img class="ui centered huge image" src="..\images\bbs19.png">

Implemented paging in List.jsp.


#### 5.	Find related posts through search
Users can find related posts by title, author, or content.

 <img class="ui centered huge image" src="..\images\bbs20.png">

Created an input value sent to list.jsp within the Form tag.


 <img class="ui centered huge image" src="..\images\bbs21.png">

Used JQuery to store the search method in the input value to be transmitted.


 <img class="ui centered huge image" src="..\images\bbs22.png">

Declared variables col and val and stored the values ​​of colname and values ​​sent from the form tag.


 
<img class="ui centered huge image" src="..\images\bbs23.png">
<img class="ui centered huge image" src="..\images\bbs24.png">
<img class="ui centered huge image" src="..\images\bbs25.png">

 
Added two parameters, col and val, to the paging method implemented above and searched the database values ​​according to the conditions of the switch statement.



<img class="ui centered huge image" src="..\images\bbs26.png">

Users can see the number of posts related to the search content and the output and paging.



#### 6.	 Implementation of comment function
Users can register, edit, or delete comments by passing values ​​through Ajax asynchronous communication.

 <img class="ui centered huge image" src="..\images\bbs27.png">

The values ​​to be transmitted within the form tag are stored in $form and communicated. 


<img class="ui centered huge image" src="..\images\bbs28.png">
<img class="ui centered huge image" src="..\images\bbs29.png">
 
A Java library for processing JSON data is imported as a Bean.
Entered the result value according to the comment function and changed the JSON object to string data.


 <img class="ui centered huge image" src="..\images\bbs30.png">

Depending on the input value received through Ajax, comments can be created, modified, or deleted, and each function can be performed.. 



#### 7. Reply function
By modifying the DAO, the method of insertion into the DB is different depending on the presence or absence of the id value coming in as a parameter.

<img class="ui centered huge image" src="..\images\bbs31.png">
<img class="ui centered huge image" src="..\images\bbs32.png">

When there is an ID value, a reply is written to the post being viewed. In this case, orN contains the value of the post to which the original reply was intended, and grN and lyN have values ​​incremented by 1 from the original post's value. If there were other replies to the original post, grN > ? All grNs are increased by 1 through conditions to prevent ordering problems.
If there is no ID value, a new post is created. Because it is a new post that is not connected to existing posts, a new post is created by finding the Max of orN and increasing it by 1.



<img class="ui centered huge image" src="..\images\bbs33.png">

In order to output posts and replies to posts in order, the query statement for paging must be modified.



<img class="ui centered huge image" src="..\images\bbs34.png">

When printing, in order to distinguish posts from replies to posts, replies were separated by an empty space at the front if grN was greater than the original value of 0. Replies to replies are separated by the value of lyN and were given more empty space than the reply. For a clean design of the post, the number of replies to a reply was limited to a maximum of two.

<img class="ui centered huge image" src="..\images\bbs35.png">

Print a reply to a post.


### View source code
[Link here](https://github.com/qkeb700/board)
