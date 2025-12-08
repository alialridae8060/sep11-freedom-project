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
// 12/15/2025





