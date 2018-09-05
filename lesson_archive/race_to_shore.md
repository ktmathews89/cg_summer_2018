---
title: Race To Shore
permalink: /race_to_shore
---

# Race To Shore - In-Class Javascript Objects

### Intro
This in-class challenge is to help you think about objects. How to create them, how to use them and how to model real things with them.

To start, follow the below link to the github project, FORK and CLONE to you local computer.

[GitHub Race To Shore Starter Template](https://github.com/ktmathews89/race_to_shore)

> To fork and clone the project, first navigate to the link.

> Click the "Fork" button just below the nav bar on the right hand side.

> Then after it clones, click the "Clone or Download" green button, copy the https link.

> Then open your terminal on your computer, navigate to the directory where you keep all your codergirl project and enter:

> git clone (paste the url you just copied)

> Then you should see the race_to_shore directory.

> Open the race_to_shore directory in atom and open the index.html file in your browser.


### Activity Planning
You are going to create an object prototype that represents a real life thing. We are going to use that object you create to race. First you need to brainstorm and plan (a pen and paper might be helpful for this).

There are a couple of requirements that your model must have, but the rest is up to you! Feel free to be as creative as you want. Since we are going simulate your object moving across water, your object must have:

1. a property called distanceFromShore
2. an action called moveCloserToShore


**STEP 1: Think of a Model**

Write down the name of an object that you could model in your Javascript that has the ability to cross through water (ex. boat).

**STEP 2: Think of Properties**

Now write down some properties that object might have... so for a boat I might use properties like name, sails, motor.

**STEP 3: Think of Actions**

Now write down some actions that object might have. These actions should adjust the properties of the object. So for a boat I might write down "openSails". You might have to go back and edit your properties as well. For example, if I want an openSails action for my boat, I would also need a property to represent that, like an "areSailsOpen" property that is a boolean.


### Code Your Object

Now it's time to turn your model into a Javascript Object! YEAH! If you look in the project that you just cloned... in the js file there is a commented section to do this called "Your Object Definition".

**STEP 1: Create an Object literal for your Model**

Object literals are objects just defined with { }.
```
var nameOfYourObject = {
    // properties go here
};
```

**STEP 2: Add Object Properties**

Time to add all the properties you wrote down during your planning session. Remember properties can store any type of javascript value.

Make sure to add the required property, `distanceFromShore` and set it to an integer of your choice. Has to be a positive number and greater than 5.

**STEP 3: Add Object Actions as Property Functions**

This part might be a little more challenging. Making properties that are functions looks pretty much like the other property definitions except you use an anonymous function for the value.

```
var nameOfYourObject = {
    // other properties here

    openSails: function (){
        // write what you want your function to do in here
    },
}
```

> note: anonymous functions don't need a name, because you use them through their variable or in this case the property name. so if I wanted to call the openSails function I would call: `nameOfYourObject.openSails()`

When writing the inside functions, keep in mind that if you need to change or use other properties within the function, you should just the keyword `this.propertyName`.

> note: the `this` keyword is just a reference to the "thing" that is calling the function.

> Since we call the function with `nameOfYourObject.openSails()`, this refers to your object, nameOfYourObject...

> And since you would access its properties through the dot operator, like `nameOfYourObject.numOfSails`

> You would then access the numOfSail property in a property function like `this.numOfSails`

So inside the openSails function, if I wanted to print the numOfSails, it would be like this:

```
var nameOfYourObject = {
    // other properties here
    numOfSails: 2,

    openSails: function (){
        console.log(this.numOfSails);
    },
}
```

Make sure to add the required action, `moveCloserToShore`. This should be a function that subtracts some integer from the `distanceFromShore` property. The amount it subtracts is up to you!

Alright! Our object should be ready to go now!! Let's connect it to the rest of the code.


### Connect Your Object to the Running Race Code

You should see this code Running Race Code section of the js file:

```
var racer;

function runRace()
{
    // TODO: fill code here
}

function resetRace()
{
    // TODO: fill code here
}
```

We are going to fill it in during the next steps.


**STEP 1: Set the Racer to be your Object**

This should be something like:
`var racer = nameOfYourObject;`

In the runRace function and the resetRace function we are going to refer to your object as racer :)


**STEP 2: Fill in the runRace function**

This function should call your racer's moveCloserToShore function until your racer's distanceFromShore is equal or greater than 0.

Each time your call your racer's moveCloserToShore function, print to the console the distanceFromShore.

Then when the racer reaches shore (distanceFromShore is equal to or less than 0), print to the console "FINISHED RACE".


**STEP 3: Fill in the resetRace function**

This function should set your racer's distanceFromShore back to what it was originally. Make it at least greater than 5.


Okay. Let's Test!


### Run It

The buttons that display in html browser, should be connected to your code. So open the index.html in a browser. Open the console log. And click the Run Race button.

Do you get what you expect in the console?
Does your racer finish the race?

When you click the Reset Race and Run Race, does the race start again?

You might need to debug and rework somethings! Once it's working you are done. We will come back to this project to make it fancy and cool.
