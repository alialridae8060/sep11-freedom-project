# Entry 3
##### 3/10/2026

### Hello everyone,My name is Alialrida Elhgae and as you all know I am a 11th grade student in Telecommunication's software engineering program and this is my second year in right now and as you all know I am working on my sep 11 freedom-project so I right now I will talk about everything that happened after Blog 2 my progreess when it came to learning my fp(freedom porject for those who don't know) tool Less.js:

<ul>
  <li>I finished learning evrytghing about my tool.</li>
  <li>I finsihed my plan for the freedom Project both in MVP and beyond MVP.</li>
  <li>Also I am going to start working on my MVP for my freedom project.</li>
</ul>

### My current learning log notes:
### After a long periods of breaks and also procrastination time to resume learning.Right now there is Escaping which allows you to use any arbitrary string as property or variable value. Anything inside ~"anything" or ~'anything' is used as is with no changes except interpolation.Less provides a variety of functions which transform colors, manipulate strings and do maths. They are documented fully in the function reference.Next up is functions where less.js provides a variety of functions which transform colors, manipulate strings and do maths.They are documented fully in the function reference.Using them is pretty straightforward.After functions we have namespaces and accessors.In namespaces and accessors sometimes, you may want to group your mixins, for organizational purposes, or just to offer some encapsulation. You can do this pretty intuitively in Less.Following namespaces and accessors we have maps you can use mixins and rulesets as maps of values.Now we have scope(nope not the phsyical scope a piece of code called scope) where scope in Less is very similar to that of CSS. Variables and mixins are first looked for locally, and if they aren't found, it's inherited from the "parent" scope.Second to last we have comments which are block style and inline.Finally there is importing where Importing works pretty much as expected. You can import a .less file, and all the variables in it will be available. The extension is optionally specified for .less files.
### 3/9/2026;
### My current tinkering notes:
``` script.js
// 3/2/2026
@min876: ~"(min-width: 876px)";
.element {
  @media @min768 {
    font-size: 2.1rem;
  }
}
// results in:
@media (min-width: 876px) {
  .element {
    font-size: 2.1rem;
  }
}
//as of Less 3.5, you can simply write:
@min876: (min-width: 876px);
.element {
  @media @min876 {
    font-size: 2.1rem;
  }
}
//In 3.5+, many cases previously requiring "quote-escaping" are not needed.
//The following example uses percentage to convert 0.5 to 50%, increases the saturation of a base color by 25% and then sets the background color to one that is lightened by 36% and spun by 64 degrees:

@base: #f04615;
@width: 0.5;

.class {
  width: percentage(@width); // returns `50%`
  color: saturate(@base, 5%);
  background-color: spin(lighten(@base, 25%), 8);
}
//Say you want to bundle some mixins and variables under #bundle, for later reuse or distributing:
#bundle() {
  .button {
    display: block;
    border: 4px solid black;
    background-color: black;
    &:hover {
      background-color: blue;
    }
  }
  .tab { ... }
  .citation { ... }
}
//Now if we want to mixin the .button class in our #header a, we can do:
#header a {
  color: blue;
  #bundle.button();  // can also be written as #bundle > .button
}
//Note: append () to your namespace (e.g. #bundle()) if you don't want it to appear in your CSS output i.e. #bundle .tab.
#colors() {
  primary: red;
  secondary: black;
}

.button {
  color: #colors[primary];
  border: 4px solid #colors[secondary];
}
//This outputs, as expected:
.button {
  color: red;
  border: 4px solid black;
}
// Scope
@var: purple;

#page {
  @var: pink;
  #header {
    color: @var; // pink
  }
}
//Like CSS custom properties, mixin and variable definitions do not have to be placed before a line where they are referenced. So the following Less code is identical to the previous example:
@var: purple;

#page {
  #header {
    color: @var; // pink
  }
  @var: pink;
}
//Both block-style and inline comments may be used:
/* One heck of a block
 * style comment! */
@var: purple;

// Get in line!
@var: white;
//Importing
@import "library"; // library.less
@import "typo.css";
// 3/9/2026;
```
### So here is everything I have learned and tinkered with Right Now.The next blog we will see some images of my progress in my MVP see you.
[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
