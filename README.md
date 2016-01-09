# Principles of Writing Consistent, Idiomatic HTML and CSS for MHDSTPA FAMCare

## All code in any code-base should look like a single person typed it, no matter how many people contributed.

### The following list outlines the practices that I use in all code that I am the original author of; contributions to projects that I have created should follow these guidelines.

### I do not intend to impose my style preferences on other people's code or projects; if an existing common style exists, it should be respected.


> ### "Arguments over style are pointless. There should be a style guide, and you should follow it"
>_Rebecca_ _Murphey_

&nbsp;

> ### "Part of being a good steward to a successful project is realizing that writing code for yourself is a Bad Idea™. If thousands of people are using your code, then write your code for maximum clarity, not your personal preference of how to get clever within the spec."
>_Idan_ _Gazit_


## Important, Non-Idiomatic Stuff:

### Code Quality Tools, Resources & References

 * [W3C HTML validator](http://validator.w3.org/nu/)
 * [Dirty Markup](http://www.dirtymarkup.com/)
 * [CSS Validation Service from W3C](https://jigsaw.w3.org/css-validator/)
 * [Sitepoint HTML](http://jsfiddle.net/)
 * [Can I Use](http://caniuse.com/)
 * [Tage List](http://www.w3schools.com/tags/)

## Get Smart

 * [Annotated ECMAScript 5.1](http://es5.github.com/)
 * [Sitepoint HTML page](http://www.sitepoint.com/html-css/html/)

### Test Facility

Forms must be thoroughly tested before going live. Develop tools and changes in the development mode and promote once the form is ready.

## Table of Contents

 * [Be Smart and Future Proof](#besmart)
 * [Document Type](#doctype)
 * [Element Names](#elenames)
 * [Closing Tags](#closetags)
 * [Use of Quotes](#doublequotes)
 * [Image Attributes](#images)
 * [Indents, Spaces and Equal Signs](#spaces)
 * [General Formatting](#formatting)
 * [Protocol](#protocol)
 * [Encoding](#encoding)
 * [Entity References](#entities)
 * [Type Attributes](#typeatts)
 * [CSS Validity](#validcss)
 * [ID and Class Names](#idnames)
 * [Type Selectors](#typesels)
 * [Shorthand Properties](#shorthand)
 * [0 and Units](#zeros)
 * [Hexadecimal Notation](#hex)
 * [Declaration Order](#decorder)
 * [CSS General Formatting](#cssgeneral)

------------------------------------------------

## Preface

The following sections outline a _reasonable_ style guide for modern JavaScript development and are not meant to be prescriptive. The most important take-away is the **law of code style consistency**. Whatever you choose as the style for your project should be considered law. Link to this document as a statement of your project's commitment to code style consistency, readability and maintainability.

## Idiomatic Style Manifesto

### 1. <a name="besmart">Be Smart and Future Proof</a>
  - In the future, programs like XML readers, may want to read your HTML.
  - Using a well-formed "close to XHTML" syntax, can be smart.
  - Always keep your style smart, tidy, clean and well-formed - these rules will help

### 2. <a name="doctype">Use Correct Document Type</a>
  - Always declare the document type as the first line in your document
  - For consistency with other elements, use lower case
  ```html
  <!doctype html>

  ```

### 3. <a name="elenames">Use Lower Case</a>

Whilst HTML5 allows mixing uppercase and lowercase letters in element names...

  - All element names are written in lowercase
  - All attributes, attribute values, CSS selectors, properties and property values are also written in lowercase

  ```html
  <!-- Bad  -->
  <DIV>
    <SPAN style="color:#E5E5E5">Example</span>
  </DIV>

  <!-- Good  -->
  <div>
    <span style="color:#e5e5e5">Example</span>
  </div>

  ```

### 4. <a name="closetages">Close All HTML Elements</a>

  HTML5 does not require elements to be close, but...

  - We will close all elements

  ```html
  <!-- Bad  -->
  <div>
    <p>Paragraph 1
    <p>Paragraph 2
  </div>

  <!-- Good  -->
  <div>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
  </div>

  ```

  - Exceptions: do not close empty elements...

  ```html
  <!-- Bad  -->
  <meta charset="utf-8" />
  <br />

  <!-- Good  -->
  <meta charset="utf-8">
  <br>
  ```

### 5. <a name="doublequotes">Use Double Quotes for attributes</a>

  - We will always use double quotes

  ```html
  <!-- Bad  -->
  <a class='primary'>Sign in</a>

  <!-- Good  -->
  <a class="primary">Sign in</a>
  ```

### 6. <a name="images">Image Attributes</a>

  - Always use the alt attribute (even if value is blank)
  - Always define image size (It reduces flickering because the browser can reserve space for images before they are loaded)

  ```html
  <!-- Bad  -->
  <img src="spreadsheet.png">
  <img src="spacer.png">

  <!-- Good  -->
  <img src="spreadsheet.png" alt="Delete icon">
  <img src="spacer.png" alt="">
  ```

### 7. <a name="spaces">Indents, Spaces and Equal Signs</a>

  - Always use 2 spaces as an indent
  - Do not tabs for indents
  - Do not place spaces between attribute names and values
  - Spaces are required when multiple values are listed
  - Always remove trailing white spaces

  ```html
  <!-- Bad  -->
  <link rel = "stylesheet" href = "styles.css">
  <div style="color:red;border:1px solid red;">
    <!-- html  -->
  </div>

  <!-- Good  -->
  <link rel="stylesheet" href="styles.css">
  <div style="color:red; border:1px solid red;">
    <!-- html  -->
  </div>
  ```

### 8. <a name="formatting">General Formatting Rules</a>

  - Do not add blank lines without a reason
  - Lines are no longer than 80 characters
  - Use a new line for every block, list, or table element, and indent every such child element
  - Lines are no longer than 80 characters
  - Use a new line for every block, list, or table element, and indent every such child element

  ```html
  <!-- Bad  -->
  <body>

    <h1>The Header</h1>

    <p>
    Tokyo is the capital of Japan, the center of the Greater Tokyo Area, and and the most populous metropolitan area in the world. It is the seat of the Japanese government and the Imperial Palace, and the home of the Japanese Imperial Family.
    </p>

  </body>

  <!-- Good  -->
  <body>
    <h1>The Header</h1>
    <p>
    Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and and the most populous metropolitan area in the world. It is the seat of
the Japanese government and the Imperial Palace, and the home of the Japanese
Imperial Family.
    </p>
  </body>

  ```

### 9. <a name="protocol">Protocol</a>

  - Omit the protocol from embedded resources

Omit the protocol portion (http:, https:) from URLs pointing to images and other media files, style sheets, and scripts unless the respective files are not available over both protocols. Omitting the protocol—which makes the URL relative—prevents mixed content issues and results in minor file size savings.

  ```html
  <!-- Bad  -->
  <script src="http://www.google.com/js/gweb/analytics/autotrack.js"></script>
  .example {
    background: url(http://www.google.com/images/example);
  }

  <!-- Good  -->
  <script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>
  .example {
    background: url(//www.google.com/images/example);
  }
  ```

### 10. <a name="encoding">Encoding</a>

  - Always use UTF-8 (make sure your editor uses UTF-8 as character encoding, without a byte order mark)

  ```html
  <!-- Good  -->
  <meta charset="utf-8">
  ```

### 11. <a name="entities">Entity References</a>

  - Use entity names (FAMCare does not recognize the symbols regardless of encoding)

  ```html
  <!-- Bad  -->
  The currency symbol for the Euro is €.

  <!-- Good  -->
  The currency symbol for the Euro is &euro; or &#8364;.
  ```

### 12. <a name="attributes">Type Attributes</a>

  - Omit type attributes for style sheets and scripts.

  ```html
  <!-- Bad  -->
  <link rel="stylesheet" href="//www.google.com/css/maia.css" type="text/css">
  <script src="//www.google.com/js/gweb/analytics/autotrack.js"
 type="text/javascript"></script>

  <!-- Good  -->
  <link rel="stylesheet" href="//www.google.com/css/maia.css">
  <script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>
  ```

### 13. <a name="validcss">CSS Validity</a>

  - Always use valid CSS where possible
  - Use tools such as the W3C [CSS validator](http://jigsaw.w3.org/css-validator/) to test

### 14. <a name="idnames">ID and Class Names</a>

  - Always use meaningful or generic ID and class names
  - Names that are specific and reflect the purpose of the element should be preferred as these are most understandable and the least likely to change
  - Generic names are simply a fallback for elements that have no particular or no meaning different from their siblings. They are typically needed as “helpers”
  - Using functional or generic names reduces the probability of unnecessary document or template changes
  - Using ID and class names this way contributes to acceptable levels of understandability and code efficiency
  - Use ID and class names that are as short as possible but as long as necessary

  ```html
  <!-- Bad  -->
  #yee-1901 {}
  <img src="spacer.png">
  .button-green {}
  .clear {}

  <!-- Good  -->
  /* specific  */
  #gallery {}
  #login {}
  .video {}
  /* generic  */
  .aux {}
  .alt {}  
  ```

### 15. <a name="typesels">Type Selectors</a>

  - Avoid qualifying ID and class names with type selectors (for performance reasons)

  ```html
  <!-- Bad  -->
  ul#example {}
  div.error {}

  <!-- Good  -->
  #example {}
  .error {}
  ```

### 16. <a name="shorthand">Shorthand</a>

  - Always use shorthand properties where possible

  ```html
  <!-- Bad  -->
  border-top-style: none;
  font-family: palatino, georgia, serif;
  font-size: 100%;
  line-height: 1.6;
  padding-bottom: 2em;
  padding-left: 1em;
  padding-right: 1em;
  padding-top: 0;

  <!-- Good  -->
  border-top: 0;
  font: 100%/1.6 palatino, georgia, serif;
  padding: 0 1em 2em;
  ```

### 17. <a name="zeros">0 and Units</a>

  - Omit unit specification after "0" values
  - Omit leading "0"s in values

  ```html
  <!-- Bad  -->
  margin: 0px;
  padding: 0px;
  font-size: 0.8em;

  <!-- Good  -->
  margin: 0;
  padding: 0;
  font-size: .8em;
  ```

### 18. <a name="hex">Hexadecimal Notation</a>

  - Use 3 character hexadecimal notation where possible

  ```html
  <!-- Bad  -->
  color: #eebbcc;

  <!-- Good  -->
  color: #ebc;
  ```

### 19. <a name="decorder">Declaration Order</a>

  - Put declarations in alphabetical order in order to achieve consistent code in a way that is easy to remember and maintain

  ```html
  <!-- Bad  -->
  color: black;
  background: fuchsia;
  border-radius: 4px;
  border: 1px solid;
  -moz-border-radius: 4px;
  -webkit-border-radius: 4px;
  text-align: center;
  text-indent: 2em;

  <!-- Good  -->
  background: fuchsia;
  border: 1px solid;
  -moz-border-radius: 4px;
  -webkit-border-radius: 4px;
  border-radius: 4px;
  color: black;
  text-align: center;
  text-indent: 2em;
  ```

### 20. <a name="cssgeneral">General Formatting</a>

  - Indent all block content, that is rules within rules as well as declarations, so to reflect hierarchy and improve understanding
  - End every declaration with a semicolon for consistency and extensibility reasons
  - Always use a single space between property and value (but no space between property and colon) for consistency reasons
  - Always use a single space between the last selector and the opening brace that begins the declaration block, and the opening brace should be on the same line as the last selector in a given rule
  - Always start a new line for each selector and declaration
  - Use single quotation marks for attribute selectors and property values
  - Separate rules by new lines

  ```html
  <!-- Bad  -->
  #video{
    margin-top: 1em;
  }
  #video
  {
    margin-top: 1em;
  }
  a:focus, a:active {
  position: relative; top: 1px;
  }
  html {
    font-family: "open sans", arial, sans-serif;
  }

  <!-- Good  -->
  #video {
    margin-top: 1em;
  }

  h1,
  h2,
  h3 {
    font-weight: normal;
    line-height: 1.2;
  }

  html {
    font-family: 'open sans', arial, sans-serif;
  }
  ```

## Appendix
----------
<a rel="license" href="http://creativecommons.org/licenses/by/3.0/deed.en_US"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by/3.0/80x15.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">FAMCare: Principles of Writing Consistent JavaScript</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/scouserantro/idiomatic.js" property="cc:attributionName" rel="cc:attributionURL">Antro</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/3.0/deed.en_US">Creative Commons Attribution 3.0 Unported License</a>.<br /><a rel="Style guide" href="https://google.github.io/styleguide/htmlcssguide.xml">Based Google Style Guide</a> and <a rel="Style Guide" href="http://www.w3schools.com/html/html5_syntax.asp">w3schools Style Guide</a>
