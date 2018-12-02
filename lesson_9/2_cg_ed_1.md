---
title: CG Education - JS 1
permalink: /lesson_9/2_cg_ed_1
---

# CG Education - Javascript Part I

### Part I - learning a little javascript
We are going to use the nodeschool.io for our first javascript course. So follow the setup instructions on the site... and if you are confused, definitely reach out to a mentor.

[NodeSchool.io Javascripting](https://github.com/workshopper/javascripting)


#### Challenge 1: Learning Variables and some Data Types
Before you continue to Part II, complete the below challenges in the nodeschool.io course:

INTRODUCTION through NUMBER TO STRING

So basically stop at FOR LOOP challenge...


#### Challenge 2: Web Dev Tools and Javascript

Just like you can use Web Dev Tools to debug your HTML and CSS, you can also use it for javascript. To learn more, let's revisit the Web Dev Tools Course at CodeSchool.

Just complete LEVEL 3 - Console.

[CodeSchool Web Dev Course - Level 3](http://discover-devtools.codeschool.com/chapters/3)



### Part II - practicing a little javascript
Now that you have learned a little, let's practice with our CG Education Project (the project you should have completed with Flexbox).

To start, go ahead and open your terminal, navigate to that project, and make sure all your work is committed with git. Now open the project directory in your text editor and let's begin!



#### Challenge 1: Create and Link a Javascript File.

You can write javascript in your html file by using a `<script>` tag. However, this is not best practice.

Go ahead and create a new file called `main.js`. It is up to you where you store it. Sometimes all javascript files are kept in a folder called `js` just like you would keep all your css files in a folder called `css`. But the file structure is up to you.

In that file let's put a `console.log` statement like you used in the CodeSchool course. For example, `console.log("This file is linked!")`;

Now go into your html file add a `<script>` tag inside the `<head>` like the other `<link>` tags. Make sure to give the script tag a src attribute with the file path to your js file that you just created.

To test, open your index.html in a browser, open your web dev tools, click on the console tab, and refresh the page. You should see the message you logged!

> If you do not see the message, you src file path is most likely wrong. Try adjusting. If you can't get the message to appear still... use that Slack channel to ask for help :)



#### Challenge 2: Playing with Variables.

In your course, you should have learned how to create and use variables... like  
```
var name = "value";
```

Now create some variables for a teacher.

- Create a teacher name variable which should store a string with a full name.  
- Create a department variable which should store a string with a department name.   
- Create a rating 1, 2 and 3 variable which should store different float numbers limited to (0-5).

Now print a message to the console (using console log) that prints all these variables.

Bonus points for making it pretty... like:

>Teacher: Sally Jones  
Department: Physics  
Ratings: 3.4, 5.0, 4.2  


To test refresh your page and look in the console.



#### Challenge 3: Do a little math.

Now we are going to calculate the teacher's average rating and store it in a variable called avgRating.

Use the 3 float variables you created in your last challenge... add them and divide them by 3.

Tricky part... round the avgRating to a the near 10th place decimal...
definitely use Google!

now update your print out statement so it should look like this:

>Teacher: Sally Jones  
Department: Physics  
Ratings: 3.4, 5.0, 4.2  
Avg Rating: 4.4  


#### Challenge 4: Variables to Represent Data!

We just created variables that represented the data used on the teachers page. But what about the students and courses data. We should create variables to represent those items as well.

First, make sure your javascript file is linked to both of those html files.

Then, make a list of data used on those pages and create variables to represent them. Make sure the data type you use... like string or int or float... best presents the item.

After you create the variables... create nice print statements :)



THE END. Now you are ready to learn some more Javascript... onto the next Javascript Challenge!!
