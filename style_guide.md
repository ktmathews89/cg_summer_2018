---
title: Style Guide
permalink: /style_guide
---

Since it is fairly rare these days for a developer to always work alone, as a team we need to follow a style guide. No, this has nothing to do with your CSS, this is how we are going to structure your code so that it is easily readable.

## Things to follow:

### Indention

**HTML**

Good:

```html
<div>
  <h1>Hello</h1>
  <p>
    Lots of words. Lots of words. Lots of words. Lots
    of words. Lots of words. Lots of words. Lots of
    words. Lots of words. Lots of words.
  </p>
  <ul>
    <li>Short</li>
    <li>
      Lots of words. Lots of words. Lots of words. Lots
      of words. Lots of words. Lots of words.
      </li>
  </ul>
</div>
```

Bad:

```html
<div>
<h1>Hello</h1>
<p> Lots of words. Lots of words. Lots of words. Lots of words. Lots of words. Lots of words. Lots of words. Lots of words. Lots of words.  </p>
<ul>
  <li>Short</li>
  <li> Lots of words. Lots of words. Lots of words. Lots of words. Lots of words. Lots of words.  </li>
</ul>
</div>
```

**CSS**

Good:

```css
.main {
  background-color: #eeeeee;
}
```

**Javascript**

Good:

```js
function hello() {
  var greeting = 'Hello CoderGirl!';
  console.log(greeting);
}
```

[Home]( /web_group_cohort )
