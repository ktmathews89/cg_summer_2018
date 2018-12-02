---
title: Use Ajax
permalink: /1_2018/lesson_11/1_use_ajax
---

# Using AJAX

Now you should know:
* AJAX is used to retrieve data from a url
* the data is usually formatted with JSON
* we can just the jquery `$.get()` function to retrieve data from a url and do something with it

YAY! Let get to it.

**Goal:** The goal of this exercise is to use a public API (meaning you don't need any permissions to access the data) to grab data and display it on a web page with jQuery.

## Build A Mini App With an API

There are a lot of public APIs out there that you can use to build an web application. We have a pre-build idea for you below.  However, there are A BUNCH of fun APIs out there... If you want to forge your own path ahead, feel free to browse through the below APIs and create you own mini application! You might be able to apply some of the guidelines below with your own twist.

[Donald Trump Quotes](https://docs.tronalddump.io/)

[Dad Jokes](https://icanhazdadjoke.com/api)

[NBA Stats](https://any-api.com/nba_com/nba_com/docs/_teamgamelog/GET)

[Robot Avatars](https://robohash.org/)


Anyways! I spent way too long looking through those... okay. Ready to build something! If you are just going to proceed with the application we designed, a Trivia App... continue below.


## Build A Trivia App With an API

For this project, we are going to build a mini trivia api game. The styles and look are all up to you, but I have some minimum requirements listed below.

1. Users should be able to see a question
2. Users should be able to click a button to see correct answer
3. Users should be able to retrieve the next (new) question

... like so:


<img src="../../images/trivia_api.gif" />


For this project, we are going to use a Trivia API, called [Open Trivia Database](https://opentdb.com/api_config.php).

Go ahead and look through it... They give you some form fields to fill out with your preferences. Then when you click the "Generate API URL" button at the bottom, it will give you the url to use for you ajax request.

Something like, `https://opentdb.com/api.php?amount=1`.

Which will return you a JSON object like:
```
{
    "response_code":0,
    "results":[
        {
            "category":"Art",
            "type":"multiple",
            "difficulty":"hard",
            "question":"Which of these is not an additional variation of the color purple?",
            "correct_answer":"Kobicha",
            "incorrect_answers":["Byzantium","Pomp and Power","Palatinate"]
        }
    ]
}
```

This JSON data is what you will use to populate your questions and answers! YAY!


### Project Setup

This should be pretty typical by now... but go ahead and setup your project folder where ever you keep your other CoderGirl projects. In that project directory go ahead and create the three following files (with the starter code):
* index.html
* main.css
* main.js

**index.html**
```
<!DOCTYPE html>
<html>
<head>
    <title>Trivia Game</title>
    <link rel="stylesheet" type="text/css" href="main.css">
    <meta content="width=device-width,maximum-scale=1.0,initial-scale=1.0,minimum-scale=1.0,user-scalable=yes" name="viewport">
</head>
<body>

    <!-- Ready to Code! -->

    <script src="https://code.jquery.com/jquery-3.2.1.min.js" integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=" crossorigin="anonymous"></script>
    <script src='main.js'></script>
</body>
</html>
```

**main.css**
```
// the styles are all up to you!
```

**main.js**
```
$(document).ready(function(){

// Ready to Code!

});
```

### Project Challenges

**Challenge 1: Code Your HTML/CSS**

We need to code something nice to display our questions and answers text. Start by mapping out your html and css.

Suggestion: While you are laying everything out use placeholder text for your question and answer text so you can get all the style stuff done. You can remove it later.

Suggestion: Keep in mind that originally the correct answer will be hidden. But you still need a place to put it and styles associated with it.


**Challenge 2: Button Toggle**

Time to use that jQuery knowledge! Make the "See Answer" and "Next Question" buttons work.

To start out, the correct answer and the next question button should be hidden.

When user clicks the "See Answer" button, it should hide the "See Answer" button AND show the answer text along with the "Next Question" button.

When the "Next Question" button is click, it should return to the start state.

Refer to the GIF if you need reminding how this functionality is suppose to work.


**Challenge 3: Get Question Data from API**

Now it's time to use AJAX an API url to grab question data.

Go back to the [Open Trivia Database](https://opentdb.com/api_config.php) to generate a url. Make sure to only retrieve ONE QUESTION at a time.

Once you have your url to make a request to, it's time to use an AJAX function to retrieve data for your js file to use.

I would recommend using the jQuery `$.get()` function like below:

```
$.get('<url-goes-here>', function (data){
    // do things with the data you receive here
});
```

Once you get that get call working, use jquery to populate the question and answer text in you html! YAY! we are getting so close...


**FINISH**

What still isn't working like the gif? Try to problem solve your way to the solution!  

Once your have your project working... you are don! Unless you are feeling motivated and having fun. Then maybe you can implement some of the BONUS Challenges.


### BONUS Challenges

These bonus challenges are just ideas! No pressure. You might see your own ways to improve the mini app.


**Challenge: Make Multiple Choice**

In the Open Trivia API there is an option to only retrieve multiple choice questions. Update your AJAX call to use a new url that only retrieves one multiple choice question at a time.

Then display the question and all options as buttons for the user to guess.

When user clicks the correct answer button,
Then display correct!
And display the correct answer.

When the user clicks a wrong answer button,
Then display wrong!
And display the correct answer.

This is a hard one! but if you can do it YAY!
