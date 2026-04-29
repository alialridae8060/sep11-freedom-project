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
// 3/9/2026:


