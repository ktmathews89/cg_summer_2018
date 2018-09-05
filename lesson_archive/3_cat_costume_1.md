---
title: Cat Costume 1
permalink: /3_cat_costume_1
---

# Exercise: Cat Costume Project: Part 1

**Plan:** List steps/tasks in [Trello Boards](https://trello.com/cg_webdev_ss_2018)

**Do:** Initialize your local Git repository for the Cat Costume Project.

**Record:** [INSERT LINK HERE](http://bomb.com)

## Intro
Time to start a new project! The Cat Costume Project! This Project will help you practice using GIT, HTML, and CSS.

## Goals
1. Make Git commits your local repository 
2. Build a mobile-first website from someone else's designs
3. Use media queries to create a responsive website experience
4. Learn how to use CSS classes effectively

The material for this exercise is broken up in to two parts:
- [Part 1](/cg_summer_2018/lesson_6/3_cat_project_1): Setting up your Git repository
- [Part 2](/cg_summer_2018/lesson_6/4_cat_project_2): Starting your responsive website

## Challenge 1: Create your File Structure and your HTML/CSS files.

**STEP 1: Create Project Directory**  
1. Open your terminal
2. Navigate to the directory that you keep your programming projects in (you should have created it when you created your portfolio project)
3. Create a new directory with the `mkdir` command called `cat_costume_project`

**STEP 2: Download Starter Files**  
We set this project up for you so you can get to practicing HTML/CSS part faster.

Download these project files here:
[Cat Costume Project - GitHub](https://github.com/castavridis/web_group_project_1)

    > click the green "Clone or Download" button.
    > click the "Download Zip" option.
    > find that downloaded zip file on your computer.
    > unzip the file by double clicking it.


Now copy and paste the contents of the `web_group_project_1-master` into your `cat_costume_project` directory. (this is probably easier to do in a Finder/Explorer window rather than the terminal).

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


## Challenge 2: Initialize Git Repository

**STEP 1: Initialize Git Repo**  
Open your terminal (if not already open) and navigate to your `cat_costume_project` directory using the `cd` command.

Make sure you are inside your `cat_costume_project` directory so when you `ls` you see the `index.html` file.

Use the `git init` command to initialize this project as a git repository.

Then configure your git name and email with the following commands:

```
git config --global user.name <name>
git config --global user.email <email>
```

> Note: Initializing the directory as a Git repository allows you to use Git version control on this project.

**STEP 2: Add Files to Git**
Now, your repository has been initialized, but nothing has been added to it. Let's see what can be added to it by using `git status`.

You should see something like:

```
Untracked files:
  (use "git add <file>..." to include in what will be committed)

    README.md
    assets/
    design/
    index.html

nothing added to commit but untracked files present (use "git add" to track)
```

Did you notice the two `use "git add <file>..."`? Usually Git tries to suggest next steps. So if you find yourself getting stuck make sure to carefully read the message from Git outputs to your terminal.

In the example above, Git mentioned that there are untracked files present. That's because you _just_ initialized this repository and Git doesn't know which files to track! You can tell Git which files to track using `git add <file>` (`<file>` is a placeholder for any filepath).

Ok, let's add _all_ of the files in your `cat_costume_project` directory:

```
git add .
```

> Note: The `.` in `git add .` tells Git to add every file in the project directory for tracking.

Run `git status` again to see what you've added. You should see a long list of items. Sometimes these are colored green. Now you need to commit these updates in order to create your first version of the project.

**STEP 3: Make your first commit**
Since this is a new repository, there are a lot of changes to commit! Run the following command:

```
git commit -m "Initial commit: Adds file structure."
```

> Note: Remember to run `git commit` with the `-m`like, `git commit -m "With your custom message here."`. If you don't your terminal may open it's own editor, like [vi](https://en.wikipedia.org/wiki/Vi). If that happens you _may_ be able to type `:q` to "quit" the editor.

**STEP 4: Pat yourself on your back**

![Cheers!](https://media.giphy.com/media/609o8uNjasiJO/giphy.gif)

That's it! Now you are ready to code! As you write code, you should be using `git add`, `git commit`, and `git push` to track updates to you project.

Below is a Git cheatsheet to help you:

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

Now that you have set up your Git repository. Let's start working on your HTML and CSS.

On to [Part 2](Part 2](/cg_summer_2018/lesson_6/4_cat_project_2)!
