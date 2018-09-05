# Exercise: Cat Costume Project: Part 2

**Plan:** List steps/tasks in [Trello Boards](https://trello.com/cg_webdev_ss_2018)

**Do:** Build a mobile-first website from a design.

**Record:** [INSERT LINK HERE](http://bomb.com)

## Intro
You just set up your Git repository following [Part 1](/cg_summer/2018/lesson_6/3_cat_project_1)!

Remember to make Git commits frequently as you code. The benefits of commit often are many, including rolling back your code to a version that worked a little better in the past.

Now, you're ready to start coding the mobile-first website. If you haven't already taken the [Udacity Responsive course](https://classroom.udacity.com/courses/ud893) yet, it's okay. There are prompts below to indicate which lessons you should review in order to complete the challenges.

You can also learn why people choose mobile-first here: [ZURB](https://zurb.com/word/mobile-first).

## Goals
1. Continue to make Git commits to your local repository
2. Build a mobile-first website from someone else's designs
3. Use media queries to create a responsive website experience
4. Learn how to use CSS classes effectively

## Challenge 1: Review the designs
You will be working on the mobile version of the site first. But, take a look at both of the _mobile and desktop_ design files for this project. (They are located in the `/design` directory.) Keep the desktop version of the site in the back of your mind.

The cat costume site uses Google Fonts named PT Sans Narrow, PT Sans Narrow Bold, PT Serif, and PT Serif Bold. The design also features a number of colors you should use. Hexadecimal numbers are below for your convenience:

- #323232
- #eeeeee
- #00897f
- #f26522

Use your wireframing techniques to break the site down into repeatable chunks so you can reuse you classes and write as little repetitive CSS as possible! Pick a piece of the site to work on and go from there.


### Course Material for Challenge 2

[Take Udacity Responsive Lesson 1 and 2](https://classroom.udacity.com/courses/ud893)

## Challenge 2: Get acquainted with Fluid Layout & Responsive Widths

Since we're building mobile first, you will want to use relative percent units. But, you don't have to use relative units for ALL divs or html elements. For example, you probably want the about boxes or the Get In Touch boxes to keep a certain fixed sized.

Use your own discretion on what looks good. You definitely want each of the html sections to span the whole browser width. Also keep in mind you can use max-width and min-width.

Remember you can use both `width: 80%;` and `max-width:400px;` together. This would keep the element at 80% it's container's width, but will not ever get bigger than 400px.

## Challenge 3: Build the mobile site using HTML and CSS
First, add the below viewport meta element in your html's <head></head>. This is a viewport tag and keeps your browser from automatically zooming in on mobile (or smaller) devices.

```
<meta name='viewport' content='width=device-width, initial-scale=1.0, maximum-scale=1.0' />
```

Next, add the Google Fonts you need!

While you're coding your CSS, try to reuse as much CSS as possible. The wireframing step should help you identify common styles. Here is an example of consolidating repetitive CSS inspired by [CSS Wizardry](https://csswizardry.com/2013/07/writing-dryer-vanilla-css/):

Repetitive CSS:
```
CSS
.page--home {
    background: url(home.jpg) center center no-repeat;
}

.page--about {
    background: url(about.jpg) center center no-repeat;
}

.page--work {
    background: url(work.jpg) center center no-repeat;
}

.page--contact {
    background: url(contact.jpg) center center no-repeat;
}

HTML
<div class="page--home">...</div>
<div class="page--about">...</div>
<div class="page--work">...</div>
<div class="page--contact">...</div>
```

Notice that the only thing that is different about value of each `background` property above is the `url(...)`. We can consolidate the `center center no-repeat` into one class.

```
CSS:
.page {
    background-position: center center;
    background-repeat: no-repeat;
}

.page--home     { background-image: url(home.jpg); }
.page--about    { background-image: url(about.jpg); }
.page--work     { background-image: url(work.jpg); }
.page--contact  { background-image: url(contact.jpg) }

HTML:
<div class="page page--home">...</div>
<div class="page page--about">...</div>
<div class="page page--work">...</div>
<div class="page page--contact">...</div>
```

Now, the `background-position` and `background-repeat` CSS properties have been crunched into one class called "page". That way, we can change the position and repeat properties of all `.page` elements at once! The primary difference is that you have to add two classes to the HTML elements. One to apply the `.page` CSS properties, and another to apply the more specific `page--` background images.

#### Course Material for Challenge 4

[Take Udacity Responsive Lesson 3](https://classroom.udacity.com/courses/ud893)

In this lesson you will learn about media queries and a little about flexbox.

#### Challenge 4: Use media queries to make the site responsive

In today's world, we rarely make sites just adaptive. Usually we want the site to look good on ALL device and don't usually target just one particular device and screen size. This means we want our site to be RESPONSIVE.

**STEP 1: Make the site look good at sizes larger than 1200px.

It seems like the desktop site was designed for screen sizes of 1200px. Try to replicate the desktop design inside of a media query for widths larger than 1200px.

**STEP 2: Determine widths where site breaks down**

Start resizing your screen (by dragging in the window size) from desktop to mobile. When you notice something "break", like 2 boxes sliding under each other or elements overlapping, then make note of the window width. You can see width width in the top right hand corner of your browser window but ONLY when you have developer tools opened.

**STEP 3: Add Media Query for that Break**

Now we are going to add a media query for that particular break.

Remember media queries are structured like this:

```
@media screen and (max-width: 600px){
    // styles for screen 600px and under
}
```

> hint: the max-width should be the window width you wrote down in step 1.


**STEP 4: Fix styling of the Break**

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

Now go ahead and fix the CSS you need to inside the media query you wrote in the previous step.

**STEP 5: Repeat for all Breaks in Your site**

Repeat this process for all your sections. Keep incrementally resizing your browser to find breaks, add media queries and styles to fix those breaks. When you are done, your site should look good on ALL browsers and devices.

#### Still Confused? Or just want a Debrief of What you Learned?

Here is a nice reading with pretty images to debrief all this stuff you just did! The person who wrote it is focusing on styles changing from desktop to tablet to mobile. It would be good to skim and look at the pictures. You might pick up some tips for the next project you create :)

[Responsive Design Article](https://internetingishard.com/html-and-css/responsive-design/)
