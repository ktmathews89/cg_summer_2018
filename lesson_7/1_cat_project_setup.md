---
title: Cat Project Setup - Part 1
permalink: /lesson_7/1_cat_project_setup
---

# Cat Project Setup: Part 1

**Plan:** List steps/tasks in [Trello Boards](https://trello.com/cg_webdev_ss_2018)

**Do:** Build a mobile-first website from a design.

**Record:** [Lesson 7.1 - Cat Project Setup - Part I](https://learn.launchcode.org/courses/131/assignments/7047)

## Intro
Time to start a new project! The Cat Costume Project! This Project will help you practice using GIT, HTML, and CSS.

## Goals
1. Make Git commits your local repository
2. Build a mobile-first website from someone else's designs
3. Use media queries to create a responsive website experience
4. Learn how to use CSS classes effectively

The material for this exercise is broken up in to two parts:
- Part 1 - this page: Setting up your Git repository
- [Part 2](./2_cat_project_challenges): Starting your responsive website

So start here!

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
Open your terminal (if not already open) and navigate to your `cat_costume_project` directory.

Make sure you are inside your project directory so `cd cat_costume_project` and when you `ls` you see the index.html file.

Use the `git init` command to initialize this project as a git repository.

Then configure your git name and email with the following commands.

```
git config --global user.name <name>
git config --global user.email <email>
```


> Initializing the directory as a git repository, allows you to use git version control on this project.

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

Did you notice the two `use "git add <file>..."`? Usually Git tries to suggest next steps. So if you find yourself getting stuck make sure to carefully read the message from Git.

Git mentioned there are untracked files present. That's because you _just_ initialized this repository and Git doesn't know which files to track! You can tell Git which files to track using `git add <file>` (`<file>` is a placeholder for any filepath).

Ok, let's add _all_ of the files in your directory. You should be inside of `cat_costume_project`.

```
git add .
```

The `.` in `git add .` tells Git to add every file in the project directory for tracking.

Run `git status` again to see what you've added.

**STEP 3: Make your first commit**
Since this is a new repository, there are a lot of changes to commit! Run the following command:

```
git commit -m "Initial commit: Adds file structure."
```

> Note: Remember to run `git commit` with the `-m`like, `git commit -m "With your custom message here."`. If you don't your terminal may open it's own editor, like [vi](https://en.wikipedia.org/wiki/Vi). If that happens you _may_ be able to type `:q` to "quit" the editor.

**STEP 4: Pat yourself on your back**
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

On to [Part 2](./2_cat_project_challenges)!
