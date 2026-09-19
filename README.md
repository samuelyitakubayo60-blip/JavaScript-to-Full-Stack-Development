# Lesson 1: Introduction to JavaScript & Development Environment

## Course

**JavaScript → React.js → Node.js → PostgreSQL → MongoDB → Full-Stack Development**

---

# 1. Learning Objectives

By the end of this lesson, the learner should be able to:

- Explain what JavaScript is.
- Understand why JavaScript is called a programming language.
- Understand what a runtime environment is.
- Explain the difference between JavaScript and Node.js.
- Explain where JavaScript can run.
- Understand browser JavaScript.
- Understand Node.js.
- Set up a JavaScript development environment.
- Run JavaScript from a browser console.
- Create and execute a `.js` file with Node.js.
- Use `console.log()`.
- Understand the basic JavaScript development workflow.

---

# 2. What Is JavaScript?

JavaScript is a **programming language**.

A programming language allows us to give instructions to a computer.

For example:

```js
console.log("Hello, JavaScript!");
```

We are telling the computer:

> Display the text `"Hello, JavaScript!"`.

JavaScript is widely used for web development, but it is not limited to websites.

It can be used to build:

- Interactive websites
- Web applications
- Frontend applications
- Backend APIs
- Servers
- Command-line applications
- Automation scripts
- Desktop applications
- Mobile applications
- Full-stack applications

In this course, we are going to use JavaScript to eventually build a complete **Student Management System**.

---

# 3. Why Are We Starting With JavaScript?

Our final application will contain several technologies:

```text
React.js
Node.js
Express
PostgreSQL
MongoDB
Bootstrap
Tailwind CSS
```

But JavaScript is the foundation for several of them.

The relationship looks like this:

```text
                    JavaScript
                        │
            ┌───────────┴───────────┐
            │                       │
         React.js                 Node.js
         Frontend                 Backend
            │                       │
            └───────────┬───────────┘
                        │
                    Full Stack
```

React uses JavaScript.

Node.js executes JavaScript on the backend.

Express runs on Node.js.

Therefore, before learning React and Node.js, we need a strong JavaScript foundation.

---

# 4. JavaScript Is a Language

This distinction is important.

JavaScript is **not** the same thing as:

```text
Chrome
Node.js
React
Express
```

These are different things.

Think of it this way:

```text
JavaScript
= Programming language
```

while:

```text
Browser
= Environment that can execute JavaScript

Node.js
= Runtime that can execute JavaScript

React
= JavaScript library for building user interfaces

Express
= Backend framework/library built for Node.js
```

We will study each of these later.

---

# 5. What Is a Runtime?

Writing JavaScript code is one thing.

Something must actually execute that code.

That is where a **runtime environment** comes in.

Think of the process as:

```text
JavaScript Code
       ↓
JavaScript Runtime
       ↓
Program Executes
```

For example:

```js
console.log("Hello");
```

The code itself does not magically execute.

A JavaScript runtime executes it.

Two important environments for us are:

```text
Browser
Node.js
```

---

# 6. JavaScript in the Browser

Web browsers such as:

- Google Chrome
- Microsoft Edge
- Firefox
- Safari

can execute JavaScript.

For example, a web page might contain:

```html
<button>Click Me</button>
```

JavaScript can make that button interactive.

Conceptually:

```text
HTML
 ↓
Browser
 ↓
JavaScript
 ↓
Interactive Website
```

Later we will learn how JavaScript can:

- find HTML elements
- change text
- respond to clicks
- handle forms
- communicate with APIs

This part of JavaScript is called **frontend development**.

---

# 7. JavaScript in Node.js

Node.js allows JavaScript to run **outside the browser**.

This is extremely important.

Without Node.js, beginners often think:

> JavaScript is only for websites.

That is not true.

Node.js allows us to use JavaScript for backend development.

For example:

```text
Browser
   ↓
React
   ↓
HTTP Request
   ↓
Node.js + Express
   ↓
Database
```

Later our Student Management System will use exactly this architecture.

---

# 8. Browser vs Node.js

Both can execute JavaScript.

But they provide different environments.

| Feature                | Browser      | Node.js        |
| ---------------------- | ------------ | -------------- |
| Executes JavaScript    | Yes          | Yes            |
| Used for frontend      | Yes          | No             |
| Used for backend       | Not normally | Yes            |
| DOM available          | Yes          | No browser DOM |
| Browser APIs           | Yes          | Different APIs |
| Can create HTTP server | Not normally | Yes            |
| Common use             | Web UI       | Backend/API    |

The important point is:

> **JavaScript is the language. The environment determines what additional capabilities are available.**

---

# 9. Your Development Environment

Before writing serious JavaScript programs, we need some tools.

We will use:

```text
Visual Studio Code
Node.js
Web Browser
Terminal
```

Git will also become important later.

---

# 10. Visual Studio Code

Visual Studio Code is our code editor.

We will use it to:

- create files
- write JavaScript
- organize projects
- use extensions
- run terminal commands
- debug applications
- eventually work with React and Node.js

Create a folder for the course:

```text
javascript-course
```

Open that folder in Visual Studio Code.

---

# 11. Check Node.js

Open the terminal in Visual Studio Code.

Run:

```bash
node --version
```

You should see something similar to:

```text
v22.x.x
```

The exact version may be different.

Then check npm:

```bash
npm --version
```

You should also receive a version number.

---

# 12. What Is npm?

You will hear the word **npm** frequently.

npm is the package manager commonly used with Node.js.

It allows us to install JavaScript packages.

For example, later we may install:

```bash
npm install express
```

or:

```bash
npm install mongodb
```

or:

```bash
npm install bcrypt
```

npm will become extremely important when we start building real applications.

For now, simply understand:

```text
Node.js
    ↓
npm
    ↓
Install/manage JavaScript packages
```

---

# 13. Your First JavaScript Program

Inside your project folder, create:

```text
lesson1.js
```

The `.js` extension means this is a JavaScript source file.

Write:

```js
console.log("Hello, JavaScript!");
```

Save the file.

Then run:

```bash
node lesson1.js
```

You should get:

```text
Hello, JavaScript!
```

Congratulations.

You have executed your first JavaScript program using Node.js.

---

# 14. Understanding `console.log()`

You will use:

```js
console.log()
```

many times during this course.

It displays information in the console.

For example:

```js
console.log("Hello");
console.log("Welcome");
console.log("I am learning JavaScript");
```

Output:

```text
Hello
Welcome
I am learning JavaScript
```

We can also print numbers:

```js
console.log(10);
console.log(50);
console.log(100);
```

Output:

```text
10
50
100
```

We will study why text and numbers behave differently when we learn data types.

---

# 15. Multiple Instructions

JavaScript programs can contain many instructions.

For example:

```js
console.log("Student Management System");
console.log("Welcome");
console.log("Loading students...");
console.log("Application started");
```

When executed:

```text
Student Management System
Welcome
Loading students...
Application started
```

For now, use this simple mental model:

```text
JavaScript program
       ↓
Instruction 1
       ↓
Instruction 2
       ↓
Instruction 3
       ↓
Instruction 4
```

Later, conditions, loops, functions, events, and asynchronous operations will make the execution model more sophisticated.

---

# 16. JavaScript Statements

You will often see JavaScript instructions written as statements.

Example:

```js
console.log("Hello");
```

Another:

```js
console.log("Welcome");
```

Semicolons are commonly used to terminate statements:

```js
console.log("Hello");
console.log("World");
```

JavaScript can often automatically insert semicolons, but during learning it is useful to consistently write them.

---

# 17. Comments

Comments allow us to write notes in our code.

A single-line comment starts with:

```js
//
```

Example:

```js
// Display welcome message
console.log("Welcome");
```

JavaScript ignores the comment when executing the program.

We can also write multi-line comments:

```js
/*
  This program demonstrates
  basic JavaScript output.
*/

console.log("Hello");
```

Comments should help humans understand the code.

---

# 18. Running JavaScript in the Browser

JavaScript does not have to be run only with Node.js.

Open Google Chrome.

Press:

```text
F12
```

Then select:

```text
Console
```

You can type:

```js
console.log("Hello from the browser!");
```

Press Enter.

You should see:

```text
Hello from the browser!
```

You have now executed JavaScript in the browser.

---

# 19. Browser Console Experiment

Try:

```js
console.log(10);
console.log(20);
console.log(10 + 20);
```

You should get:

```text
10
20
30
```

Notice that JavaScript can perform calculations.

We will study operators later.

---

# 20. The Big Picture

At this point, understand this architecture:

```text
                     JavaScript
                         │
             ┌───────────┴───────────┐
             │                       │
          Browser                  Node.js
             │                       │
             ▼                       ▼
        Frontend UI             Backend/API
             │                       │
             └───────────┬───────────┘
                         │
                    Full-Stack App
```

Later:

```text
React
 ↓
Node.js + Express
 ↓
PostgreSQL / MongoDB
```

---

# 21. Our Final Project

Throughout this course, we will progressively build a:

# Student Management System

The final system will eventually contain:

```text
Authentication
Dashboard
Students
Student CRUD
Search
Filtering
Database
REST API
Role-based access
Responsive UI
```

The technology stack will be:

```text
Frontend
→ React.js

Styling
→ Bootstrap 5 / Tailwind CSS

Backend
→ Node.js + Express

Database
→ PostgreSQL

Additional database practice
→ MongoDB
```

But we are not going to jump directly into React.

We will build the foundation first.

---

# 22. The Learning Path

Our progression is:

```text
JavaScript Fundamentals
        ↓
Modern JavaScript
        ↓
DOM + Events
        ↓
Modules
        ↓
JSON
        ↓
Fetch + APIs
        ↓
Async JavaScript
        ↓
React
        ↓
Node.js + Express
        ↓
PostgreSQL
        ↓
MongoDB
        ↓
Authentication
        ↓
Full-Stack Application
```

Every stage depends on the previous stages.

That is why we are starting with JavaScript fundamentals.

---

# 23. Practical Exercise 1 — Personal Introduction

Create:

```text
exercise1.js
```

Write a program that prints:

```text
My name is __________.
I am learning JavaScript.
I am learning full-stack development.
```

Use three `console.log()` statements.

For example:

```js
console.log("My name is Samuel.");
console.log("I am learning JavaScript.");
console.log("I am learning full-stack development.");
```

Run:

```bash
node exercise1.js
```

---

# 24. Practical Exercise 2 — Five Messages

Create:

```text
exercise2.js
```

Print five different messages.

Example:

```js
console.log("Welcome");
console.log("JavaScript is powerful");
console.log("I am practicing");
console.log("I will build applications");
console.log("Let's code!");
```

Use your own messages.

---

# 25. Practical Exercise 3 — Numbers

Create:

```text
exercise3.js
```

Write:

```js
console.log(10);
console.log(20);
console.log(30);
console.log(40);
console.log(50);
```

Then try:

```js
console.log(10 + 20);
console.log(100 - 50);
console.log(5 * 5);
console.log(100 / 10);
```

Don't worry about memorizing operators yet.

We will study them properly.

---

# 26. Practical Exercise 4 — Browser Console

Open the browser console and execute:

```js
console.log("I am running JavaScript in the browser");
```

Then:

```js
console.log(100);
```

Then:

```js
console.log(50 + 50);
```

Then:

```js
console.log("Student Management System");
```

---

# 27. Practical Exercise 5 — Compare Environments

Run this in your browser console:

```js
console.log(window);
```

Then try the same code with Node.js:

```js
console.log(window);
```

Observe the difference.

The goal is not to memorize the `window` object.

The goal is to understand:

```text
Browser ≠ Node.js
```

even though both can execute JavaScript.

---

# 28. Common Beginner Mistakes

## Mistake 1: Thinking Node.js is a programming language

Incorrect:

```text
Node.js = programming language
```

Correct:

```text
JavaScript = programming language
Node.js = JavaScript runtime
```

---

## Mistake 2: Thinking JavaScript only works in browsers

Incorrect:

```text
JavaScript = browser only
```

Correct:

```text
JavaScript
→ Browser
→ Node.js
→ Other JavaScript runtimes
```

---

## Mistake 3: Confusing React with JavaScript

React is not a replacement for JavaScript.

React is built around JavaScript.

You need JavaScript knowledge before React becomes comfortable.

---

## Mistake 4: Copying code without running it

Don't just read:

```js
console.log("Hello");
```

Actually run it.

Programming is learned through practice.

---

## Mistake 5: Being afraid of errors

Errors are normal.

For example:

```js
console.log("Hello"
```

will produce an error because something is missing.

The correct reaction is not:

> "I'm bad at programming."

The correct reaction is:

> "What does the error message tell me?"

Debugging is part of professional development.

---

# 29. The Professional Development Cycle

From the beginning, develop this habit:

```text
Write
  ↓
Save
  ↓
Run
  ↓
Observe
  ↓
Find problems
  ↓
Fix
  ↓
Run again
```

This cycle will remain important when we are building:

```text
React applications
Node APIs
PostgreSQL queries
MongoDB applications
Full-stack systems
```

---

# 30. What You Should Understand — Not Memorize

You should understand these ideas:

### JavaScript

A programming language.

### Runtime

An environment capable of executing JavaScript.

### Browser

A JavaScript runtime environment with browser-specific APIs.

### Node.js

A JavaScript runtime that allows JavaScript to run outside the browser.

### `console.log()`

Used to display information in the console.

### `.js`

The common file extension for JavaScript source files.

### npm

A package manager used to install and manage JavaScript packages.

---

# 31. Teacher Checkpoint

Before moving to Lesson 2, the learner should answer these questions without simply reading the answers.

### Question 1

What is JavaScript?

### Question 2

Is JavaScript the same thing as Node.js?

### Question 3

What is a runtime?

### Question 4

Where can JavaScript run?

### Question 5

What is Node.js used for?

### Question 6

What is `console.log()` used for?

### Question 7

How do you execute a JavaScript file called `app.js` using Node.js?

### Question 8

What is npm?

### Question 9

What is the difference between browser JavaScript and Node.js?

### Question 10

Why should a programmer run their code frequently while developing?

---

# 32. Mini Challenge

Without copying an example, create:

```text
student.js
```

It should print a small introduction to a fictional student.

For example, it could output:

```text
Student Management System
-------------------------
Name: John
Age: 21
Course: Information Technology
Status: Active
```

At this stage, you can simply print each line using `console.log()`.

Do not worry about variables yet.

We will introduce variables in the next lesson.

---

# 33. Lesson Summary

In this lesson, we established the foundation of the entire course.

We learned that:

```text
JavaScript
= Programming language
```

and:

```text
Node.js
= Runtime that executes JavaScript outside the browser
```

We also learned that browsers can execute JavaScript.

The basic model is:

```text
JavaScript
     ↓
Runtime
     ├── Browser → Frontend
     └── Node.js → Backend
```

We created our first JavaScript file:

```text
lesson1.js
```

and executed it using:

```bash
node lesson1.js
```

We also executed JavaScript directly in the browser console.

Most importantly, we established the development mindset:

```text
Write
 ↓
Run
 ↓
Test
 ↓
Debug
 ↓
Improve
```

The next lesson will move from simply printing information to storing and manipulating information using:

```text
Variables
Values
Data Types
Operators
```

That is where we begin writing real JavaScript programs.
