# Web Technologies — Revision Notes

**Category:** Essentials · **Focus Area:** JavaScript Development · **Level:** Beginner

---

## Table of Contents

1. [HTML](#1-html)
2. [Debug](#2-debug)
3. [JavaScript](#3-javascript)
4. [JavaScript Debugging](#4-javascript-debugging)
5. [jQuery](#5-jquery)
6. [jQuery Debugging](#6-jquery-debugging)
7. [Web Design — Best Practices](#7-web-design--best-practices)

---

## 1. HTML

### 1.1 Web Technology — Definition and Terminologies

**Web technology** refers to the way computers/devices communicate with each other using markup languages. It establishes communication between different types of devices across the internet, and helps create, deliver, and manage web content using **HTML (HyperText Markup Language)**.

| Term | Definition |
|---|---|
| **Internet** | A large network of networks connecting thousands of computers that can communicate with one another |
| **World Wide Web** | A system of "interlinked hypertext documents" that can be accessed by users via the internet |
| **Web Browser** | An application software on your device used to access the web |
| **Web Server** | Where websites are hosted — receives the request for information, processes it, and sends the response back |

**Additional terminologies:**

- **Web Page** — an HTML document displayed as a single page in a browser; it can be connected to other pages
- **Website** — a collection of several web pages connected together; may contain text, images, audio, and video, usually present at the same internet address. The first page of a website is called the **home page**
- **Web Application** — a piece of software accessed by the browser. It ensures authentication before access and requires a sophisticated server to manage user requests (e.g., Google Apps, Amazon, YouTube)

### 1.2 Web Development

Web development refers to the building, creating, and maintaining of websites. It includes web design, web publishing, web programming, and database management.

- **Frontend web development** — building the "client side" of the application; the part of the website the user directly interacts with.
  - Frontend stack: **HTML, CSS, JavaScript** → further extended by **ES6, TypeScript, JS Frameworks, JS Libraries**
- **Backend web development** — refers to the server side of the website. Languages used: Java, PHP, Python, Node.js, etc.

### 1.3 Static Web Page

- A static web page/website is the basic type of website whose content is static
- Usually written in plain HTML
- Pre-built content is the same every time the page is loaded — it sends exactly the same response for every request
- Content only changes when someone publishes/updates the file and sends it to the web server
- **Flexibility** is the main advantage of a static website

```
Client → HTTP Request → Server → (Static HTML files) → HTTP Response → Client
```

### 1.4 Dynamic Web Page

- **Client-side scripting** generates content at the client, based on user input. The browser receives the page from the server and processes the code within the page to render information.
- In **server-side scripting**, software runs on the server, processes the code, and once completed, sends the page to the client.
- A dynamic website uses client-side scripting, server-side scripting, or both, to generate dynamic content.
- A dynamic web page shows different information at different points in time, and may generate different HTML for each request.
- It accesses content from a database or Content Management System (CMS) — updating the database updates the website content.

```
Client → HTTP Request → Server → Script/Method → HTTP Response → Client
```

### 1.5 Introduction to HTML

- **Hyper Text** — refers to the way web pages are linked to each other
- **Markup** — usage of tags to structure the web page
- HTML is used for developing web pages for applications. Web pages are text files containing HTML.
- **HTML Editor** — essentially a word processor for writing HTML

**HTML Structure:**

- HTML is comprised of **Elements**
- The structure begins with `<html>` and ends with `</html>`
- Elements (tags) are nested one inside another
- HTML describes structure using two main sections: `<head>` and `<body>`

### 1.6 Basic HTML Tags

| Tag | Purpose |
|---|---|
| `<html>` | Root element of the page |
| `<head>` | Contains meta information |
| `<title>` | Sets the page title |
| `<body>` | Contains the visible page content |
| `<h1>`–`<h6>` | Headings |
| `<p>` | Paragraph |
| `<br>` | Line break |
| `<hr>` | Horizontal rule |
| `<!-- -->` | Comments |

- **Paragraph tag:** The `<p>` tag defines a paragraph. Browsers automatically add space before and after each `<p>` element.
- `<!DOCTYPE>` — gives instructions to the web browser about the version of HTML used.

**HTML5** is essentially:
- A bit of HTML
- A whole sprinkling of JavaScript
- A dash of CSS

### 1.7 Links

- `<a>` — anchor tag (the hyperlink can be text or an image, which is clickable)
- `href` — defines the destination location
- `target` — defines where the targeted page must be opened

### 1.8 Semantic Tags

A **semantic element** clearly describes its meaning to both the browser and the developer.

- **Semantic elements:** `<form>`, `<table>`, `<article>`
- **Non-semantic elements:** `<div>`, `<span>`
- The `<div>` tag defines a division or section in an HTML document.

**New Semantic Elements:**

| Tag | Purpose |
|---|---|
| `<header>` | Specifies a header for a document or section |
| `<article>` | Represents a self-contained composition in a document, page, etc. |
| `<nav>` | Groups links together to pages or to parts of the current page |
| `<aside>` | Defines a section that is tangentially related to the content around it |
| `<footer>` | Refers to the footer of a web page |

### 1.9 HTML Forms

To build a form, the following HTML elements are commonly used: `<form>`, `<label>`, `<input>`, `<textarea>`

**Form Attributes:**

| Attribute | Purpose |
|---|---|
| `action` | Specifies the destination on submission |
| `method` | Specifies the HTTP method used to send the form — **GET** (data sent along the URL) or **POST** (data sent via the message body) |
| `autocomplete` | Specifies whether a form should have autocomplete on or off |
| `novalidate` | Specifies that the form should not be validated when submitted |

**Form — Input Elements:**

`<input>`, `<textarea>`, `<button>`, `<select>`, `<option>`, `<optgroup>`, `<fieldset>`, `<label>`

---

## 2. Debug

> Placeholder — the source notepad did not include dedicated HTML debugging content. Add browser DevTools techniques, HTML validation tools, or common markup error patterns here once available.

---

## 3. JavaScript

Most JavaScript usage spans both **client side** and **server side**:

- **Client side** — executed by the browser (via HTML)
- **Server side** — executed by **Node.js**

**JavaScript is used to:**
- Handle user events
- Implement business logic
- Handle dynamic content

### 3.1 Introduction to Scripting Language

- A computer language with a series of commands within a file
- Capable of being executed without being compiled
- Scripts provide changes to the webpage

**Two types of scripting:**
- Server-side scripting
- Client-side scripting

**Server-side scripting flow:** `Client → Internet → Server`

**Client-side scripting flow:** `Client ⇔ Server`

1. User requests a page
2. Runtime engine finds the source page in the web file
3. Runtime engine produces the HTML page, running all server code while creating the page
4. Runtime engine sends the page to the client
5. Client interprets and displays the HTML page, executing client-side JavaScript statements

### 3.2 JavaScript Introduction

JavaScript can be used on the client and server side:

- **Client side** — processing user input, validations
- **Latest implementation** — client-side / Single Page Applications
- **Server side (Node.js)**
  - Can create standalone applications, network applications, web applications
  - REST services, service layers
- **From traditional validation modules to:**
  - JavaScript libraries — jQuery, DOJO, React, and so on
  - JavaScript frameworks — Angular, Ember, and so on

### 3.3 Embedding JavaScript in HTML

3 methods to embed JavaScript into HTML code:

1. **Inline Script**
2. **Internal Script**
3. **External Script** (separate `.js` file):
   ```html
   <script src="myJavaScriptFile.js"></script>
   ```

### 3.4 JavaScript Data Types

**Primitive types:**

| Type | Example |
|---|---|
| String | `var name = "John";` |
| Number | `var age = 16;` |
| Boolean | `var isStudent = true;` |
| Undefined | `var city; // undefined` |
| Null | `var car = null;` |

**Reference types:**

| Type | Example |
|---|---|
| Array | `var ids = [101, 102, 103];` |
| Object | `var x = {id: 101, name: "John", salary: 40000};` |
| Function | `function greet() { console.log("Hello!"); }` |
| Date | `var today = new Date();` |
| Regex | `var pattern = /[A-Z]+/;` |

### 3.5 JavaScript Variables

- **Declaration** — registers a variable in the corresponding scope
- **Initialization** — allocates memory for the variable
- **Assignment** — assigns a specified value to the variable

**Scope of Variables:**

- **Global Variables** — `var` keyword is not mandatory
- **Local Variables** — `var` keyword is mandatory

### 3.6 Operators

**Arithmetic Operators:** `+`, `-`, `*`, `/`, `%`, `++`, `--`

**Assignment Operators:** `=`, `+=`, `-=`, `*=`, `/=`, `%=`

**Relational and Logical Operators:**

| Expression | Result | Meaning |
|---|---|---|
| `x == 8` | false | equal to (value) |
| `x == 5` | true | equal to (value) |
| `x === "5"` | true | *(as noted in source material)* |
| `x === 5` | false | equal value and equal type |
| `x === "5"` | true | equal value and equal type |
| `x != 8` | true | not equal |
| `x !== "5"` | false | not equal value or not equal type |
| `x > 8` | false | greater than |
| `x < 8` | true | less than |
| `x >= 8` | false | greater than or equal to |
| `x <= 8` | true | less than or equal to |
| `x < 10 && y > 1` | true | AND |

**Conditional Operator:**
`?:` (ternary) — If condition is true → value X, otherwise → value Y

### 3.7 Comments in JavaScript

- Single line: `// commented statement`
- Multiple line: `/* commented statement(s) */`

### 3.8 Programming Constructs in JavaScript

```
Control Structures
│
├── Decision Making
│   ├── if
│   ├── if-else
│   └── switch
│
└── Looping
    ├── do-while
    ├── for
    └── while
```

### 3.9 Event Handling

- **Event** — an action that is fired (initiated) within a webpage
- Useful for creating interactive websites
- JavaScript uses **asynchronous callbacks**

### 3.10 JavaScript Validation

- **JavaScript (client-side) data validation** happens **before** the form is submitted
- **Server-side application validation** happens **after** the form is submitted to the application server
- **Form Validation** consists of: Basic Validation & Data Format Validation

### 3.11 Strings and RegExp

- **String** — an array of characters. Example: `var name = "Teknoturf";`
- **RegExp Object** — a regular expression is an object that describes a pattern of characters

### 3.12 JavaScript Document Object Model (DOM)

- Every web page displayed inside a browser window can be considered an object
- JavaScript arranges objects in a **Document Object Model (DOM)**

### 3.13 Window Object

The **Window object** is the top-level object in the DOM.

**Window Object Properties:**

| Property | Description |
|---|---|
| `window.innerHeight` | Represents the inner height of the browser window |
| `window.innerWidth` | Represents the inner width of the browser window |

> Note: works across IE, Chrome, Firefox, Opera, and Safari

**Window Object Methods:**

| Method | Description |
|---|---|
| `window.open()` | Opens a new window |
| `window.close()` | Closes the current window |
| `window.moveTo()` | Moves the current window |
| `window.resizeTo()` | Resizes the current window |

### 3.14 Cookies

On the client machine, a text file called a **cookie** holds information about the user. Along with the request, the cookie information is passed to the server, so the server can easily understand it is from the same client.

---

## 4. JavaScript Debugging

> Placeholder — the source notepad did not include dedicated JavaScript debugging content. Add browser console/DevTools techniques, breakpoints, `console.log` strategies, or common runtime error patterns here once available.

---

## 5. jQuery

### 5.1 Introduction to jQuery

- jQuery makes JavaScript DOM work much easier
- **jQuery** is a JavaScript Library created by **John Resig** in **2006**
- jQuery is a fast, small, and feature-rich JavaScript library

### 5.2 Using jQuery Libraries

jQuery can be used in two ways:

**1. Local Installation** — downloaded directly to the local machine, then referenced via the script tag:
```html
<script type="text/javascript" src="jquery/jquery-3.6.0.js"></script>
```

**2. CDN Based Version** — jQuery Content Delivery Network (CDN), referenced directly from the jQuery CDN domain:
```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
```

### 5.3 jQuery DOM

jQuery contains methods for changing and manipulating DOM elements and attributes.

### 5.4 jQuery DOM Insertions

| Method | Description |
|---|---|
| `append()` | Inserts content at the end of the selected elements |
| `prepend()` | Inserts content at the beginning of the selected elements |
| `after()` | Inserts content after the selected elements |
| `before()` | Inserts content before the selected elements |

### 5.5 jQuery Effects

jQuery enables adding effects on a web page. jQuery effects can be categorized into:

- Display
- Fading
- Sliding
- Hiding/Showing
- Other animation effects

### 5.6 jQuery with JSON

**JSON (JavaScript Object Notation)** is a standard text-based format for representing structured data, based on JavaScript object syntax.

- A syntax for storing and exchanging data
- A lightweight data-interchange format
- "Self-describing" and easy to understand
- Language independent

**JSON Syntax Rules:**
- JSON data is in name/value pairs
- Data is separated by commas
- Curly braces `{}` hold objects
- Square brackets `[]` hold arrays

**JSON Arrays:**
- An array is an ordered collection of values
- Values are enclosed within brackets `[]`
- Values are separated by commas

---

## 6. jQuery Debugging

> Placeholder — the source notepad did not include dedicated jQuery debugging content. Add selector-testing techniques, `.length` checks, common jQuery pitfalls, or version-conflict debugging here once available.

---

## 7. Web Design — Best Practices

### 7.1 Characteristics of Good Quality Code

| Characteristic | Description |
|---|---|
| **Robustness** | Ability to handle errors in program execution |
| **Portability** | The web design should work the same across different computers, browsers, monitors, and resolutions |
| **Maintainability** | Easy to add new features, modify existing features, or fix issues with minimum effort, without affecting other modules and functionalities |
| **Readability** | Ensures the code is understood by everyone else |

---

## Quick Revision Checklist

- [ ] Can define Internet, World Wide Web, Web Browser, Web Server
- [ ] Can differentiate Web Page vs Website vs Web Application
- [ ] Can differentiate Frontend vs Backend development
- [ ] Can differentiate Static vs Dynamic web pages, with request/response flow
- [ ] Can list HTML structure and basic tags
- [ ] Can differentiate Semantic vs Non-semantic elements, and list new semantic tags
- [ ] Can list HTML form attributes and input elements
- [ ] Can list JavaScript primitive vs reference data types
- [ ] Can differentiate Declaration, Initialization, Assignment
- [ ] Can differentiate Global vs Local variable scope
- [ ] Can use `==` vs `===` and `!=` vs `!==` correctly
- [ ] Can list JavaScript control structures (decision making + looping)
- [ ] Can explain client-side vs server-side validation timing
- [ ] Can explain what the DOM and Window object represent
- [ ] Can explain what a cookie is and why it's used
- [ ] Can explain what jQuery is and who created it
- [ ] Can list jQuery DOM insertion methods
- [ ] Can list JSON syntax rules
- [ ] Can list the 4 characteristics of good quality code