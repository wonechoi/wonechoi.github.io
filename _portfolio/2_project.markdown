---
layout: post
title: Project
description: a project with a background image
img: /img/2.jpg
---

This survey is designed to gather information about how consumer preferences and behavior are changed.

live link: <a href="http://choihyew.dev.fast.sheridanc.on.ca/nyu_survey_201811/pages/q1.php"> nyu_survey_201811</a>

	---
	Duration: November 2018
	Languages: HTML, CSS, Javascript, JQuery, Bootstrap
						PHP, MySQL
	---


<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/surveyPage1.jpg" alt="" title="First page"/>
	<img class="col one" src="{{ site.baseurl }}/img/surveyPage2.jpg" alt="" title="Middle page"/>
	<img class="col one" src="{{ site.baseurl }}/img/surveyPage3.jpg" alt="" title="End Page"/>
</div>
<div class="col three caption">
	15+ different pages designed responsive to any screen sizes comprise the survey.<br>
	To prevent from misuse or abuse of the survey, a session check a page a respondent should proceed and direct to only the page.<br>
	Any responses, even when respondents quit in the middle of survey, are saved in MySQL databases to be analyzed. 
</div>
<br><br>
<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/img/surveyScn1.jpg" alt="" title="Scenario 1"/>
</div>
<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/img/surveyScn2.jpg" alt="" title="Scenario 2"/>
</div>
<div class="col three caption">
	5 scenarios per a survey are picked from random pool, with soft drinks arranged in random orders as well.<br>
	A respondent add soft drinks to the shopping cart within a limit instructed in each questions.<br>
	Inserting the data considers the order in which a respondent put them into the cart.	
</div>

You can also put regular text between your rows of images. Say you wanted to write a little bit about your project before you posted the rest of the images. You describe how you toiled, sweated, *bled* for your project, and then.... you reveal it's glory in the next row of images.


<div class="img_row">
	<img class="col two" src="{{ site.baseurl }}/img/6.jpg" alt="" title="example image"/>
	<img class="col one" src="{{ site.baseurl }}/img/11.jpg" alt="" title="example image"/>
</div>
<div class="col three caption">
	You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


<br/><br/><br/>


The code is simple. Just add a col class to your image, and another class specifying the width: one, two, or three columns wide. Here's the code for the last row of images above: 

	<div class="img_row">
	  <img class="col two" src="/img/6.jpg"/>
	  <img class="col one" src="/img/11.jpg"/>
	</div>
