---
title: Cat Costume 1
permalink: /cat_costume_1
---

# Cat Costume Project

### Intro
Time to start a new project! The Cat Costume Project!

This Project will help you practice using HTML & CSS as well as GIT.



#### Challenge 1: Create your File Structure and your HTML/CSS files.

**STEP 1: Create Project Directory**  
Open your terminal and navigate to the directory that you keep your programming project in (you should have created it when you created your portfolio project).

Create a new directory with the `mkdir` command called cat_costume_project.



**STEP 2: Download Starter Files**  
We set this project up for you so you can get to practicing HTML/CSS part faster.

Download these project files here:
[Cat Costume Project - GitHub](https://github.com/LaunchCoderGirlSTL/web_group_project_1)

    > click the green "Clone or Download" button.
    > click the "Download Zip" option.
    > find that downloaded zip file on your computer.
    > unzip the file by double clicking it.


Now copy and paste the contents of the "web_group_project_1-master" into your "cat_costume_project" directory. (this is probably easier to do in a Finder/Explorer window rather than the terminal).

Now you should have a project directory that looks like this:

```
cat_costume_project/
    assets/
        css/
            index.css
        images/
            (all the images you will need)

    design/
        (design files)

    index.html
    README.md
```
Open your Project In Atom.


#### Challenge 2: Initialize Git Repository

**STEP 1: Initialize Git Repo**  
Open your terminal (if not already open) and navigate to your `cat_costume_project` directory.

Make sure you are inside your project directory so `cd cat_costume_project` and when you `ls` you see the index.html file.

Use the `git init` command to initialize this project as a git repository.

Then configure your git name and email with the following commands.

```
git config --global user.name <name>
git config --global user.email <email>
```


> Initializing the directory as a git repository, allows you to use git version control on this project.

**STEP 2: Making Your First Commit**  
Use the following commands to make your first initial commit...

```
git add .
git commit -m "created project structure"
```

That's it! Now you are ready to code!

#### Challenge 3: Start Working on the HTML/CSS

Take a look at the design files for this project (located in the design folder). Pick a piece to work on and go from there. Remember to use git along the way to keep track of changes. Below is a cheat sheet to help you:

```
// what changes have been made from my previous version
git status

// stage these changes, they are pretty good and I will probably want to commit them
git add <file-path>

// commit all my staged changes because I am done with a little piece
git commit -m “this is what i changed”

// list all of my commits
git log

// undo this file change because I messed up and don't want it anymore
git checkout <file>

```
