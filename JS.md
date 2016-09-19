# Javascript Style Guide

## Language Usage

- Always use semicolons
- Use ALL CAPS for constants 
~~~~~~JS
/* Wrong */
var easing_constant = 0.4;

/* Correct */
var EASING_CONSTANT = 0.4;
~~~~~~

- When looping over arrays, always use the iterative loops
- Only use `for...in` when going over keys, not arrays
~~~~~~JS
var arr = [x1, x2, x2];
var obj = {
  key1: val,
  key2: val2
}
/* Wrong */
for(val in arr) {
  console.log(val);
}

/* Correct iteration over arrays */
for(var i = 0; i <= arr.length; i++ ) {
  console.log(arr[i]);
}

/* Correct use of `for...in` */
for(key in obj) {
  console.log(obj.key);
}
~~~~~~

- When accessing object values, use the dot syntax
~~~~~~JS
var obj = {
  key1: val,
  key2: val2
}
/* Wrong */
var foo = obj[key1];

/* Correct */
var foo = obj.key1;
~~~~~~

- When creating arrays and objects, use the literal syntax
~~~~~~JS
/* Wrong */
var foo = new Array(val1, val2, val3);
var bar = new Object();

/* Correct */
var foo = [val1, val2, val3];
var bar = {
  key1: val,
  key2: val2
};
~~~~~~

## Naming and Style
- Use camelCase


## Code Formatting
- Use 2 spaces for indentation
- Remove trailing spaces
- Limit your line to 80 characters
- No spaces inside grouping symbols: [], (), {}
- No space before opening parenthesis in function declarations
- If object and array initializations are within 80 characters, keep them inline.
- If object and array initializations must span multiple lines, use 2 spaces to indent.
~~~~~~JS
// Sample code from Google
// Object initializer.
var inset = {
  top: 10,
  right: 20,
  bottom: 15,
  left: 12
};

// Array initializer.
var rows = [
  '"Slartibartfast" <fjordmaster@magrathea.com>',
  '"Zaphod Beeblebrox" <theprez@universe.gov>',
  '"Ford Prefect" <ford@theguide.com>',
  '"Arthur Dent" <has.no.tea@gmail.com>',
  '"Marvin the Paranoid Android" <marv@googlemail.com>',
  'the.mice@magrathea.com'
];

// Used in a method call.
goog.dom.createDom(goog.dom.TagName.DIV, {
  id: 'foo',
  className: 'some-css-class',
  style: 'display:none'
}, 'Hello, world!');
~~~~~~

## Functions
- When a function takes more than 3 arguments, put them in multiple lines and align
them with the parenthesis
~~~~~~JS
/* Wrong */
var foo = function(longArgument1, longArgument2, longArgument3, longArgument4, longArgument5, longArgument6) {
}
/* Correct */
var foo = function(longArgument1,
                   longArgument2,
                   longArgument3,
                   longArgument4,
                   longArgument5,
                   longArgument6) {
}
~~~~~~

- When method chaining, put the next function on the next line and put the dot at the beginning
~~~~~~JS
var foo = ready()
          .set()
          .go();
~~~~~~
