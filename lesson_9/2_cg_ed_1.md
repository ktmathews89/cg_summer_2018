---
title: CG Education - JS 1
permalink: /lesson_9/2_cg_ed_1
---

# CG Education - JavaScript Part I

**Plan:** List steps/tasks in [Trello Boards](https://trello.com/cg_webdev_ss_2018)

**Do:**  Download app to your phone and play (instructions below).

**Record:** [Lesson 9.3 CoderGirl Education Project Part 1](https://learn.launchcode.org/courses/131/assignments/7553)

## Intro

You're here! You made it! You rock! Welcome to the start of your final project!

**To complete the challenges on this page:** you should be finished with Lesson 1 of Codecademy's "Introduction to JavaScript" course. We will include relevant Codecademy material in each challenge. Here's what your final project could look like by the end: [video](https://youtu.be/l8nviFt9oAU).

**To complete the _entire_ project:** you will have to work through lesson nine of the Codecademy [course](https://www.codecademy.com/learn/introduction-to-javascript). By the end of this project, you should have a working knowledge of Variables, Conditionals, Functions, Scope, Arrays, Loops, Iterators, Objects and Classes.

## Goals (for Part 1)
1. Read and understand someone else's code.
2. Use Google to solve problems!
3. Become more comfortable using Developer Tools, specifically Console.
4. *Frequently* use JavaScript's built-in `console` object to test and debug your work.
5. Create some variables.
6. Do basic math with those variables.
7. Learn how to use resources like MDN to discover more functions you can use for built-in JavaScript objects and data types.

## Getting Started

First, download the project files [here](https://bit.ly/cg_ss18_cg-education). The HTML and CSS files have been written for you so you can focus on the JavaScript. However, you are free to update the HTML and CSS as you like! Just remember that the focus of this project is the JavaScript. You'll find basic wireframes for the site design in the `wireframes/` directory.

## Challenges
### Challenge 1: Create and Link a JavaScript File.

> Introduction to Javascript: [Console](https://www.codecademy.com/courses/introduction-to-javascript/lessons/introduction-to-javascript/exercises/console)

You can write JavaScript in your html file by writing JavaScript inline between `<script>...</script>` tags. However, writing inline JavaScript is not best practice. Why? Well, you may want to share your JavaScript (JS) between several different web pages. Copying and pasting your inline JS between the pages could lead to mistakes and make your site very hard to maintain.

Does this sound familiar? It should! It's just like what you should do with your CSS–try to keep your styles in a `.css` file!

Now, create a new file called `main.js`. It is up to you where you store it. Some developers like to keep all of their JavaScript files in a folder called `js` (just like you would keep all your css files in a folder called `css`). But, the file structure is up to you.

In your new `main.js` file, let's put a `console.log(...);` statement like you used in the Codecademy course. For example, `console.log("Hello world!");`. Or, `console.log("I hope my code works the first time!")`, because that's what developers at all levels of experience hope when they run their code for the first time!

Now go into your `index.html` file and add a `<script>` tag inside the `<head>` like the other `<link>` tags. Make sure to give the script tag a `src` attribute with the file path to the `main.js` file that you just created.

To test, open `index.html` in a browser, open your Developer Tools (DevTools), click on the Console tab, and refresh the page. You should see the message you logged!

If you don't see it, you've found your first bug! You can debug your code by reviewing your HTML and JS, or by checking your Console. It's possible you might see an error in your Console like:

> GET bloop-a-de-doop-doop/main.js net::ERR_FILE_NOT_FOUND

Errors like these may be daunting at first, but if you read through the error message you'll see clues like, `net::ERR_FILE_NOT_FOUND`. Google errors you see in your Console to see what you find! Most developers frequently use sites like Google and Stack Overflow to help them research and solve problems. So when in doubt, Google! Based on what you learn when you search, you can try adjusting your source files and then refresh the web page you're debugging.

If you still can't get your `console.log(...);` to appear, use that Slack channel to ask for help :)

### Challenge 2: Playing with Variables.

> Introduction to JavaScript: [Variables](https://www.codecademy.com/courses/introduction-to-javascript/lessons/variables/)

Codecademy taught three ways to create variables: `var`, `let`, and `const`:

```
var name = "Beyoncé"; // Old way of declaring, or creating, variables

let newName = "Bey"; // New way of declaring variables that can reassigned later
newName = "Sasha Fierce"; // Example of newName being reassigned
const song = "All the Single Ladies"; // New way of declaring variables that cannot be reassigned
song = "All the Single Maladies"; // Not only is this a terrible pun, it will throw an error, "TypeError: Assignment to constant variable."
```

In your `main.js` file, create some variables to represent different information about a teacher. You can name the variables however you like, however most variables are written in `camelCase` to show multiple words, in this case "camel case".

- Create a teacher name variable to store a String with a full name.  
- Create a department variable to store a String with a department name.   
- Create a rating 1, 2 and 3 variable to store different "float" Numbers between 0.0 and 5.0.

Now print a message to the Console (using `console.log(...);`) using all of the variables you just declared.

Bonus points for making your `console.log(...);` output easy to read, like:

>Teacher: Sally Jones  
Department: Physics  
Ratings: 3.4, 5.0, 4.0  

To test, refresh your page and look at your DevTools Console.

### Challenge 3: Do a little math.

> Introduction to Javascript: [Variables - Mathematical Assignment Operators](https://www.codecademy.com/courses/introduction-to-javascript/lessons/variables/exercises/mathematical-shortcuts)

Now, calculate an average of your three ratings and store it in a variable called, `avgRating`. To calculate an average, simply add the three ratings from the last challenge and divide their sum by three!

Update your print out statement. It might look something like this:

>Teacher: Sally Jones  
Department: Physics  
Ratings: 3.4, 5.0, 4.0
Avg Rating: 4.133333333333334

Tricky part, round your `avgRating` to the nearest 5th place decimal...definitely use Google!

### Challenge 4: Variables to Represent Student and Course Data!

Now to take what you've learned and test it out a couple more times! You just created variables that represented the data used on the teachers page. But what about the students and courses data? You should create variables to represent one student and one course as well.

First, make sure your JavaScript file is linked to both of those `.html` files. After you link them all, you should be able to see the same `console.log(...);` output when you look at your DevTools Console.

Then, make a list of data used on those pages and create variables to represent them. Make sure the data type you use (such as a string, int, or float) best represents the data you're trying to store.

After you create the variables, print them in your Console just like you did with the teacher data.

THE END.

Phew, that was a lot! In the next part, you'll get to build on all the work you just created!
