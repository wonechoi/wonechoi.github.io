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
<p>Now that I think about it.. my best idea to struct contacts is a tree features that its nodes can have several contacts have same first name, connected by linked lists.</p>
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

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/SearchData1.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/SearchData1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/SearchData2.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/SearchData2.jpg"/></a>
</div>
<div class="col three caption">
	Search contacts by a first name. 
</div>
<p>
command: -rharry<br>
The program lists contacts which have a same first name. And it shows additional menus.
</p>
<br>

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/EditData1.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/EditData1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/EditData2.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/EditData2.jpg"/></a>
</div>
<div class="col three caption">
	Edit a contact 
</div>
<p>
command: -eharry,porter/malfoy,draco,28372617372<br>
The program checks if the old full name has existed and the new full name does not exist. Then, it deletes old data after insert new data. Or it shows an error message.
</p>
<br>

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/DeleteData1.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/DeleteData1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/DeleteData2.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/DeleteData2.jpg"/></a>
</div>
<div class="col three caption">
	Delete a contact 
</div>
<p>
command: -dharry,williams<br>
The program deletes the data. Or it shows an error message.
</p>
<br>

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/ShowList1.jpg" target="_blank"><img class="col one" style="height:360px" src="{{ site.baseurl }}/img/PhoneBook/ShowList1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/ShowList2.jpg" target="_blank"><img class="col one" style="height:360px" src="{{ site.baseurl }}/img/PhoneBook/ShowList2.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/ShowList3.jpg" target="_blank"><img class="col one" style="height:360px" src="{{ site.baseurl }}/img/PhoneBook/ShowList3.jpg"/></a>
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

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/WriteData1.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/WriteData1.jpg"/></a>
	<a href="{{ site.baseurl }}/img/PhoneBook/WriteData2.jpg" target="_blank"><img class="col one" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/WriteData2.jpg"/></a>
</div>
<div class="col three caption">
	Write all contacts to a file. 
</div>
<p>
command: -wnewfile.txt<br>
It visits every node in the tree by pre-order to list data.
</p>
<br>

<div class="img_row" style="height:360px">
	<a href="{{ site.baseurl }}/img/PhoneBook/Exit.jpg" target="_blank"><img class="col three" style="width:50%; height:360px" src="{{ site.baseurl }}/img/PhoneBook/Exit.jpg"/></a>
</div>
<div class="col three caption">
	Exit the program.
</div>
<p>
command: -e<br>
If any data has been added, edited or deleted while the program is on, the program reflects the changes to the current phone book file.
</p>
<br>

