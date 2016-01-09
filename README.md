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

### [Annotated ECMAScript 5.1](http://es5.github.com/)
### [Sitepoint HTML page](http://www.sitepoint.com/html-css/html/)

### Test Facility

Forms must be thoroughly tested before going live. Develop tools and changes in the development mode and promote once the form is ready.

## Table of Contents

 * [Be Smart and Future Proof](#besmart)
 * [Document Type](#doctype)
 * [](#elenames)
 * [](#cloasetags)
 * [Use of Quotes](#doublequotes)
 * [Image Attributes](#images)
 * [Indents, Spaces and Equal Signs](#spaces)
 * [General Formatting](#formatting)
 * [Protocol](#protocol)
 * [Encoding](#encoding)
 * [Entity References](#entities)
 * [Type Attributes](#)
 * [CSS Validity](#)
 * [ID and Class Names](#)
 * [Type Selectors](#)
 * [Shorthand Properties](#)
 * [0 and Units](#)
 * [ID and Class Name Delimiters](#)
 * [](#)
 * [](#)
------------------------------------------------


## Preface

The following sections outline a _reasonable_ style guide for modern JavaScript development and are not meant to be prescriptive. The most important take-away is the **law of code style consistency**. Whatever you choose as the style for your project should be considered law. Link to this document as a statement of your project's commitment to code style consistency, readability and maintainability.

## Idiomatic Style Manifesto

1. <a name="besmart">Whitespace</a>
  - In the future, programs like XML readers, may want to read your HTML.
  - Using a well-formed "close to XHTML" syntax, can be smart.
  - Always keep your style smart, tidy, clean and well-formed - these rules will help

2. <a name="doctype">Use Correct Document Type</a>
  - Always declare the document type as the first line in your document
  - For consistency with other elements, use lower case
  ```html
  <!doctype html>

  ```

3. <a name="elenames">Use Lower Case</a>

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

4. <a name="closetages">Close All HTML Elements</a>

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

5. <a name="doublequotes">Use Double Quotes for attributes</a>

    - We will always use double quotes

    ```html
    <!-- Bad  -->
    <a class='primary'>Sign in</a>

    <!-- Good  -->
    <a class="primary">Sign in</a>

    ```

5. <a name="images">Image Attributes</a>

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

6. <a name="spaces">Indents, Spaces and Equal Signs</a>

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
7. <a name="formatting">General Formatting Rules</a>

    - Do not add blank lines without a reason
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

## Appendix
----------
<a rel="license" href="http://creativecommons.org/licenses/by/3.0/deed.en_US"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by/3.0/80x15.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">FAMCare: Principles of Writing Consistent JavaScript</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/scouserantro/idiomatic.js" property="cc:attributionName" rel="cc:attributionURL">Antro</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/3.0/deed.en_US">Creative Commons Attribution 3.0 Unported License</a>.<br />Based on work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/rwldrn/idiomatic.js" rel="dct:source">github.com/rwldrn/idiomatic.js</a> - Thanks to Rick Waldon and the other contributors.
