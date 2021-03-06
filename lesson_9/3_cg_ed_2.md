---
title: CG Education 2
permalink: /lesson_9/3_cg_ed_2
---

# CG Education Part II

**Plan:** List steps/tasks in [Trello Boards](https://trello.com/cg_webdev_ss_2018)

**Do:**  Download app to your phone and play (instructions below).

**Record:** [Lesson 9.3 CoderGirl Education Project Part 2](https://learn.launchcode.org/courses/131/assignments/7556)


### Intro
To start, go ahead and open your terminal, navigate to that project, and make sure all your work from the last CG Education JS Practice is committed with git. Now open the project directory with your text editor and let's begin!

**To complete the challenges on this page:** you should be finished through lesson seven of Codecademy's "Introduction to JavaScript" course. We will include relevant Codecademy material in each challenge. Here's what your final project could look like by the end: [video](https://youtu.be/l8nviFt9oAU).

**To complete the _entire_ project:** you will have to work through lesson nine of the Codecademy [course](https://www.codecademy.com/learn/introduction-to-javascript). By the end of this project, you should have a working knowledge of Variables, Conditionals, Functions, Scope, Arrays, Loops, Iterators, Objects and Classes.



## Goals (for Part 2)
1. Read and understand someone else's code.
2. Use Google to solve problems!
3. Become more comfortable using Developer Tools, specifically Console.
4. *Frequently* use JavaScript's built-in `console` object to test and debug your work.
5. Use arrays to store data more efficiently.
6. Use loops to take action on the array data.
7. Use function to group together operations that you might want to use more than once.



#### Challenge 1: Making Teachers Fancy

Now that we know more than we did the last time we started using javascript in this project... let's make the teacher variables better.

You should have something like this currently in your javascript file... it might not be exactly like this which is great...
```
var teacherName = "Susan Baylor";
var teacherDepartment = "Physics";
var teacherRating1 = 3.5;
var teacherRating2 = 1.0;
var teacherRating3 = 5.0;

var teacherAvgRating = (teacherRating1 + teacherRating2 + teacherRating3) / 3;
teacherAvgRating = Math.round( teacherAvgRating * 10 ) / 10;
```

**STEP 1: Turn teacher rating variables into an array**

Now that we know about the array data structure, it would do a much better job at storing our teacher ratings. So go ahead and create an array to store the teacher ratings.


**STEP 2: Turn teacher's avg rating calculation into a function**

Create a function called `getRatingAvg` that takes one parameter, an array of ratings. The function should calculate and return the average rating from all the ratings in the array that is passed into the function (as a parameter).


**STEP 3: Create an add teacher rating function**

Create function called addTeacherRating, that takes 2 parameters... a ratings array and a new rating.

This function should add the new rating to the ratings array and return the array.


**STEP 4: Putting All the Pieces Together**

Now time to put all the pieces together...
create a prompt that asks the user to review a teacher... the prompt should say..

> if you don't know what a prompt is look to [this](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt) resource for help

"We would like for you to review <teacher name>. Please enter a rating between 0.0 - 5.0?"

note: make sure you store that value in a variable so you can use the users response...

then...
1) check that the user entered a number between 0.0 and 5.0...
2) if they did not, prompt them again...
3) if they did, add the rating value to the teacher's rating array
4) AND alert back to the user... "Thanks for you review! <teacher's name> average rating is now <avgRating>."



#### Challenge 2: Making Courses Fancy


**STEP 1: Create a courses array**

This courses array is actually going to be a double array... meaning it will be an array of arrays! Don't worry... one thing at a time.

You want your courses array to look like this...
```
[
    [<course-title>, <course-department>],
    [<course-title>, <course-department>],
    ..etc
]
```
course will be an array filled with courses and each course is an array with index 0 being a course title and index 1 being the department the course is associated with.

[Here](http://www.dyn-web.com/javascript/arrays/multidimensional.php) is a good resource for accessing elements in a nested array.

**STEP 2: Create a function that filters course by departments**

This function should take 2 parameter a course array and a department. The function should return a new array filled with courses that are ONLY in the department specified in the parameter.

note: to test that this works... I would suggest calling the function and then console.log the result to make sure it is filtering as expected.


**STEP 3: Putting it all together**

Create another prompt. (also you might have to comment the other prompt out, so that they don't interfere...). This prompt should ask the user what department they are looking for a course in. The user should enter a department name. Then...

1) check that the user entered a valid department name...
2) if they did not, prompt them again...
3) if they did, use the function you create above to filter the course list
4) AND alert (the js function like prompt) back to the user the course titles that they can choose from.


### Continue...

Hopefully these challenges helped you practice what you learned in the CodeAcademy Course.. now you are ready to continue on and take the next CodeAcademy lesson and learn about Objects. Then we will be back in this project and REALLY be able to make it fancy.

YEAH! ON WARD! (but first git commit!!! make those commits!!)
