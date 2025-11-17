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



