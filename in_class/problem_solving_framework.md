---
title: Problem Solving Framework
permalink: /1_2018/in_class/problem_solving_framework
---

# Problem Solving Framework

So we have been learning a lot of Javascript... conditionals, loops, functions... just learning the javascript syntax is challenging in itself. But *using* those javascript tools to *solve problems* is a different kind of challenge. Here we are going to talk about a framework to help you approach solving the javascript challenges that you encounter.

## 6 Step Framework for Approaching Problems

**1) Define/*UNDERSTAND* the Problem/*GOAL***  
_do I need to understand the goal better... rewrite goal with more description_

**2) List out what you *KNOW* or what you have**  
_what are you starting with... what js things do we know_

**3) Identify what you *NEED***  
_are there things I need to find before I can get to my goal_

**4) *WRITE* (in words) Individual *STEPS***  
_how do we get what we need... how do we put it together... what sequence_

**5) *IMPLEMENT* the Individual Steps**  
_figure out how to write each individual step with javascript, one step at a time_

**6) *TEST* & Debug**   
_try out your implementation... might need to console.log some values_

**(optional) 7) Revise**   
_can you make your solution better... anything else you want to add_


### Real Life example

I have a book from the library that I need to return... how do I return it?

**1. Goal**

Need to take book from my house to the closest library.

**2. Know**

* I have a book.
* There is a library in St. Louis.
* I am able to get there through some mode of transportation.


**3. Need**

Figure out:
* where the library is
* my mode of transportation
* due date of book


**4. Write Steps**

```
// Google Where the Library is

// Grab book

// If library is Close
    // walk to library
// Else if weather is good
    // bike to library
// Else if have car
    // drive to library
// Else
    // take bus

// if dropbox
    // drop book in box
// else
    // return to front desk

```

**5. Implement Steps**

To implement we would attempt to return the book the library.

**6. Test & Debug**

If we successfully return the book, the solution worked! If not, like maybe that library doesn't exist. We might need to revise our solution. Like maybe the library was closed... we should probably update our steps to make sure the library is open before we leave the house.

**7. Revise**

Can we make this solution better?


So we do this kind of problem solving logic in our head through out our daily life all the time. We can apply the same problem solving logic to solving javascript challenges.


### A Code Example

We might have a javascript challenge like put the book in the correct row, given the following:
```
var bookId = 1200;

var row_1_start = 0000;
var row_1_end = 1000;

var row_2_start = 1001;
var row_2_end = 2000;

var row_3_start = 2001;
var row_3_end = 3000;

var row1 = [ ];

var row2 = [ ];

var row3 = [ ];
```

**1. Goal**
How the goal is stated above ("put the book in the correct row") isn't the most clear phrase based on the code. We could rewrite this goal like:
```
put the bookId into the correct row array based on the bookId value
```

**2. Know**

* book id is 1200
* the range of ids that belong in each row
* 3 different row arrays that we could put the book into

**3. Need**

* compare bookId to row ranges
* how to put something in an array

**4. Write Steps**

For these individual steps, it might help to start general and then try to make each one more specific. For example, we might start with:
```
// Figure out which row the books goes into
```

OR
```
// Compare Book Id to Row ranges
```

Then we can actually start making things more specific:
```
// if book id less than row 1 end #
    // put in row1

// else if book id less than row 2 end #
    // put in row2

// else if book id less than row 3 end #
    // put book in row3

// else
    // error: can't put book away
```

Okay now this looks like something we could start writing code for.


**5. Implement Steps**

Now it's time to start implementing each individual step. One thing at a time, so we can just focus on the if-else statements first.
```
// if book id less than row 1 end #
if (bookId <= row_1_end){
    // put in row 1

} else if (bookId <= row_2_end){
    // put in row 2

} else if (bookId <= row_3_end){
    // put in row 3

} else  {
    console.log("error: book donated!");
}
```

Now let's add the book to the row
```
// if book id less than row 1 end #
if (bookId <= row_1_end){
    row1.push(bookId);

} else if (bookId <= row_2_end){
    row2.push(bookId);

} else if (bookId <= row_3_end){
    row3.push(bookId);

} else  {
    console.log("error: book donated!");
}
```

YEAH! That is looking pretty good. But now we need to test it to see if our solution works.

**6. Test & Debug**

To test and debug in javascript, it is very helpful to use console.log statements. Let's add some to our code so we can figure out what is going on.

```
console.log("Book: " + bookId);

// if book id less than row 1 end #
if (bookId <= row_1_end){
    row1.push(bookId);
    console.log("added book to Row1!");

} else if (bookId <= row_2_end){
    row2.push(bookId);
    console.log("added book to Row2!");

} else if (bookId <= row_3_end){
    row3.push(bookId);
    console.log("added book to Row3!");

} else  {
    console.log("error: book donated!");
}
```

Does it work? Are there problems? What if we change the bookId to 3001 or 100. Do those values go in the correct row? If everything is working correctly YAY! If not, try to use the console.log statements to see what is going wrong.


**7. Revise**

What if we had 3 books we wanted to place in the correct rows? We could make this logic reusable with a function. It's not necessary to solve the problem but definitely an upgrade.

So our final solution might look something like this:

```
// Challenge: put a book away in the correct row based on id

// var bookId = 3001;

var row_1_start = 0000;
var row_1_end = 1000;

var row_2_start = 1001;
var row_2_end = 2000;

var row_3_start = 2001;
var row_3_end = 3000;

var row1 = [ ];

var row2 = [ ];

var row3 = [ ];

function returnBook (bookId){
    console.log("Returning Book Id: " + bookId);

    // if book id less than row 1 end #
    if (bookId <= row_1_end){
        // put in row 1
        row1.push(bookId);
        console.log("added book to Row1!");

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
}

var booksToReturn = [700, 2, 2018, 700, 2, 2018, 700, 2, 2018 ,700, 2, 2018, 700, 2, 2018, 700, 2, 2018];

for (var i = 0; i < booksToReturn.length; i++){
    returnBook(booksToReturn[i]);
}

```


### Conclusion

Thinking about challenges this way, thinking through and breaking down the larger problem into small actionable steps is very helpful. Especially when using a new language. By writing out steps BEFORE you start writing javascript syntax, makes it easier to figure out which javascript tools you need to use.

Try it out in your challenges and see if it helps!
