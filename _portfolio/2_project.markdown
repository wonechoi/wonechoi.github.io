---
layout: post
title: Phone Book 
description: developed with C language and an AVL tree structure
img: /img/PhoneBook/phoneBookMain.jpg
---

This phone book project is designed to show knowledge kinds of collections and structures in C language.

github: <a href="https://github.com/wonechoi/PhoneBook" target="_blank">Phone Book</a>

	---
	The individual project in Data Structures & Algorithm Development - C class
	Duration: April 2019
	Feature: 
  - By seperating data structure from main sources, 
  brought some of the style of object-oriented programming to C.
  - Used an AVL tree structure to save contacts.
  - Retrieve, Edit, Delete, Show, Add, Load, Save, Exit
	---
  
<p><strong>Array</strong>: is not suitable for a phone book since the maximum number of contacts to be stored could not be determined. <br>
<strong>Linked List</strong>: is the most efficient with O(1) cost when saving a new contact, but a phone book is more frequently used for search than insert. It costs O(n) to search for contacts. <br>
<strong>Hash map</strong>: cannot be used for a phone book since I am not sure my hash algorithm makes the same key for different names.<br>
<strong>Tree</strong>: saves contacts as an ordered list by the first name. There it doesn't need any additional algorithms to sort for listing all contacts. And it costs O(nlogn) to search for contacts. However, the tree can be likely to become a one-sided tree depends on an initial file used to register. Hence, I chose an AVL tree which is a self-balancing binary search tree. <br><br>
  
<strong>Disadvantage</strong>: a tree cannot save the same value. But a phone book should be able to have the same names. I consist of the tree by the first name and allow to save the same first names, but not last names. Before adding a new contact, the program checks if there is the same full name. When a search for contacts by a first name, the program continues the search under its subtree after finding a contact. Same first name can be in the right part of its left child or in the left part of its right child.  <br><br>  
</p>  
<p>Now that I think about it.. my best idea to struct contacts is a tree by the full name and each node can have several contacts connected by linked lists.</p>
<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/Main1.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/Main1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/Main2.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/Main2.jpg"/></a>
</div>
<div class="col three caption" style="margin-bottom:5px">
	Main page
</div>
<p>The phone book automatically loads records from contacts file(csv format) when it starts.<br>The application parses user input.<br>
How to use:<br>-r retrieve data with followed firstname.<br>-s show all contacts ordered by firstname.<br>-a add new data. firstname,lastname,mobile<br>-l load a following file name.<br>-w write the phone book to a new file. The name of file is following.<br>-e Exit the phone book
</p>
<br>

<div class="img_row">
	<a href="{{ site.baseurl }}/img/Survey/surveyPage1.jpg" target="_blank"><img class="col one" src="{{ site.baseurl }}/img/Survey/surveyPage1.jpg" alt="" title="First page"/></a>
	<a href="{{ site.baseurl }}/img/Survey/surveyPage2.jpg" target="_blank"><img class="col one" src="{{ site.baseurl }}/img/Survey/surveyPage2.jpg" alt="" title="Middle page"/></a>
	<a href="{{ site.baseurl }}/img/Survey/surveyPage3.jpg" target="_blank"><img class="col one" src="{{ site.baseurl }}/img/Survey/surveyPage3.jpg" alt="" title="End Page"/></a>
</div>
<div class="col three caption" style="margin-bottom:5px">
	15+ different pages designed responsive to any screen sizes comprise the survey.
</div>
<p>To prevent from misuse or abuse of the survey, a session checks the page and ensures the respondent should proceed and is directed to the next page only.	Any responses, even when respondents quit in the middle of survey, are saved in MySQL databases to be analyzed. 
</p>
<br>

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/ShowList1.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/ShowList1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/ShowList2.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/ShowList2.jpg"/></a>
</div>
<div class="col three caption">
	Show all contacts. 
</div>
<p>
command: -s<br>
It visits every node in the tree by in-order to show ordered data. If the length of data is over-sized, the rest of data is shown in the next page.
</p>

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/AddData1.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/AddData1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/AddData2.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/AddData2.jpg"/></a>
</div>
<div class="col three caption">
	Add new contact. 
</div>
<p>
command: -ahyewon,choi,4372300401<br>
It visits every node in the tree by in-order to show ordered data. If the length of data is over-sized, the rest of data is shown in the next page.
</p>
<br>

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/LoadData1.jpg" target="_blank"><img class="col one" style="height:360px" src="{{ site.baseurl }}/img/PhoneBook/LoadData1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/LoadData2.jpg" target="_blank"><img class="col one" style="height:360px" src="{{ site.baseurl }}/img/PhoneBook/LoadData2.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/LoadData3.jpg" target="_blank"><img class="col one" style="height:360px" src="{{ site.baseurl }}/img/PhoneBook/LoadData3.jpg"/></a>
</div>
<div class="col three caption">
	Load new contacts from a file. 
</div>
<p>
command: -lNEWCONTACTS.txt
</p>
<br>


