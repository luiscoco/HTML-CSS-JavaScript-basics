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
  <button id="myFirstButton">Change user</button>
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

#### 2.2.4. How to link a CSS stylesheet to the HTML page

```html
<link href="styles/style.css" rel="stylesheet" type="text/css">
```

The HTML ```<link>``` tag in your code is used to link external resources to an HTML document. In this specific instance, it's linking a CSS stylesheet to the HTML page. Here’s a brief explanation of the components of the tag:

```<link>``` Tag: This is used to define a relationship between the HTML document and an external resource. It is a self-closing tag and is placed inside the <head> section of the HTML document.

**Attributes**:

**href="styles/style.css"**: This attribute specifies the path to the external file that is being linked to the HTML document

In this case, it's a CSS file named style.css located in a folder named styles

**rel="stylesheet"**: The rel (relationship) attribute specifies the relationship between the current document and the linked file

Here, stylesheet indicates that the linked file is a stylesheet. This tells the browser how to use the linked file

**type="text/css"**: This attribute specifies the MIME type of the linked file, telling the browser what kind of file it is. text/css indicates that the file is a CSS (Cascading Style Sheets) file

Although this attribute is optional in HTML5 (as browsers can infer the type from the rel attribute), it can still be included for clarity or compatibility with older HTML specifications

Here is how this tag typically fits into an HTML document:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Example Page</title>
    <link href="styles/style.css" rel="stylesheet" type="text/css">
</head>
<body>
    <p>This is an example of a web page using an external CSS file to style its content.</p>
</body>
</html>
```

In this setup, **the CSS file linked in the <link> tag would contain the styles (like colors, fonts, layouts) that apply to elements in the HTML document**, helping to separate content from presentation.

#### 2.2.5. How to link an external CSS stylesheet from Google Fonts to the HTML document

The HTML ```<link>``` tag in your code is used to link an external CSS stylesheet from Google Fonts to the HTML document. This specific tag includes the Open Sans font family in your webpage. Here’s a brief breakdown of each component of the tag:

```<link>``` Tag: This is utilized to establish a relationship between the HTML document and an external resource, which, in this case, is a CSS stylesheet that includes the font styles from Google Fonts. This tag is usually placed inside the <head> section of an HTML document.

**Attributes**:

**href="https://fonts.googleapis.com/css?family=Open+Sans"**: This attribute specifies the URL where the stylesheet is located

The URL points to Google's font service, which provides the Open Sans font. The query parameter family=Open+Sans in the URL specifies that the stylesheet should include the Open Sans font.

**rel="stylesheet"**: The rel attribute indicates the relationship between the document and the linked resource. Here, setting rel to "stylesheet" tells the browser that the linked resource is a CSS stylesheet to be used for styling the webpage.

**type="text/css"**: This attribute describes the MIME type of the linked resource, here indicating that it is a CSS file. While often optional in modern web development due to browsers' ability to infer type from context, it provides explicit information about the content type of the linked resource.

Here’s how the ```<link>``` tag fits into an HTML document:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Example Page</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet" type="text/css">
</head>
<body>
    <p style="font-family: 'Open Sans', sans-serif;">This text uses the Open Sans font loaded from Google Fonts.</p>
</body>
</html>
```

In this example, the font Open Sans is applied to a paragraph element in the body of the document. The linked CSS file provided by Google Fonts ensures that the Open Sans font is available and rendered in the browser, enhancing typography across the webpage.

#### 2.2.6. HTML elements included in the body

The HTML code provided contains several fundamental **HTML elements** that structure the content of a **web page**. Here's a breakdown of each element:

```<h1>```: The ```<h1>``` tag is used for the main heading of the page. It has the highest level of importance among heading tags (```<h1>``` through ```<h6>```) and helps in structuring the content and improving SEO by emphasizing key topics. In your example, ```<h1>Mozilla is cool</h1>``` sets the main topic of the content.

```<img>```: The ```<img>``` tag is used to embed an image in the HTML page. It has several attributes:

**src="images/firefox-icon.png"** specifies the path to the image file.

**alt="The Firefox logo"**: a flaming fox surrounding the Earth." provides alternative text that describes the image, which is useful for accessibility (screen readers) and when the image cannot be displayed.

```<p>```: The ```<p>``` tag defines a paragraph. It's used to organize the text into blocks, making the content easier to read. You have several paragraphs in your example, each describing different aspects of Mozilla's mission and work.

```<ul>``` and ```<li>```:

```<ul>``` stands for "unordered list," which is used to group a list of items with no particular order. It is often rendered with bullet points.

```<li>``` stands for "list item" and is used inside ```<ul>``` (or ```<ol>``` for ordered lists) to represent individual items in the list. In your example, the list details various roles people have in the Mozilla community.

```<a>```: The ```<a>``` tag defines a hyperlink, which is used to link from one page to another. This tag makes the web interconnected. In your example:

**href="https://www.mozilla.org/en-US/about/manifesto/"** specifies the URL of the page the link goes to.

The clickable text "Mozilla Manifesto" leads users to more detailed information about Mozilla's values and principles.

```<button>```: The ```<button>``` tag is used to create a clickable button. Buttons are typically used to submit data to a server or trigger interactive JavaScript actions. In your code:

**id="myFirstButton"** is an **attribute** that provides a **unique identifier for the button**, which can be referenced in JavaScript or CSS.

Each of these elements plays a specific role in structuring the webpage, enhancing its functionality, accessibility, and user interaction.

#### 2.2.7. How to include a JavaScript file into the webpage

The ```<script src="scripts/main.js"></script>``` tag in your HTML code is used to **include a JavaScript file into the webpage**

This tag is crucial for **adding interactivity and dynamic behavior to web pages**. Here's a brief explanation of its components and purpose:

```<script>``` Tag: This tag is used to embed a JavaScript script within an HTML document. It can either contain inline scripting or link to an external script file, which is what is done in your example.

**Attributes**:

**src="scripts/main.js"**: The src (source) attribute specifies the path to the JavaScript file that is to be included. This path can be a relative URL (as in your example, pointing to a file within the same site) or an absolute URL (linking to a file hosted on a different domain). The file **main.js** in your example likely contains JavaScript code that handles functionalities such as DOM manipulations, event handling, or data fetching.

**Placement in the Document**: The ```<script>``` tag is **placed near the end of** the ```<body>``` section. This is a common practice **to ensure that the HTML content above it is loaded before the script is executed**

Placing scripts at the **bottom** can help improve page load times as the browser doesn't need to pause the parsing of HTML to load and execute the script unless specifically needed earlier.

**Execution**: When the browser reaches the ```<script>``` tag during the rendering of the page, it fetches the script file specified in the src attribute and executes it. This script can manipulate the webpage's content dynamically, respond to user interactions, or perform many other functions.

**Example Usage**:

In your HTML structure, the **JavaScript file main.js** might contain code that interacts with the DOM, such as attaching an event listener to the button with the ID myFirstButton

When clicked, this button could trigger JavaScript functions defined within main.js, possibly changing the user interface or fetching and displaying data

By including the ```<script src="scripts/main.js"></script>``` tag in your webpage, you effectively integrate JavaScript, enhancing the webpage's interactivity and functionality

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

let myButton = document.querySelector('#myFirstButton');
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

