# Lesson 2: Variables, Values, Data Types & Operators

## Course

**JavaScript → React.js → Node.js → PostgreSQL → MongoDB → Full-Stack Development**

---

# 1. Learning Objectives

By the end of this lesson, the learner should be able to:

- Explain what a variable is.
- Create variables using `const`, `let`, and `var`.
- Understand the difference between `const` and `let`.
- Understand what a value is.
- Identify common JavaScript data types.
- Work with strings, numbers, and booleans.
- Understand `undefined` and `null`.
- Understand arrays and objects at a basic level.
- Use arithmetic operators.
- Use assignment operators.
- Understand the difference between `=` and `===`.
- Use comparison operators.
- Use logical operators.
- Write expressions.
- Apply variables and operators in practical programs.

---

# 2. What Is a Variable?

A variable is a named place used by a program to hold a value.

For example:

```js
const name = "John";
```

Here:

```text
name
```

is the variable.

And:

```text
"John"
```

is the value.

Think of a variable as a labeled box:

```text
┌─────────────────┐
│ name            │
│                 │
│ "John"          │
└─────────────────┘
```

The label is:

```text
name
```

The value stored inside is:

```text
"John"
```

---

# 3. Why Do We Need Variables?

Imagine building a Student Management System.

Without variables, you might repeatedly write:

```js
console.log("John");
console.log("John");
console.log("John");
```

That becomes difficult to maintain.

Instead:

```js
const studentName = "John";

console.log(studentName);
console.log(studentName);
console.log(studentName);
```

Now the student's name has a meaningful name in the program.

This becomes extremely important when applications become large.

---

# 4. Creating a Variable

The most common modern ways of creating variables are:

```js
const
let
```

For example:

```js
const name = "John";
let age = 20;
```

The general structure is:

```text
keyword variableName = value;
```

Example:

```js
const course = "Information Technology";
```

Breaking it down:

```text
const
 ↓
Declaration keyword

course
 ↓
Variable name

=
 ↓
Assignment operator

"Information Technology"
 ↓
Value
```

---

# 5. `const`

Use `const` when the variable should not be reassigned.

Example:

```js
const name = "John";

console.log(name);
```

You can read the value:

```js
console.log(name);
```

But you cannot reassign it:

```js
name = "Peter";
```

This produces an error.

The important idea is:

```text
const
=
This variable binding cannot be reassigned.
```

---

# 6. `let`

Use `let` when the variable needs to be reassigned.

Example:

```js
let age = 20;

console.log(age);

age = 21;

console.log(age);
```

Output:

```text
20
21
```

The variable started with:

```text
20
```

and was later assigned:

```text
21
```

---

# 7. `const` vs `let`

The basic rule is:

```text
const
→ use when reassignment is not needed

let
→ use when reassignment is needed
```

Example:

```js
const name = "John";
const country = "Rwanda";

let age = 20;

age = 21;
```

A good modern JavaScript habit is:

> Start with `const`. Use `let` only when you know the value needs to be reassigned.

---

# 8. What About `var`?

Older JavaScript code often uses:

```js
var
```

Example:

```js
var name = "John";
```

Modern JavaScript generally prefers:

```js
const
let
```

because they have clearer scoping behavior and reduce certain programming mistakes.

You should understand `var` because you will encounter it in older code, but don't make it your default for new code.

---

# 9. Variable Naming

Variable names should describe the value they contain.

Good:

```js
const studentName = "John";
const studentAge = 21;
const studentCourse = "IT";
```

Bad:

```js
const x = "John";
const a = 21;
const thing = "IT";
```

Meaningful names make code easier to understand.

---

# 10. Camel Case

JavaScript developers commonly use **camelCase**.

Examples:

```js
studentName
studentAge
studentCourse
firstName
lastName
phoneNumber
emailAddress
```

Notice:

```text
firstName
```

not:

```text
first_name
```

Although `snake_case` is valid in JavaScript, camelCase is the common convention for JavaScript variables.

---

# 11. Variable Names Rules

A variable name:

- can contain letters
- can contain numbers
- can contain `_`
- can contain `$`
- cannot start with a number
- cannot contain spaces
- cannot use reserved JavaScript keywords

Valid:

```js
const studentName = "John";
const student2 = "Peter";
const _value = 10;
```

Invalid:

```js
const 2student = "John";
```

Invalid:

```js
const student name = "John";
```

---

# 12. What Is a Value?

A variable stores a value.

For example:

```js
const age = 21;
```

Here:

```text
Variable → age
Value    → 21
```

Another:

```js
const name = "John";
```

```text
Variable → name
Value    → "John"
```

Another:

```js
const isActive = true;
```

```text
Variable → isActive
Value    → true
```

Different values have different **data types**.

---

# 13. Data Types

JavaScript has several data types.

Important ones for this course include:

```text
String
Number
Boolean
Undefined
Null
Object
Array
```

We will study them gradually.

---

# 14. String

A string represents text.

Examples:

```js
const name = "John";
const country = "Rwanda";
const course = "Information Technology";
```

Strings can use:

```js
"Hello"
```

or:

```js
'Hello'
```

Both are valid.

For example:

```js
const firstName = "John";
const lastName = 'Peter';
```

---

# 15. Numbers

JavaScript uses the `number` type for ordinary numeric values.

Examples:

```js
const age = 21;
const marks = 85;
const price = 1500;
const temperature = 24.5;
```

Both integers and decimal numbers are `number` values.

---

# 16. Boolean

A boolean has only two possible values:

```text
true
false
```

Example:

```js
const isStudent = true;
const isAdmin = false;
```

Booleans are extremely important in programming because they allow us to represent conditions.

For example:

```js
const isLoggedIn = true;
```

Later:

```js
if (isLoggedIn) {
    // allow access
}
```

This becomes the foundation of conditional programming.

---

# 17. `undefined`

A variable can exist without having a value assigned to it.

Example:

```js
let studentName;

console.log(studentName);
```

The result is:

```text
undefined
```

This means:

> The variable exists, but no value has been assigned to it.

---

# 18. `null`

`null` is commonly used to explicitly represent the absence of a value.

Example:

```js
const selectedStudent = null;
```

This communicates:

> There is currently no selected student.

A useful mental distinction is:

```text
undefined
→ value has not been provided

null
→ intentionally no value
```

The exact semantics can be more nuanced, but this distinction is useful at this stage.

---

# 19. Arrays

An array stores multiple values in an ordered collection.

Example:

```js
const students = ["John", "Peter", "Mary"];
```

Think of it as:

```text
students
   ↓
┌───────┬───────┬───────┐
│ John  │ Peter │ Mary  │
└───────┴───────┴───────┘
   0       1       2
```

Arrays use zero-based indexes.

Therefore:

```js
students[0]
```

returns:

```text
John
```

and:

```js
students[1]
```

returns:

```text
Peter
```

We will study arrays much more deeply later.

---

# 20. Objects

An object groups related information together.

Example:

```js
const student = {
    name: "John",
    age: 21,
    course: "IT"
};
```

Think of the object as:

```text
student
   │
   ├── name → "John"
   ├── age → 21
   └── course → "IT"
```

You can access a property using:

```js
student.name
```

or:

```js
student.age
```

Objects will become one of the most important concepts in the entire course.

React, Node.js, APIs, JSON, MongoDB, and PostgreSQL applications all rely heavily on objects and structured data.

---

# 21. Checking Data Types with `typeof`

JavaScript provides:

```js
typeof
```

to inspect a value's type.

Example:

```js
console.log(typeof "John");
```

Result:

```text
string
```

Try:

```js
console.log(typeof 21);
```

Result:

```text
number
```

Try:

```js
console.log(typeof true);
```

Result:

```text
boolean
```

And:

```js
console.log(typeof undefined);
```

Result:

```text
undefined
```

---

# 22. A Strange JavaScript Detail

Try:

```js
console.log(typeof null);
```

JavaScript returns:

```text
object
```

This is a historical behavior in JavaScript.

It does **not** mean that `null` is actually an object in the conceptual sense we are learning.

It is simply one of JavaScript's well-known quirks.

You may also encounter:

```js
typeof [];
```

which returns:

```text
object
```

because arrays are objects in JavaScript.

Don't worry about these details yet.

---

# 23. Arithmetic Operators

JavaScript can perform mathematical operations.

The main arithmetic operators are:

```text
+
-
*
/
%
**
```

They mean:

```text
+   addition
-   subtraction
*   multiplication
/   division
%   remainder
**  exponentiation
```

---

# 24. Addition

```js
const result = 10 + 20;

console.log(result);
```

Output:

```text
30
```

---

# 25. Subtraction

```js
const result = 50 - 20;

console.log(result);
```

Output:

```text
30
```

---

# 26. Multiplication

```js
const result = 10 * 5;

console.log(result);
```

Output:

```text
50
```

---

# 27. Division

```js
const result = 100 / 4;

console.log(result);
```

Output:

```text
25
```

---

# 28. Remainder `%`

The `%` operator returns the remainder after division.

Example:

```js
console.log(10 % 3);
```

Result:

```text
1
```

because:

```text
10 ÷ 3
= 3 remainder 1
```

This becomes useful for tasks such as determining whether a number is even or odd.

---

# 29. Exponentiation

```js
console.log(2 ** 3);
```

Result:

```text
8
```

Because:

```text
2 × 2 × 2 = 8
```

---

# 30. Assignment Operator

The assignment operator is:

```js
=
```

Example:

```js
let age = 20;
```

It means:

> Assign the value `20` to `age`.

This is different from mathematical equality.

In JavaScript:

```js
age = 20;
```

means assignment.

---

# 31. Assignment vs Equality

This distinction is extremely important.

```js
=
```

means:

```text
assignment
```

while:

```js
===
```

means:

```text
strict equality comparison
```

Example:

```js
let age = 20;
```

Assignment.

But:

```js
age === 20
```

asks:

> Is `age` exactly equal to `20`?

The result is a boolean:

```text
true
```

---

# 32. Comparison Operators

Common comparison operators are:

```text
===    strictly equal
!==    strictly not equal
>      greater than
<      less than
>=     greater than or equal
<=     less than or equal
```

Example:

```js
console.log(10 > 5);
```

Result:

```text
true
```

Another:

```js
console.log(10 < 5);
```

Result:

```text
false
```

---

# 33. Strict Equality `===`

Example:

```js
const age = 20;

console.log(age === 20);
```

Result:

```text
true
```

Another:

```js
console.log(age === 25);
```

Result:

```text
false
```

`===` checks both value and type.

For example:

```js
console.log(10 === "10");
```

Result:

```text
false
```

because:

```text
10
```

is a number, while:

```text
"10"
```

is a string.

---

# 34. Strict Inequality `!==`

Example:

```js
const age = 20;

console.log(age !== 30);
```

Result:

```text
true
```

It asks:

> Is the value not strictly equal?

---

# 35. Greater Than

```js
const marks = 75;

console.log(marks > 50);
```

Result:

```text
true
```

---

# 36. Less Than

```js
const age = 15;

console.log(age < 18);
```

Result:

```text
true
```

---

# 37. Greater Than or Equal

```js
const marks = 70;

console.log(marks >= 70);
```

Result:

```text
true
```

This is especially useful for grading systems.

---

# 38. Less Than or Equal

```js
const age = 18;

console.log(age <= 18);
```

Result:

```text
true
```

---

# 39. Logical Operators

JavaScript provides:

```text
&&
||
!
```

These are:

```text
&&  AND
||  OR
!   NOT
```

They allow us to combine conditions.

We will use them heavily in the next lesson.

---

# 40. AND `&&`

Example:

```js
const age = 20;
const hasId = true;

console.log(age >= 18 && hasId === true);
```

Both conditions must be true.

Conceptually:

```text
Condition 1
     AND
Condition 2
     ↓
Result
```

---

# 41. OR `||`

With OR, at least one condition needs to be true.

Example:

```js
const isAdmin = false;
const isTeacher = true;

console.log(isAdmin || isTeacher);
```

Result:

```text
true
```

because one of the two conditions is true.

---

# 42. NOT `!`

The `!` operator reverses a boolean.

Example:

```js
const isLoggedIn = true;

console.log(!isLoggedIn);
```

Result:

```text
false
```

Because:

```text
true
```

becomes:

```text
false
```

---

# 43. Expressions

An expression is code that produces a value.

For example:

```js
10 + 20
```

produces:

```text
30
```

This is an expression.

Another:

```js
age >= 18
```

produces:

```text
true
```

Another:

```js
name === "John"
```

produces:

```text
true
```

Expressions become extremely important when we start writing conditions and functions.

---

# 44. Combining Variables and Operators

Now let's create something closer to a real application.

```js
const studentName = "John";
const marks = 75;

const passed = marks >= 50;

console.log(studentName);
console.log(marks);
console.log(passed);
```

Output:

```text
John
75
true
```

We have already started building logic for a student system.

---

# 45. Practical Example — Student Information

```js
const studentName = "John";
const age = 21;
const course = "Information Technology";
const marks = 78;
const isActive = true;

console.log(studentName);
console.log(age);
console.log(course);
console.log(marks);
console.log(isActive);
```

This represents a simple student's data.

Later, instead of keeping these as separate variables, we will group them into an object:

```js
const student = {
    name: "John",
    age: 21,
    course: "Information Technology",
    marks: 78,
    isActive: true
};
```

That is one reason understanding variables and values is important before learning objects deeply.

---

# 46. Practical Example — Calculating Student Marks

Suppose a student has:

```js
const mathematics = 80;
const programming = 75;
const database = 85;
```

We can calculate the total:

```js
const total = mathematics + programming + database;

console.log(total);
```

Output:

```text
240
```

We can calculate the average:

```js
const average = total / 3;

console.log(average);
```

Output:

```text
80
```

This is already useful application logic.

---

# 47. Practical Example — Student Eligibility

Suppose a student needs at least 50 marks to pass.

```js
const marks = 65;

const passed = marks >= 50;

console.log(passed);
```

Result:

```text
true
```

If:

```js
const marks = 35;
```

then:

```js
const passed = marks >= 50;
```

produces:

```text
false
```

We will use this type of expression extensively when learning conditions.

---

# 48. Practical Example — Login State

```js
const isLoggedIn = true;

console.log(isLoggedIn);
```

We can check:

```js
console.log(isLoggedIn === true);
```

or simply:

```js
console.log(isLoggedIn);
```

This becomes important when building authentication later.

---

# 49. Important `const` Concept: Objects and Arrays

There is an important detail about `const`.

This is not allowed:

```js
const students = [];

students = [];
```

because the variable binding cannot be reassigned.

However, you can modify the array:

```js
const students = [];

students.push("John");

console.log(students);
```

Result:

```text
["John"]
```

Similarly:

```js
const student = {
    name: "John"
};

student.name = "Peter";

console.log(student.name);
```

This works.

The key idea is:

> `const` prevents reassignment of the variable binding; it does not make every object or array inside it immutable.

We will revisit this concept when working with React state.

---

# 50. Practical Exercise 1 — Personal Information

Create:

```text
exercise2-1.js
```

Create variables for:

```text
first name
last name
age
country
course
```

Then print all of them.

Example structure:

```js
const firstName = "John";
const lastName = "Peter";
const age = 21;
const country = "Rwanda";
const course = "IT";

console.log(firstName);
console.log(lastName);
console.log(age);
console.log(country);
console.log(course);
```

Use your own fictional data.

---

# 51. Practical Exercise 2 — Calculator

Create:

```text
calculator.js
```

Create two variables:

```js
const number1 = 20;
const number2 = 10;
```

Calculate and print:

- addition
- subtraction
- multiplication
- division
- remainder

Expected operations:

```js
number1 + number2
number1 - number2
number1 * number2
number1 / number2
number1 % number2
```

---

# 52. Practical Exercise 3 — Student Marks

Create:

```text
student-marks.js
```

Create:

```js
const mathematics = 80;
const programming = 75;
const database = 85;
```

Calculate:

```text
total
average
```

Then determine whether the student passed:

```text
average >= 50
```

Print:

```text
Total
Average
Passed
```

---

# 53. Practical Exercise 4 — Age Comparison

Create:

```text
age-check.js
```

Create:

```js
const age = 20;
```

Then print the result of:

```text
age >= 18
age < 18
age === 20
age !== 30
```

Observe which results are `true` and which are `false`.

---

# 54. Practical Exercise 5 — Login Information

Create:

```text
login-check.js
```

Create:

```js
const username = "admin";
const password = "1234";
```

Then create:

```js
const correctUsername = username === "admin";
const correctPassword = password === "1234";
```

Finally:

```js
const loginValid = correctUsername && correctPassword;

console.log(loginValid);
```

At this stage, this is only a programming exercise.

**Do not use this pattern for real authentication.**

Real authentication will use hashed passwords, backend verification, authentication tokens/sessions, and protected routes.

---

# 55. Practical Exercise 6 — `let`

Create:

```text
age.js
```

Write:

```js
let age = 20;

console.log(age);

age = 21;

console.log(age);

age = 22;

console.log(age);
```

Observe how the value changes.

Then change `let` to `const` and see what happens.

---

# 56. Practical Exercise 7 — Data Types

Create:

```text
types.js
```

Write:

```js
const name = "John";
const age = 21;
const isStudent = true;
let course;
const selectedStudent = null;

console.log(typeof name);
console.log(typeof age);
console.log(typeof isStudent);
console.log(typeof course);
console.log(typeof selectedStudent);
```

Observe the results.

Pay particular attention to:

```text
typeof null
```

---

# 57. Common Beginner Mistakes

## Mistake 1: Using `=` when you mean comparison

Incorrect:

```js
age = 18
```

when your intention is to ask:

> Is age 18?

Use:

```js
age === 18
```

---

## Mistake 2: Using `var` everywhere

Modern JavaScript should generally prefer:

```js
const
let
```

Use `var` mainly when reading or maintaining older JavaScript code.

---

## Mistake 3: Using `let` for everything

This works:

```js
let name = "John";
```

But if the value never needs reassignment, prefer:

```js
const name = "John";
```

---

## Mistake 4: Confusing `"10"` with `10`

These are different:

```js
"10"
```

and:

```js
10
```

The first is a string.

The second is a number.

This difference becomes very important when working with forms, APIs, and databases.

---

## Mistake 5: Poor variable names

Avoid:

```js
const x = 75;
```

Prefer:

```js
const marks = 75;
```

Good names make code easier to read.

---

# 58. Mental Model for This Lesson

Think about JavaScript data like this:

```text
Variable
   ↓
stores a
   ↓
Value
   ↓
has a
   ↓
Data Type
```

For example:

```text
studentAge
    ↓
21
    ↓
number
```

Another:

```text
studentName
    ↓
"John"
    ↓
string
```

Another:

```text
isActive
    ↓
true
    ↓
boolean
```

---

# 59. Important Mental Model for Operators

Think of operators as tools that work with values.

```text
Arithmetic
→ calculate

Comparison
→ compare

Logical
→ combine conditions

Assignment
→ assign/change values
```

For example:

```js
const marks = 80;
```

Assignment.

```js
marks >= 50
```

Comparison.

```js
marks + 10
```

Arithmetic.

```js
marks >= 50 && marks <= 100
```

Logical combination.

---

# 60. Teacher Checkpoint

Before moving to the next lesson, the learner should be able to answer:

1. What is a variable?

2. What is a value?

3. What is the difference between `const` and `let`?

4. What is `var`?

5. What is a string?

6. What is a number?

7. What is a boolean?

8. What does `undefined` mean?

9. What is `null`?

10. What is an array?

11. What is an object?

12. What does `typeof` do?

13. What does `=` mean?

14. What does `===` mean?

15. What does `!==` mean?

16. What does `&&` mean?

17. What does `||` mean?

18. What does `!` mean?

19. What does `%` do?

20. What is an expression?

---

# 61. Mini Challenge

Build a small **Student Result Calculator**.

Create:

```text
student-result.js
```

Use:

```text
Student name
Mathematics
Programming
Database
```

Calculate:

```text
Total
Average
```

Then create a boolean:

```text
Passed
```

where the student passes if:

```text
average >= 50
```

For example:

```js
const studentName = "John";

const mathematics = 80;
const programming = 75;
const database = 85;

const total = mathematics + programming + database;
const average = total / 3;

const passed = average >= 50;

console.log(studentName);
console.log(total);
console.log(average);
console.log(passed);
```

Then change the marks and observe how the result changes.

---

# 62. Lesson Summary

In this lesson, we moved from simply printing messages to storing and manipulating information.

We learned:

```text
Variable
↓
stores
↓
Value
↓
has a
↓
Data Type
```

We learned the main variable declarations:

```js
const
let
var
```

with the modern rule:

```text
Start with const.
Use let when reassignment is needed.
Understand var because you will encounter it in older code.
```

We learned important data types:

```text
String
Number
Boolean
Undefined
Null
Object
Array
```

We also learned operators:

```text
Arithmetic
+
-
*
/
%
**

Comparison
===
!==
>
<
>=
<=

Logical
&&
||
!

Assignment
=
```

Most importantly, we began combining these concepts to create actual application logic.

For example:

```js
const marks = 75;

const passed = marks >= 50;

console.log(passed);
```

This is the beginning of programming logic.

The next lesson will build directly on these concepts by introducing:

```text
if
else
else if
nested conditions
truthy/falsy
ternary operator
switch
```

We will use them to make JavaScript **make decisions**.