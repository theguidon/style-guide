# HTML/CSS Style Guide
*Note: These loosely follow the style guide created by [Google](https://google.github.io/styleguide/htmlcssguide.xml)*

## HTML Style Guide

- Use lowercase only
~~~~~~html
<!-- Wrong -->
<A HREF="THEGUIDON.COM">The GUIDON</A>

<!-- Correct -->
<a href="theguidon.com">The GUIDON</a>
~~~~~~

- No trailing whitespace
- Use 2 spaces to indent
- Attributes should be enclosed in double quotations ""

## CSS Style Guide

## CSS Naming

- Name classes and IDs based on their purpose in the page
~~~~~~~CSS
/* Wrong */
.box-129 {}

/* Correct */
.navbar {}
.menu {}
~~~~~~~

- Classes added as fallback should still have a descriptive name
~~~~~~CSS
.inquiry-red-text { color: <>; }
.inquiry-red-bg { background-color: <>; }
~~~~~~

- Use dashes to separate names
~~~~~~CSS
/* Wrong */
.sectionBox {}
.section_box {}

/* Correct */
.section-box {}
~~~~~~

## CSS Values

- Use shorthand whenever possible
~~~~~~CSS
/* Wrong */
.box {
  padding-top: 50px;
  padding-bottom: 50px;
  padding-left: 20px;
  padding-right: 20px;
}

/* Correct */
.box {
  padding: 50px 20px; /* Top/Bottom Left/Right */
  padding: 50px 20px 0; /* Top Left/Right Bottom */
}
~~~~~~

- Do not put the units in values of 0
~~~~~~CSS
/* Wrong */
.box { padding: 0px; }

/* Correct */
.box { padding: 0; }
~~~~~~

## Code Organization

- Group related declarations and separate using line breaks
~~~~~~CSS
.box {
  margin: 0;
  padding: 0;

  display: flex;
  flex-direction: column;
  align-items: center;

  font-family: 'Tiempos Regular', serif;
  font-size: 1.2em;
  line-height: 1.4em;

  transform: translateX(10px);
  transition: top 1s ease-in;
}
~~~~~~

- If there is only one line of declaration for a class, put it in one line
~~~~~~CSS
/* Wrong */
.box {
  padding: 0;
}

/* Correct */
.box { padding: 0; }
~~~~~~

- Always leave a space between the selector and the opening bracket
~~~~~~CSS
/* Wrong */
.box{}

/* Correct */
.box {}
~~~~~~
