---
title: CG Education - FINAL
permalink: /1_2018/lesson_10/1_cg_ed_final
---

# CG Education - Final (JS + jQuery)

### Intro
Alright!!! Time to put all your knowledge to the test. Javascript... jQuery... even HTML/CSS. Let's get started!


#### Course Filters

For our first challenge... we are going to add some filters to the course page AND make those filters actually work.


**STEP 1: Dynamically Create Courses**

What do we mean by "dynamically create"? Well if you have noticed, you have 2 sets of course. One set is coded in the html/css. And the other set is our courses array in our JS code.

Our goal: To make them match by using our js courses array to create the html. And we can do this by using [html strings](http://api.jquery.com/Types/#htmlString) in our JS then inserting it into our html.

Create a function called `updateCourseDisplay` that takes one parameter courses (an array of course objects). This functions should loop through the courses, generate an html string for that course, and add it to your html.

> note: your html strings should match what your html/css currently looks like so your courses display the same way you currently have them. Also you might have to delete the hard-coded courses in your html/css because now we want javascript to add them.

Finally call this function passing to it your all courses array.

YEAH! your courses should now be dynamically creating on load, rather than static in your html/css.


**STEP 2: Add Filters for Courses**

Now back to html/css for a little bit! We are going to add some dropdown filters to our courses page that look relatively like this:

<img width="80%" src="./images/cd_ed_course_filter.png" />


**STEP 3: Make Filters Work**

Let's start with the department filter. We should already have a function that filters an array by department.

1) create an event listener that is triggered every time the "filter" button is clicked. When clicked get the value from the department dropdown ... and  `console.log` it, so we can make sure we are grabbing the correct value :)

2) once we are grabbing the correct value, let's call the filter department function.

> note: this should pass back a new course array so make sure you have a variable to capture this!

3) let's call the `updateCourseDisplay` function we created in step one, with the new course array!

Is it working?!?! If not, time to debug. Use that console.log to see what values you are gettin.

If so, YEAH! this is exciting.

So exciting that we should also make the select semester filter work as well. I am not going to give you step by step instructions for this one. So if you have questions holla.



#### Teacher Ratings

Now it's time to make the teacher's page fancy! We are going to a panel that slides open with teacher information AND that has a little form for adding a new teacher rating.


**STEP 1: Implement the HTML/CSS jQuery**

Below is the new design. When a teacher card is clicked... a panel should slide open with a little info about the teacher and an add new rating form. the panel should close when the x in the top right corner is clicked OR on a submit of the add new rating form.

<img width="80%" src="./images/cg_ed_teacher_panel.png" />

If you have other questions on how this should work, feel free to ask. We aren't worried about actually doing anything with the new rating yet. Just want to get the html/css and jQuery part working.


**STEP 2: Dynamically Create Teachers**

First (since we don't already have one like we did with the courses), we need to create an array of teacher objects. Let's go ahead and do that now. Use the teacher information you have "hard-coded" in the html/css.

Then create a function to display them all (like we did with the courses).


Once this is done, be sure to test and make sure your sliding panel still works!

YEAH! we are doing it! We are really doing it!


**STEP 3: Add Teacher Rating**

Okay so. Now we need to make the submit rating button work. This will require:

1) An event listener to watch for the submit rating button click.

2) Using jQuery to grab the teacher rating entered.

3) Using jQuery AND javascript to figure out which teacher we need to add the rating to.

4) Use our previous addRating function to add the new rating to the teacher object.

5) Update the displayed teacher rating in the html/css.

6) Don't forget to close the panel after the new rating is submitted.

Whew. This is going to be a lot of work. But I believe in you. I am purposely leaving the instructions vague, so you have to use some brain power to logically figure out how the html/css, jQuery and javascript are going to work together here. Remember there are definitely more than one way to get this to work.


#### New Students

Okay, You should be getting the hang of it by now... so I am going to give you a little less instruction and just describe our next feature. We are going to add a panel (it doesn't have to slide open, it can just stay open) to the student page that looks like this:

<img width="80%" src="./images/cg_ed_new_student.png" />

This form should allow you to create a new student. Somethings to get you started...

1) I don't think we have created a student object prototype in our javascript yet so at some point we are going to need to do that.
2) Dynamically creating the students like we did with the courses and teachers could be helpful for when we want to add the new student.
3) Currently, our new student form does not have a place to upload an image or add courses, so don't worry about those 2 things for now. You should just use a place holder for new student images.

Alight, good luck! Let a mentor know if you have questions about getting started.


#### THE END

So you can be done with this project now! whoo!

But if you want to add some additional features I have some ideas:

1) Create an Individual Course Page. So when you click on a course, it takes you to a page where you can view information just about that one course.

2) On that individual course page, add a form that allows you to add students to a course roster. You should only be able to add students that exist in your Javascript and you are going to have to modify the Course Object a little so you can have a roster property to fill with student objects. YEAH!

I bet you have experience with interacting with applications like this on the web... do you have any features you think could be added?
