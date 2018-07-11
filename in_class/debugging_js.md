---
title: Debugging Javascript
permalink: /1_2018/in_class/debugging_js
---

# Debugging Javascript

Objective: Learn how to use Javascript debugging tools in Chrome Web Dev tools.

There are a couple of features in Chrome Web Dev Tools that can help you figure out what is going on with your javascript code.

The first way we learned to inspect our javascript code with `console.log` statements and the Console tab of the Web Dev Tools. We can print to the console tab variables or strings so we can see their value at a particular time. This has helped us figure out why code isn't working or problem solve where the actual error is.

We can do the same thing in the Sources tab of the web dev tools! Chrome provides us some clever tools to help use inspect our javascript code at a particular point in time.

Here you will learn about:

**break points**

Break points are used to STOP the execution of your javascript code right before the line you indicate. Every time your code goes to execute the line indicated by a break point, it will stop and give you control of how to proceed.

**steps**

After reach a break point, the step button lets the user just run the next line and stop again. Basically it lets you step through your code one line at a time!

**check variables and their scope**

Chrome provides users a panel to view any variable declared and its value. Users can also add variables to their Watch panel to key an eye on how that variable changes as they step through their code.


### Learning Material

Google has a pretty good lesson on how you can use this tool:

[Google: Getting Started With Javascript Debugging ](https://developers.google.com/web/tools/chrome-devtools/javascript/)


### InClass Discussion

In class, we talked about the code below and walked through exactly what was happening. We went through break points, steps, checking variables in Global sections and adding variable to the Watch tab.

note: We added the saySuccessful function and passed it as a parameter to the returnBook function.

This is the code, we used on 05/02/2018:
```
/* Returning Books */

var booksToReturn = [700, 2, 2018];

booksToReturn[1] = 4;

var row_1_start = 0000;
var row_1_end = 1000;

var row_2_start = 1001;
var row_2_end = 2000;

var row_3_start = 2001;
var row_3_end = 3000;

var row1 = [ ];

var row2 = [ ];

var row3 = [ ];


function returnBook (bookId, doNext){
    console.log("Returning Book Id: " + bookId);

    // if book id less than row 1 end #
    if (bookId <= row_1_end){
        // put in row 1
        row1.push(bookId);

    } else if (bookId <= row_2_end){
        // put in row 2
        row2.push(bookId);
        console.log("added book to Row2!");

    } else if (bookId <= row_3_end){
        // put in row 3
        row3.push(bookId);
        console.log("added book to Row3!");

    } else  {
        // TODO: donate - error case
        console.log("error: book donated!");
    }
    doNext(bookId);
}

var saySuccessful = function (bookId){
    alert("You did it! Returned book: " + bookId);
};

console.log(saySuccessful);

for (var i = 0; i < booksToReturn.length; i++){
    returnBook(booksToReturn[i], saySuccessful);
}
```
