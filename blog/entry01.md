# Entry 1
##### 11/3/2025

### Hello everyone,My name is Alialrida ELhgae and I am a 11th grade student in Telecommunication's software engineering program and this right now is my second year in the program and I am currently working on my sep 11 freedom-project so I right now I want to talk about my experience in my first year but today I will be talking about the tool I've decided on,why I choose it,how I tinkered with it,what am I going to make with the tool and finally where I got the information for the tool where I would explain what my tool is.

#### <ul>
#### <li>What tool did I decide on?; I decided to work the mild,one flaming emoji level tool Less.js.</li>
#### <li>Why did I choose Less.javascript ?; I choose Less.js to work with as I had a difficult time back in Sep 10 and I ended the year of with a 67% as my avergae in Sep 10 so I choose this tool as its an easy tool from what I saw on the list so I decided I would choose that tool.</li>
#### <li> How I tinkered with Less.javascript ?; While I haven't tinkered with it much I tinker with it in my IDE in a file in the tool folder of the sep11-freedom-project folder of my projects folder in my entire IDE that for this year is named javascript or js.
#### </ul>

### Link to the website of Less.js where it explains the code needed so it can be used in web development:https://lesscss.org/ .

### Here are my code snippets and these shall explain my current skills,edp and professionalism with Less.js by themselves withput me needing to write anything;
``` script.js

// 11/10/2025
@base: #f04615;
@width: 0.75;

.class {
  width: percentage(@width);
  color: saturate(@base, 8%);
  background-color: spin(lighten(@base, 30%), 10);
} //Functions

#bundle() {
  .button {
    display: block;
    border: 2px solid green ;
    background-color: blue;
    &:hover {
      background-color: red;
    }
  }
  .tab { ... }
  .citation { ... }
} //Namespaces and Accessors
// 11/17/2025
// Variables
@width: 11px;
@height: @width + 11px;

#header {
  width: @width;
  height: @height;
}
// Output is;
#header {
  width: 10px;
  height: 20px;
// Mixins;
.bordered {
  border-top: dotted 4px black;
  border-bottom: solid 5px black;
}
// And we want to use these properties inside other rule-sets. Well, we just have to drop in the name of the class where we want the properties, like so:
#menu a {
  color: #234;
  .bordered();
}

.post a {
  color: orange;
  .bordered();
}
//The properties of the .bordered class will now appear in both #menu a and .post a. (Note that you can also use #ids as mixins.).
// Let's say we have the following CSS:
#header {
  color: black;
}
#header .navigation {
  font-size: 14px;
}
#header .logo {
  width: 400px;
}
//In Less, we can also write it this way:
#header {
  color: black;
  .navigation {
    font-size: 12px;
  }
  .logo {
    width: 300px;
  }
}
//The resulting code is more concise, and mimics the structure of your HTML.
//Here's the classic clearfix hack, rewritten as a mixin (& represents the current selector parent):
.clearfix {
  display: block;
  zoom: 1;

  &:after {
    content: " ";
    display: block;
    font-size: 1;
    height: 1;
    clear: both;
    visibility: hidden;
  }
}

```
### Notes from my Learning log about Less.js;
### 11/10/2025
### So I already used two forms of code in tinkering.md which are practice code structures from https://lesscss.org/ but I'm not sure if the results are good or bad since I've just started tinkering with them the first one is functions and let me sight wording from the website:"Less provides a variety of functions which transform colors, manipulate strings and do maths. They are documented fully in the function reference.Using them is pretty straightforward.".The next up is Namespaces and Accessors and heres the description from the website:"Sometimes, you may want to group your mixins, for organizational purposes, or just to offer some encapsulation. You can do this pretty intuitively in Less.".This is what I have so far.
### 11/17/2025
### So I decided to lock in and began learning about Less.js.So Less.js is also knwon as Leaner Style Sheets which is a backwards-compatible language extension for CSS. This is the official documentation for Less, the language and Less.js, the JavaScript tool that converts your Less styles to CSS styles.The Variables of Less.js are pretty self explanatory as they are like the code for CSS.Next up is Mixins which are a way of including ("mixing in") a bunch of properties from one rule-set into another rule-set.Next up is Nesting where less gives you the ability to use nesting instead of, or combine with CSS.You can also bundle pseudo-selectors with your mixins using this method. 

### So this is the end of my first blog for my sep11 freedom-project,we shall meet again my faithful readers once the need to make another blog apperas so goodbye and I hope you all read my next blog and can understand me better and my future skills,edp and professionalism with Less.js will improve so you can understand them better. Goodbye .

[Next](entry02.md)

[Home](../README.md)
