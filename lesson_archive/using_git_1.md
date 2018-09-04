---
title: Using Git 1
permalink: /using_git_1
---

# Using Git: Moving a Local Repo to GitHub

### Intro
The goal of this activity is to move your local version of your portfolio project to GitHub.


#### Challenge 1: Create a GitHub Repository

**STEP 1: Login to Git Hub**  

Open GitHub in a browser. Login. Navigate to your Profile Page.


**STEP 2: Create a New Repository**  

Click on the "Repository Tab". Click the green "New" button. Name the repository the same name as the repository (project directory name... like portfolio_project) on your computer.

Click the green "Create Repository" button.

Now Leave this screen up and continue with the next instructions...


#### Challenge 2: Link Your Local Repo to the new GitHub repo.

**STEP 1: Navigate to your Local Repo with Your Terminal**  

Open you terminal and navigate to your project directory (or local repo).

Do a `git status` to make sure you don't have any outstanding changes. If you do, go ahead and make a new commit.

```
git add .
git commit -m "message about what changed"
```

**STEP 2: Add a new remote repository**
Now, go back to your github repository page (the one that you should have left up).

Copy the "HTTPS" url of the repository located in the below image:


<img width="80%" src="images/repo_clone.png" />


Then back in your terminal use the git remote command...

```
git remote add origin (url you just copied)
```

**STEP 3: Verify the remote was added**

Use the command `git remote -v` to see if the remote repo was linked correctly. The command should display
> origin 'url that you pasted' (fetch)

> origin 'url that you pasted' (push)

origin being the remote "nickname" and the url to your github repo. note: fetch and push are there stating that you have read and write access to the repository, meaning you can get changes AND make changes.


#### Challenge 3: Move your code to new GitHub repo.

**STEP 1: Push Your Code to the Remote Repo (Github)**

Now that you setup the link, you can go ahead and move your changes over to Github.

Use the `git push -u origin master` command.

> git push (remote-you-want-to-push-to) (branch-you-want-to-push)

> you only have to use -u argument the first time you push. After that you can just use the git push command.

**STEP 2: Verify that Github now has your changes**

Refresh you Github repo page. It should now look something like this:

<img width="80%" src="images/repo_push.png" />

Click the "commits" tab to see all your commits that you made locally now in the remote version of your repository!

YEAH YOU DID IT!


#### Challenge 4: Make Your Portfolio Visible

**STEP 1: Setup a Public URL with GitHub Pages**

On your repository page (like above image), click on Settings. Scroll down to the "GitHub Pages" section. In the drop down, select "master branch" and click the "Save" button. The Page should refresh. If you scroll back down to the GitHub Pages section there should be a public url for your site :)
