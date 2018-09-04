# Exercise: Cat Costume Project: Part 2

**Plan:** List steps/tasks in [Trello Boards](https://trello.com/cg_webdev_ss_2018)

**Do:** Build a mobile-first website from a design.

**Record:** [INSERT LINK HERE](http://bomb.com)

## Intro
You just set up your Git repository following [Part 1](/cg_summer/2018/lesson_6/3_cat_project_1). Remember to make Git commits frequently as you code. The benefits of commit often are many, including rolling back your code to a version that worked a little better in the past.

Now, you're ready to start coding the mobile-first website. If you haven't already taken the [Udacity Responsive course](https://classroom.udacity.com/courses/ud893) yet, it's okay. There are prompts below to indicate which lessons you should complete in order to complete the challenges.

## Goals
1. Make Git commits your local repository
2. Build a mobile-first website from someone else's designs
3. Use media queries to create a responsive website experience
4. Learn how to use CSS classes effectively

## Challenge 1: Review the designs
You will be working on the mobile version of the site first. But, take a look at both of the design files for this project (located in the `/design` folder). Keep the desktop version of the site in the back of your mind.

The site uses Google Font's PT Sans Narrow, PT Sans Narrow Bold, PT Serif, and PT Serif Bold. The design also features a number of colors you should use. Hexadecimal numbers are below for your convenience:

- #323232
- #eeeeee
- #00897f
- #f26522

Use your wireframing techniques to break the site down into repeatable chunks so you can code DRY CSS! Pick a piece of the site to work on and go from there.

## Challenge 2: Start Working on the HTML/CSS
First, add the below viewport meta element in your html's <head></head>. This is a viewport tag and keeps your browser from automatically zooming in on mobile (or smaller) devices.

```
<meta name='viewport' content='width=device-width, initial-scale=1.0, maximum-scale=1.0' />
```

Next, add the Google Fonts you need!

### Course Material for Challenge 3

[Take Udacity Responsive Lesson 1 and 2](https://classroom.udacity.com/courses/ud893)

## Challenge 3: Fluid Layout & Responsive Widths

Since we're building mobile first, you will want to use relative percent units. But, you don't have to use relative units for ALL divs or html elements. For example, you probably want the about boxes or the Get In Touch boxes to keep a certain fixed sized.

Use your own discretion on what looks good. You definitely want each of the html sections to span the whole browser width. Also keep in mind you can use max-width and min-width.

Remember you can use both `width: 80%;` and `max-width:400px;` together. This would keep the element at 80% it's container's width, but will not ever get bigger than 400px.

#### Course Material for Challenge 4

[Take Udacity Responsive Lesson 3](https://classroom.udacity.com/courses/ud893)

In this lesson you will learn about media queries and a little about flexbox.

#### Challenge 4: Use Media Queries to Help with "Breaks"

In today's world, we rarely make sites just adaptive. Usually we want the site to look good on ALL device and don't usually target just one particular device and screen size. This means we want our site to be RESPONSIVE.

**STEP 1: Determine widths where site breaks down**

Start resizing your screen (by dragging in the window size) from big to small. When you notice something "break", like 2 boxes sliding under each other or elements overlapping, then make note of the window width. You can see width width in the top right hand corner of your browser window but ONLY when you have developer tools opened.


**STEP 2: Add Media Query for that Break**

Now we are going to add a media query for that particular break.

Remember media queries are structured like this:

```
@media screen and (max-width: 600px){
    // styles for screen 600px and under
}
```

> hint: the max-width should be the window width you wrote down in step 1.


**STEP 3: Fix styling of the Break**

The desktop design might help you out here a little, but if spots break down before the mobile design should kick in... you should determine a good solution on your own to keep the design looking good.

Anyways, inside the media query is where you want to fix the styles that break.

For example, if you wanted to something to appear side by side like this:

X X

when the browser is greater than 700px BUT then display top and bottom like this:

X  
X

when the browser is less than 700px in width... Your code would look like this:

```
.box {
    width: 300px;
    display: inline-block;
}

@media screen and (max-width: 700px) {
    .box {
        width: 90%;
        display: block;
    }
}
```

Now go ahead and fix the css you need to inside the media query you wrote in the previous step.


**STEP 4: Repeat for all Breaks in Your site**

Repeat this process for all your sections. Keep incrementally resizing your browser to find breaks, add media queries and styles to fix those breaks. When you are done, your site should look good on ALL browsers and devices.

#### Still Confused? Or just want a Debrief of What you Learned?

Here is a nice reading with pretty images to debrief all this stuff you just did! The person who wrote it is focusing on styles changing from desktop to tablet to mobile. It would be good to skim and look at the pictures. You might pick up some tips for the next project you create :)

[Responsive Design Article](https://internetingishard.com/html-and-css/responsive-design/)