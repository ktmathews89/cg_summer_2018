---
title: Javascript Challenges I
permalink: /lesson_8/2_js_challenges_part_1
---


# DO NOT START THIS PROJECT, IT WAS A TERRIBLE IDEA and you should move to the next lesson instead.

# Javascript Challenges I - Variables, Conditionals, Functions & Scope

**Plan:** List steps/tasks in [Trello Boards](https://trello.com/cg_webdev_ss_2018)

**Do:** Download app to your phone and play (instructions below).

**Record:** [Lesson 9.2 - JS Adventure Challenge](https://learn.launchcode.org/courses/131/assignments/7554)


## Goals
1. Setup JS Adventure Project.
2. Complete Challenge 1
3. Record completion on canvas


### Setup

Following the setup instructions for the project located in the github repository:

[JS Adventure GitHub repository](https://github.com/ktmathews89/js_adventure)


### Challenge 1

Challenge 1 is made up of three problems. To Complete this assignment solve each of the 3 problems.

Before you start we are going to do some git magic so you can see the challenge 1 problems. After you have cloned the repo, you should be on the "remote" branch called master. We need to more to the remote branch called 'ch1'. That will have the first challenges we need. To do that, open your terminal, navigate into the js_adventure project directory. Then do the following commands:

```
git checkout origin/ch1
```

Then:

```
git checkout -b ch1
```

Now you should be ready to code!

The only place you will be writing code is in the `index.js` file. All the problems you see listed below are listed in that file as well.

This can be confusing, so reach out if you need help!


#### Problem 1 - Make the spaceship move

**Problem:** The control keys are broken. We can see we are pressing a key because the keys are lighting up in the control panel on the bottom of the game, but the spaceship isn't moving. Let's fix that.

**To Solve:** Add logic to the arrowPressed function so that based on the key value passed in the appropriate spaceship move function will be called. The spaceship has 4 move functions, moveRight, moveLeft, moveUp, moveDown. You can called them like: spaceship.moveRight().

The key parameter is a string and will be one of 4 values:
'ArrowUp', 'ArrowDown', 'ArrowRight', 'ArrowLeft'


#### Problem 2 - Next Level isn't incrementing levels

**Problem:** After you land the spaceship... the next level button should move you up to the next level. But currently it's just doing the same thing as reset level does... resets the current level.

**To Solve:** Add logic to the `nextLevelBtnPressed` function. This function should increment the current level, but only if the spaceship is landed and we have not reached the highest level yet. If we are at the highest level... current level should be to a game over value. If game over or the spaceship has not landed, current level should not be updated.

`levels` has some properties you should use to complete this problem:

* setCurrentLevel(level) - a function, that will change the current level
* getCurrentLevel() - a function, that will give you the current level
* HIGHEST_LEVEL - a const, is the highest level a player can complete
* GAME_OVER - a const, that is the level that represents completion of game


#### Problem 3 - Update scroll message after each level

**Problem:** So we fixed the next level button, but the message in the scroll box isn't changing. It's suppose to change each time the next level is updated. Let's fix that.

**To Solve:** First create a function called `getMessage` that takes one input (or parameter) a level. And outputs or returns a string with the appropriate message. This function should meet the following cases:

```
     INPUT       OUTPUT  
     -------     -----------  
        1        'LEVEL 1'  
        2        'LEVEL 2'  
        3        'LEVEL 3'  
        4        'GAME OVER'  
```

Then after you have your function created and working. We are going to use it in the function you solved in problem 2. Let's add some more logic to that.

After the level is updated... set messageBox.innerHTML variable to the output of our getMessage function... make sure to pass into the function the new level.

Make sure to test the game... every time you click next level... you should see the scroll message update to the correct level number and then game over after the 3rd level.


Once all three problems are complete and the game is working... you are done!

### Record

Don't forget to record completion on canvas.
