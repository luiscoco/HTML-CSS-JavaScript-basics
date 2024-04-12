# Introduction to HTML, CSS and JavaScript

HTML basics: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics

CSS basics: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics

JavaScript basics: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics

Other samples in this repo: https://github.com/orgs/mdn/repositories

## 1. Prerequisite

Install **VSCode** and also install the **Live Server** extension

## 2. My first Web Page sample

### 2.1. Project folders and files structure

![image](https://github.com/luiscoco/HTML-and-CSS-basics/assets/32194879/98186d1e-09ed-48d3-aaa0-8c51dab8ebac)

### 2.2. HTML source code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet" type="text/css">
    <link href="styles/style.css" rel="stylesheet" type="text/css">
  </head>
  <body>
    <h1>Mozilla is cool</h1>
    <img src="images/firefox-icon.png" alt="The Firefox logo: a flaming fox surrounding the Earth.">

    <p>At Mozilla, we’re a global community of</p>

    <ul> <!-- changed to list in the tutorial -->
      <li>technologists</li>
      <li>thinkers</li>
      <li>builders</li>
    </ul>

    <p>working together to keep the Internet alive and accessible, so people worldwide can be informed contributors and creators of the Web. We believe this act of human collaboration across an open platform is essential to individual growth and our collective future.</p>

    <p>Read the <a href="https://www.mozilla.org/en-US/about/manifesto/">Mozilla Manifesto</a> to learn even more about the values and principles that guide the pursuit of our mission.</p>
  <button>Change user</button>
  <script src="scripts/main.js"></script>
  </body>
</html>
```

#### 2.2.1. Version and Type of HTML the page

```html
<!DOCTYPE html>
```

The ```<!DOCTYPE html>``` declaration in HTML is used to **instruct the web browser about the version and type of HTML the page** is written in

This declaration is not an HTML tag; rather, it is an **instruction** to the web browser

Here’s a breakdown of its purpose and function:

**Indicates HTML version**: The ```<!DOCTYPE html>``` declaration is used to tell the browser to render the page using the standards of **HTML5**

HTML5 is the latest standard as of my last update and includes many features that facilitate modern web design and application development

**Ensures proper rendering**: By including this declaration, you help ensure that the browser renders the page in standards mode

**Standards mode** is a rendering mode that is more consistent with how the HTML standards are defined

Without this declaration, the browser might render the page in "quirks mode," which is a backwards-compatible rendering mode that mimics the behavior of older browsers and may lead to inconsistent layout and functionality across different browsers

**Syntax and Placement**: The ```<!DOCTYPE html>``` declaration should be the very first line in an HTML document, before the <html> tag. It does not require a closing tag.

**Simplicity**: For **HTML5**, the declaration is simple (```<!DOCTYPE html>```), which is a significant simplification from previous HTML versions that used longer, more complex strings to specify the DOCTYPE.

Including the ```<!DOCTYPE html>``` is considered a best practice for HTML documents and is crucial for **cross-browser compatibility** and for ensuring that the HTML code is interpreted in the way it was intended.

#### 2.2.2. HTML web page root element

```html
<html lang="en">
```

The ```<html>``` **tag** is a fundamental part of any HTML document, serving as the **root element** that encapsulates all the content of the webpage

The lang="en" **attribute** within the ```<html>``` tag provides additional important information about the **language of the document's content**

Here’s what each part signifies:

```<html>``` **Tag**: This tag marks the beginning of an HTML document. It contains all the visible and hidden content of the web page, including elements like <head> and <body>. The <html> tag is closed with </html> at the end of the document.

**lang="en" Attribute**

**Purpose**: The lang attribute specifies the primary language of the document’s content. This can be crucial for accessibility, search engine optimization (SEO), and for browsers that perform language-specific processing

**Value “en”**: The value "en" indicates that the primary language used in the document is **English**

This helps assistive technologies like **screen readers to pronounce content** with correct accentuation and intonation

It also helps search engines to offer language-specific search results

**Global Attribute**: The lang attribute can be used on any HTML element, not just the ```<html>``` tag, to indicate changes in the language for specific portions of a page

Here’s how the ```<html lang="en">``` tag fits into a typical HTML document:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Example Page</title>
</head>
<body>
    <p>This is an example of a simple HTML document.</p>
</body>
</html>
```

In this structure, the ```<html lang="en">``` tag effectively communicates that the content of this webpage is primarily in English, aiding both user accessibility and web functionality

#### 2.2.3. HTML character encoding

```html
<meta charset="utf-8">
```

The ```<meta charset="utf-8">``` tag in HTML is used to specify the character encoding for the HTML document. Here's a breakdown of its components and purpose:

```<meta>``` Tag: This tag provides metadata about the HTML document. Metadata is data (information) about data. The <meta> tag does not affect the display but provides essential information to the browser and search engines. The tag is placed within the <head> section of the HTML document.

**charset="utf-8" Attribute**:

**Purpose**: The charset attribute specifies the character encoding used in the document

Character encoding is a method used to represent a repertoire of characters by some kind of encoding system that assigns a number to each character for digital representation

**Value "utf-8"**: UTF-8 (Unicode Transformation Format - 8-bit) is a widely used encoding system that can represent every character in the Unicode character set

It is designed to be backward compatible with ASCII and to avoid the complications of byte order (big-endian and little-endian) in Unicode transformations

**Importance**: Using UTF-8 ensures that all characters in the document, including special characters from various languages and unique symbols, are correctly interpreted and displayed by the browser

It is **especially important for websites that use multiple languages or special characters**.

**Placement and Usage**:

The ```<meta charset="utf-8">``` is typically placed as early as possible within the <head> section of an HTML document

**This positioning ensures that the browser knows the character encoding right from the start**, which is crucial for correctly parsing and displaying the content

Here is an example showing how this tag might appear within the HTML document:

```html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Sample Page</title>
</head>
<body>
    <p>Hello, world! Here are some special characters: é, ö, 中, عربى, 🚀</p>
</body>
</html>
```

In this example, the ```<meta charset="utf-8">``` ensures that all characters, including international characters and emojis, are correctly displayed by the browser

It's an essential part of modern HTML documents to accommodate global and multilingual content.

#### 2.2.4. 

```html
<link href="styles/style.css" rel="stylesheet" type="text/css">
```


### 2.3. CSS source code

```css
html {
    font-size: 10px;
    font-family: 'Open Sans', sans-serif;
  }
  
  
  h1 {
    font-size: 60px;
    text-align: center;
  }
  
  p, li {
    font-size: 16px;
    line-height: 2;
    letter-spacing: 1px;
  }
  
  
  html {
    background-color: #00539F;
  }
  
  body {
    width: 600px;
    margin: 0 auto;
    background-color: #FF9500;
    padding: 0 20px 20px 20px;
    border: 5px solid black;
  }
  
  h1 {
    margin: 0;
    padding: 20px 0;
    color: #00539F;
    text-shadow: 3px 3px 1px black;
  }
  
  img {
    display: block;
    margin: 0 auto;
  }
```

### 2.4. JavaScript source code

```javascript
// Image switcher code

let myImage = document.querySelector('img');

myImage.onclick = function() {
  let mySrc = myImage.getAttribute('src');
  if(mySrc === 'images/firefox-icon.png') {
    myImage.setAttribute ('src','images/firefox2.png');
  } else {
    myImage.setAttribute ('src','images/firefox-icon.png');
  }
}

// Personalized welcome message code

let myButton = document.querySelector('button');
let myHeading = document.querySelector('h1');

function setUserName() {
  let myName = prompt('Please enter your name.');
  if(!myName) {
    setUserName();
  } else {
    localStorage.setItem('name', myName);
    myHeading.innerHTML = 'Mozilla is cool, ' + myName;
  }
}

if(!localStorage.getItem('name')) {
  setUserName();
} else {
  let storedName = localStorage.getItem('name');
  myHeading.innerHTML = 'Mozilla is cool, ' + storedName;
}

myButton.onclick = function() {
  setUserName();
}
```

## 3. How to run the application


## 4. How to debug the application





**HTML elements**

**Tag**

**Attributes**: 

These are two attributes(**type** and **disabled**) sample for the HTML element **input**: 

```html
<input type="text" disabled />
```

Methods

Other features:

To use quote marks inside other quote marks of the same type (single quote or double quote), use HTML entities. 

```html
<a href="https://www.example.com" title="An &quot;interesting&quot; reference">A link to my example.</a>
```

