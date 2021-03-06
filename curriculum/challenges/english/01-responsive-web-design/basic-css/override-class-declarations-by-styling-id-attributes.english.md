---
id: bad87fee1348bd8aedf06756
title: Override Class Declarations by Styling ID Attributes
challengeType: 0
videoUrl: 'https://scrimba.com/c/cRkpDhB'
---

## Description
<section id='description'>
We just proved that browsers read CSS from top to bottom in order of their declaration. That means that, in the event of a conflict, the browser will use whichever CSS declaration came last. Notice that if we even had put <code>blue-text</code> before <code>pink-text</code> in our <code>h1</code> element's classes, it would still look at the declaration order and not the order of their use!
But we're not done yet. There are other ways that you can override CSS. Do you remember id attributes?
Let's override your <code>pink-text</code> and <code>blue-text</code> classes, and make your <code>h1</code> element orange, by giving the <code>h1</code> element an id and then styling that id.
</section>

## Instructions
<section id='instructions'>
Give your <code>h1</code> element the <code>id</code> attribute of <code>orange-text</code>. Remember, id styles look like this:
<code>&#60;h1 id="orange-text"&#62;</code>
Leave the <code>blue-text</code> and <code>pink-text</code> classes on your <code>h1</code> element.
Create a CSS declaration for your <code>orange-text</code> id in your <code>style</code> element. Here's an example of what this looks like:
<blockquote>#brown-text {<br>&nbsp;&nbsp;color: brown;<br>}</blockquote>
Note: It doesn't matter whether you declare this CSS above or below pink-text class, since id attribute will always take precedence.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your <code>h1</code> element should have the class <code>pink-text</code>.
    testString: assert($("h1").hasClass("pink-text"), 'Your <code>h1</code> element should have the class <code>pink-text</code>.');
  - text: Your <code>h1</code> element should have the class <code>blue-text</code>.
    testString: assert($("h1").hasClass("blue-text"), 'Your <code>h1</code> element should have the class <code>blue-text</code>.');
  - text: Give your <code>h1</code> element the id of <code>orange-text</code>.
    testString: assert($("h1").attr("id") === "orange-text", 'Give your <code>h1</code> element the id of <code>orange-text</code>.');
  - text: There should be only one <code>h1</code> element.
    testString: assert(($("h1").length === 1), 'There should be only one <code>h1</code> element.');
  - text: Create a CSS declaration for your <code>orange-text</code> id
    testString: assert(code.match(/#orange-text\s*{/gi), 'Create a CSS declaration for your <code>orange-text</code> id');
  - text: Do not give your <code>h1</code> any <code>style</code> attributes.
    testString: assert(!code.match(/<h1.*style.*>/gi), 'Do not give your <code>h1</code> any <code>style</code> attributes.');
  - text: Your <code>h1</code> element should be orange.
    testString: assert($("h1").css("color") === "rgb(255, 165, 0)", 'Your <code>h1</code> element should be orange.');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
</style>
<h1 class="pink-text blue-text">Hello World!</h1>
```

</div>



</section>

## Solution
<section id='solution'>

```js
// solution required
```
</section>
