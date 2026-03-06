# Tool Learning Log

## Tool:Less.js

## Project:Buisness Decision Game.

---

### 10/27/2025:
### So I've decided to use Less.js due to its simplicity and the fact it involves CSS which I find easier than phaser.js.
### 11/10/2025
### So I already used two forms of code in tinkering.md which are practice code structures from https://lesscss.org/ but I'm not sure if the results are good or bad since I've just started tinkering with them the first one is functions and let me sight wording from the website:"Less provides a variety of functions which transform colors, manipulate strings and do maths. They are documented fully in the function reference.Using them is pretty straightforward.".The next up is Namespaces and Accessors and heres the description from the website:"Sometimes, you may want to group your mixins, for organizational purposes, or just to offer some encapsulation. You can do this pretty intuitively in Less.".This is what I have so far.
### 11/17/2025
### So I decided to lock in and began learning about Less.js.So Less.js is also knwon as Leaner Style Sheets which is a backwards-compatible language extension for CSS. This is the official documentation for Less, the language and Less.js, the JavaScript tool that converts your Less styles to CSS styles.The Variables of Less.js are pretty self explanatory as they are like the code for CSS.Next up is Mixins which are a way of including ("mixing in") a bunch of properties from one rule-set into another rule-set.Next up is Nesting where less gives you the ability to use nesting instead of, or combine with CSS.You can also bundle pseudo-selectors with your mixins using this method.
### 12/8/2025
### So now is the time to resume the learning log.So after learning about Nesting now it is time to learn about the rules and bubbling of nesting.So nesting has rules @media and/or @supports that can be nested in the same way as selectors.Arithmetical operations +, -, *, / can operate on any number, color or variable. If it is possible, mathematical operations take units into account and convert numbers before adding, subtracting or comparing them. The result has leftmost explicitly stated unit type. If the conversion is impossible or not meaningful, units are ignored.Multiplication and division do not convert numbers. It would not be meaningful in most cases - a length multiplied by a length gives an area and css does not support specifying areas.However, you may find Less's Color Functions more useful.You can change Math setting, if you want to make it always work, but not recommended.For CSS compatibility, calc() does not evaluate math expressions, but will evaluate variables and math in nested functions.
### 12/15/2025
### ### 3/2/2026:
### After a long periods of breaks and also procrastination time to resume learning.Right now there is Escaping which allows you to use any arbitrary string as property or variable value. Anything inside ~"anything" or ~'anything' is used as is with no changes except interpolation.Less provides a variety of functions which transform colors, manipulate strings and do maths. They are documented fully in the function reference.Next up is functions where less.js provides a variety of functions which transform colors, manipulate strings and do maths.They are documented fully in the function reference.Using them is pretty straightforward.After functions we have namespaces and accessors.In namespaces and accessors sometimes, you may want to group your mixins, for organizational purposes, or just to offer some encapsulation. You can do this pretty intuitively in Less.Following namespaces and accessors we have maps you can use mixins and rulesets as maps of values.Now we have scope(nope not the phsyical scope a piece of code called scope) where scope in Less is very similar to that of CSS. Variables and mixins are first looked for locally, and if they aren't found, it's inherited from the "parent" scope.Second to last we have comments which are block style and inline.Finally there is importing where Importing works pretty much as expected. You can import a .less file, and all the variables in it will be available. The extension is optionally specified for .less files.
### 3/9/2026:







