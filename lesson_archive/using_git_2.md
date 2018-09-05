---
title: Using Git 2
permalink: /using_git_2
---

# Using Git: Branching and Collaboration

### Intro
The goal of this activity is to help you understand how to use git branches, how to use merge/rebase, and how git is used in a collaboration workflow.


This activity will be done in teams. We will use the same teams as we used for the Git Cheat Sheet HTML/CSS challenge.



#### The SetUp

**Assign Roles**  

Each Team should have 2-3 team member... there are 2-3 roles in this activity... person 1, person 2, person 3... assign each person in your team to one of these roles... person 3 is optional, so if you only have 2 people... just stick with person 1 and person 2.


**Creating a Shared Repository**  

_Person 1_   
ONLY PERSON 1. Log into Github. **FORK** this repository:  
[Git Branching Activity](https://github.com/LaunchCoderGirlSTL/git_branching_activity)

In order for all team members to make changes to a github project, they need to be added as collaborators.

Navigate to the Settings > Collaborators, and add your team members.



_Person 1. Person 2. Person 3._   
Everyone should now make their own local copy of the project on their computer by cloning it.

```
git clone <your repository http address>
```

AND WE ARE NOW READY TO REALLY START!! YEAH!


#### Branching

Locally, each person is going to create a branch... you should currently have one branch `master`.

```
// to list all current branches
git branch

// to create new branch
git branch <branch-name>

// to switch branches
git checkout <branch-name>
```

**Individual Changes Part**

_Person 1. Person 2. Person 3._  
create a new branch (named whatever you want)

each person make a different change...

>person 1 - add another commiting changes command (something about adding or commiting wouldn't be a bad idea)

>person 2 - add another branching command (we just learned some things, but you can also google)

>person 3 - change some styles... like the color of something or add a description of what this site is...

once everyone has their changes added and committed on their respective branches on their local repositories... continue...


**The Collaboration - Pull Before You Push (your changes)**  

Collaborating on projects through Github ... remember master branch is the branch everyone has in common and should be the "official" version of the project. That means your changes should be done on a different branch, until you are ready to share them. When you are ready to share the changes... you need to  

1) make sure you have the latest version of "official" project (what's on the master branch) and  

2) make sure your changes are applied "on top" of the official version...

when those 2 things are complete, then you can share your changes with a merge & push.



so now that everyone has their changes... Person 1 is going to share their changes first... to do this, Person 1 will need to merge their new changes branch with the master branch and then push.


>Person 1
1. checkout master branch
2. merge with their new changes branch `git merge <branch-name>`
3. then push


Everyone should check to see if those changes made it to github before proceeding!

Great! Now it's the 2nd person's turn...

>Person 2
1. checkout master branch
2. pull to get new changes from github
3. check to make sure person 1's changes are there

At this point your commit should be behind one commit, so before you bring your change into master you want to move your change on top of person's ones new changes. To do that, we use a rebase.

> Person 2
1. checkout your new branch
2. rebase this branch onto the master branch
3. check to make sure the site has YOUR changes AND PERSON 1 changes

If everything is good you are ready to proceed! and push your changes now!

> Person 2
1. checkout the master branch
2. merge with your new branch
3. push to github

Check to make sure those changes made it to github!!!

Does your group have a Person 3?! If so repeat the same process you did for Person 2, to get Person 3's changes up to github...


Now everyone... to make sure you have all the latest changes to your git_cheat_sheet_collaboration project... checkout the master branch and pull...

if the branch you just created doesn't have any new changes on it anymore... feel free to delete.



**To Complete this activity... make sure everyone can see all the team member's changes locally on their own computer :)**
