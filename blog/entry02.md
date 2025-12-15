# Entry 2
##### 12/15/2025

### Hello everyone,My name is Alialrida Elhgae and as you all know I am a 11th grade student in Telecommunication's software engineering program and this is my second year in right now and as you all know I am working on my sep 11 freedom-project so I right now I will talk about everything that happened past november 10th and my progreess when it came to learning my fp(freedom porject for those who don't know)Less.js.
<ul>
  <li>So firstly after November 10th I had to fix blog 1 since it didnt have a lot of information on it so I began to tinker with Less.js even more.</li>
  <li>I've been staying consitent with my learning logs past 11/10 in order to stay on top of my work.</li>
</ul>

### So anyway I will first show you all the tin kering I've been doing with my code from 11/17 to 12/8 and some of this is from the edits I did on blog 1.
```script.js
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
// 12/8/2025 tinkering.
// Rules and Bubbling of Nesting.
he at-rule is placed on top and relative order against other elements inside the same ruleset remains unchanged. This is called bubbling.

.component {
  width: 300px;
  @media (min-width: 768px) {
    width: 600px;
    @media  (min-resolution: 192dpi) {
      background-image: url(/img/retina2x.png);
    }
  }
  @media (min-width: 1280px) {
    width: 800px;
  }
}

// outputs:

.component {
  width: 300px;
}
@media (min-width: 768px) {
  .component {
    width: 600px;
  }
}
@media (min-width: 768px) and (min-resolution: 192dpi) {
  .component {
    background-image: url(/img/retina2x.png);
  }
}
@media (min-width: 1280px) {
  .component {
    width: 800px;
  }
}
// Operations
//Example of impossible conversion: px to cm or rad to %.
// numbers are converted into the same units
@conversion-1: 5cm + 10mm; // result is 6cm
@conversion-2: 2 - 3cm - 5mm; // result is -1.5cm
// conversion is impossible
@incompatible-units: 2 + 5px - 3cm; // result is 4px
// example with variables
@base: 5%;
@filler: @base * 2; // result is 10%
@other: @base + @filler; // result is 15%
//Less will operate on numbers as they are and assign explicitly stated unit type to the result.
@base: 2cm * 3mm; // result is 6cm
You can also do arithmetic on colors:
@color: (#224488 / 2); // result is #112244
background-color: #112244 + #111; // result is #223355
//From 4.0, No division is performed outside of parens using / operator.
@color: #222 / 2; // results in `#222 / 2`, not #111
background-color: (#FFFFFF / 16); //results is #101010
@var: 50vh/2;
width: calc(50% + (@var - 20px));  // result is calc(50% + (25vh - 20px))
```
### In addition to what the code looks like above below are screen shots on how it looks in my IDE;
<img width="1215" height="709" alt="Screenshot 2025-12-15 11 52 51 AM" src="https://github.com/user-attachments/assets/ffa23ca8-554e-4f7d-bb48-e183c904bf6f" />
<img width="1228" height="720" alt="Screenshot 2025-12-15 11 54 04 AM" src="https://github.com/user-attachments/assets/8d6315f2-281f-4f4c-bf27-9ee7a29d49a8" />
<img width="1212" height="709" alt="Screenshot 2025-12-15 11 54 50 AM" src="https://github.com/user-attachments/assets/bb21de83-e270-4b11-b0d8-ad40719389a7" />
<img width="1167" height="709" alt="Screenshot 2025-12-15 11 55 18 AM" src="https://github.com/user-attachments/assets/4f04859f-9d3a-4dc3-ad4f-3baf283fff46" />
<img width="988" height="344" alt="Screenshot 2025-12-15 11 55 53 AM" src="https://github.com/user-attachments/assets/c5713c99-ecd7-48de-8336-d5bc36ae9dc3" />
### Next up is what I recorded in my learning logs post 11/10/2025;
<ul>
  <li> 11/17/2025
 So I decided to lock in and began learning about Less.js.So Less.js is also knwon as Leaner Style Sheets which is a backwards-compatible language extension for CSS. This is the official documentation for Less, the language and Less.js, the JavaScript tool that converts your Less styles to CSS styles.The Variables of Less.js are pretty self explanatory as they are like the code for CSS.Next up is Mixins which are a way of including ("mixing in") a bunch of properties from one rule-set into another rule-set.Next up is Nesting where less gives you the ability to use nesting instead of, or combine with CSS.You can also bundle pseudo-selectors with your mixins using this method.</li>
  <li>12/8/2025
 So now is the time to resume the learning log.So after learning about Nesting now it is time to learn about the rules and bubbling of nesting.So nesting has rules @media and/or @supports that can be nested in the same way as selectors.Arithmetical operations +, -, *, / can operate on any number, color or variable. If it is possible, mathematical operations take units into account and convert numbers before adding, subtracting or comparing them. The result has leftmost explicitly stated unit type. If the conversion is impossible or not meaningful, units are ignored.Multiplication and division do not convert numbers. It would not be meaningful in most cases - a length multiplied by a length gives an area and css does not support specifying areas.However, you may find Less's Color Functions more useful.You can change Math setting, if you want to make it always work, but not recommended.For CSS compatibility, calc() does not evaluate math expressions, but will evaluate variables and math in nested functions.</li>
</ul>

### Now are my goal for winter break both related to to the freedom project.
<ul>
  <li>Get one hour of progress in my learning and tinkering logs form my tool Less.js which you will see in Blog 3.</li>
  <li>If this Blog gets less than a 6.5/10 to edit it with my new konwledge on Less.js with the 1 hour I did on the same day.</li>
</ul>







[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
