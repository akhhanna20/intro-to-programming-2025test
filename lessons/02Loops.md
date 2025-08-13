# Loops

## Overview

No overview provided

## Learning Objectives

Learning objectives will be defined as the lesson progresses.

## Topics Covered

Topics will be covered as the lesson progresses.

## Status

pending

## Assignment

Assignment for Lesson 2

### Objective

No objective specified

### Expected Capabilities

Expected capabilities will be defined as the lesson progresses.

### Instructions

Instructions will be provided when the lesson is generated.

### Tasks

#### Task 1: Task 1

**NOTE: If the CodeSandbox file gets updated, the code example below may not be up to date.  You can confirm the most recent version of this assignment by clicking this:**
[Link to CodeSandbox Assignment](https://codesandbox.io/p/sandbox/lesson-2-javascript-loops-and-arrays-2025-wzp3tj?file=%2Fsrc%2Findex.mjs)

``` javascript
//--------------- IMPORTANT!!! ---------------

// Use the keyboard shortcut Alt + Z (for PC) or Option + Z (for Mac) to allow word wrap on this document.  Word wrap breaks the lines so you don't have to keep scrolling left and right to read.

//READ THE INFORMATION IN THE BROWSER WINDOW PANEL ON THE RIGHT BEFORE BEGINNING YOUR ASSIGNMENT!!

//---------- OVERVIEW AND INSTRUCTIONS ----------

//----------------------------------
// LESSON 2 LOOPS AND ARRAYS
//----------------------------------

//# JavaScript Loops and Arrays
// This is the coding assigment for the second week of the Intro to Programming course from Code the Dream. The concepts touched on in this assignment include:
//   - Simplify Repetitive Tasks with Loops
//   - Working with ‘for’ Loops
//   - Understanding Arrays

// In this assignment you will write your own code. Your instructions are listed as "comments", meaning the instructions are grayed out and start with '//' at the beginning of the line of code. Put your answers immediately below the instructions for each question. As mentioned in the Welcome to week 2 information to the right, you'll need to use console logs for all the questions to check your code output. Using a function in a console.log is very similar to how you were using them with variables last week. To invoke/call the function use the syntax:

//  console.log("Q#: ", functionName(anyInput))

// Please be sure to check the output of your called functions and console logs in the Console tab to the bottom right of this screen. If your Console is not showing, click the Inspect Button in the top right (see the Welcome to week 2 information to the right if you need help finding that)  Check to make sure that the output you get in your Console is the expected output.

// ---------- QUESTION 1 ----------
// Write a function called 'repeat' that takes 1 integer parameter and, using a for or while loop, prints out the string "Hello World!" to the console the same number of times as the parameter. NOTE: for this question, since your console log should be inside your function, you only need to call/invoke the function after you write it rather than call/invoke it inside of a console.log.

// EXAMPLE "LOG":
//    repeat(3);
// EXAMPLE OUTPUT:
//    Hello World!
//    Hello World!
//    Hello World!

// PUT YOUR CODE HERE

// ---------- QUESTION 2 ----------
// Write a function called 'pyramidCounting' that takes 1 integer parameter and returns the sum of all of the numbers between 0 and the parameter.

// EXAMPLE LOG:
//    console.log("Q2: ", pyramidCounting(4));
// EXAMPLE OUTPUT:
//    Q2: 10
// The mathematical explanation of this is 0+1+2+3+4 = 10.

//PUT YOUR CODE HERE

// ---------- QUESTION 3 ----------
// Write a function called 'noVowels' that take a string parameter and removes vowels from that string using a loop.

// EXAMPLE LOG:
//    console.log("Q3: ", noVowels(adventurous));
// EXAMPLE OUTPUT:
//    Q3: dvntrs

// PUT YOUR CODE HERE

// ---------- QUESTION 4 ----------
// Write a function called 'vowelCount' that takes 1 string parameter and returns the number of vowels in that string.

// EXAMPLE LOG:
//    console.log("Q4: ", vowelCount('I love to code.'));
// EXAMPLE OUTPUT:
//    Q4: 6

// PUT YOUR CODE HERE

// ---------- QUESTION 5 ----------
// Write a function called 'numOfOdds' that takes 1 integer parameter and returns the number of odd numbers between 0 and that number, including the number if it's odd. (Hint: Use the modulo operator)

// EXAMPLE LOG:
//    console.log("Q5: ", numOfOdds(15));
// EXAMPLE OUTPUT:
//    Q5: 8

// PUT YOUR CODE HERE

// ---------- QUESTION 6 ----------
// Create two variables named 'empty' and 'full'.  Assign an empty array to the 'empty' variable and any array of strings or numbers to the 'full' variable.  Write a function called 'arrayChecker' that returns true if the array passed as a parameter is empty and false if not.  Check both the 'empty' and 'full' variables to make sure they are returning the expected values.

// EXAMPLE LOGS:
//    console.log("Q6 empty: ", arrayChecker(empty));
//    console.log("Q6 not empty: ", arrayChecker(full));
// EXAMPLE OUTPUTS:
//    Q6 empty: true
//    Q6 not empty: false

// PUT YOUR CODE HERE

// ---------- QUESTION 7 ----------
// Write a function called 'getElementAt' that takes an array parameter and an integer parameter.  The function should return the element in the array at the given number index or 'null' if it doesn't exist.  Use your 'full' variable from Question 6 to test.

// EXAMPLE LOGS:
//    console.log("Q7: ", getElementAt(full, 2));
//    console.log("Q7: ", getElementAt(full, 7));
// EXAMPLE OUTPUT: (if the array assigned to variable 'full' is ["dream", 19, "code", 24, 180])
//    Q7: code
//    Q7: null

// ---------- QUESTION 8 ----------
// Write a function called 'insertInArray' that takes an array parameter, makes a NEW array with the value '0' inserted at the second position in the NEW array.  The function should return the NEW array.  Use your 'full' variable from Question 6 to test.  NOTE: Assigning an array to a new variable does not make a copy, it's another reference to the same array.  To make a copy you can use the slice() method as in this example:
// let newArray = originalArray.slice()
// LEARNING MOMENT: Also console log the variable 'full' to compare the new array to the original.

// EXAMPLE LOG:
//    console.log("Q8: ", insertInArray(full));
//    console.log("original array: ", full);
// EXAMPLE OUTPUT: (if the array assigned to variable 'full' is ["dream", 19, "code", 24, 180])
//    Q8: ["dream", 0, 19, "code", 24, 180]
//    original array: ["dream", 19, "code", 24, 180]

// PUT YOUR CODE HERE

// ---------- QUESTION 9 ----------
// Write a function called 'compareArrays' that takes two Array parameters (containing numbers or strings only) and returns true if they are equal, false if not.  The purpose of this function should be to look at each element of the two arrays and compare them, returning false when they either hit two items that don't match, or returning false if the two arrays themselves are different lengths. You can test this with the 'empty' and 'full' variables from Question 6, and/or you can create a variable called 'compare' and assign it an array identical to 'full' to compare those.  To further test your function's accuracy, create a new variable called 'part' that is a partial copy of the 'full' variable and test that as well.

// REMEMBER: In JavaScript, 1 === '1' is false, but 1 == '1' is true. You'll need to use the triple equals operator which is more strict because it compares data type.

// EXAMPLE LOG:
//    console.log("Q9 same: ", compareArrays(full, compare));
// EXAMPLE OUTPUT: (if both arrays assigned to variable 'full' and 'compare' are ["dream", 19, "code", 24])
//    Q9 same: true

// EXAMPLE LOG:
//    console.log("Q9 different: ", compareArrays(full, empty));
// EXAMPLE OUTPUT: (if using variables from Question 6)
//    Q9 different: false

// EXAMPLE LOG:
//    console.log("Q9 partial: ", compareArrays(full, part));
// EXAMPLE OUTPUT: (if 'full' variable is ["dream", 19, "code", 24] and if 'part' variable is ["dream", 19, "code"])
//    Q9 different: false

// PUT YOUR CODE HERE

// ---------- QUESTION 10 ----------
// Create a variable called 'numbers' and assign it an array with at least 3 numbers as elements (example: [10, 3, 4]).  Write a function called 'calculateTotal' that takes one array parameter and loops through the array in order to return the sum of all the array elements.

// STRETCH GOAL: write another version of calculateTotal (call it calculateTotal2) using the 'reduce()' method

// EXAMPLE LOG:
//    console.log("Q10: ", calculateTotal(numbers));
// EXAMPLE OUTPUT: (if the array assigned to variable 'numbers' is [3, 4, 2 ,8])
//    Q10: 17

// PUT YOUR CODE HERE

// ---------- QUESTION 11 ----------
// Write two functions called 'findEvens' and 'findOdds' that each take one array parameter and each returns a NEW Array of all the even or odd numbers as indicated.  NOTE: Assigning an array to a new variable does not make a copy, it's another reference to the same array.  To make a copy you can use the slice() method as in this example:
// let newArray = originalArray.slice()
// STRETCH GOAL: write another version of findEvens or findOdds using the `filter()` method

// EXAMPLE LOG:
//    console.log("Q11 evens: ", findEvens([10,2,3,19,7,6,93]));
//    console.log("Q11 odds: ", findOdds([10,2,3,19,7,6,93]));
// EXAMPLE OUTPUT:
//    Q11 evens: [10,2,6]
//    Q11 odds: [3,19,7,93]

// PUT YOUR CODE HERE

// ---------- QUESTION 12 ----------
// Write a function called 'makeSquares' that takes one array parameter and returns a NEW Array with the squared values of each of the numbers.  NOTE: Assigning an array to a new variable does not make a copy, it's another reference to the same array.  To make a copy you can use the slice() method as in this example:
// let newArray = originalArray.slice()
// STRETCH GOAL: write another version makeSquares using the `map()` method

// EXAMPLE LOG:
//    console.log("Q12: ", makeSquares([2,5,8]));
// EXAMPLE OUTPUT:
//    Q12: [4,25,64]

// PUT YOUR CODE HERE

// ---------- QUESTION 13 ----------
// Back in the old days, the early 2000s, this was a famous technical interview question. Write a function definition that takes NO parameters. The function will loop from 1 to 15 and return an array of numbers. While looping, the function will check if the current value in the loop is divisible by 3, by 5, or by both. If the current value in the loop is divisible by 3, the function will add the string "fizz" to an array. If the current value in the loop is divisible by 5, the function will add the string "buzz" to the array. If the current value in the loop is divisible by both, the function will add the value "fizzbuzz" to the array. If the number isn't divisible by 3, 5, OR both, it will add the number to the array.  The function will return the array of values.

// EXAMPLE LOG:
//    console.log("BONUS: ", fizzBuzz();
// EXAMPLE OUTPUT:
//    BONUS: [1,2,'fizz',4,'buzz','fizz',7,8,'fizz','buzz',11,'fizz',13,14,'fizzbuzz']

// PUT YOUR CODE HERE

```


```

```

### Submission Instructions

Please submit on time

### Checklist

Checklist will be provided when the lesson is generated.

### Check for Understanding

Understanding checks will be provided when the lesson is generated.

## Subsections

### Loops

You can either use the written Odin Project lessons or the video lessons in Scrimba.

- [V2 Scrimba - JS Deep Dive - Arrays](https://v2.scrimba.com/javascript-deep-dive-c0a/~01h)
- **NOTE: Watch only the first four videos in this playlist ( (1) Module Intro: Arrays, (2) Build Flexible Collections with Arrays, (3) Challenge: Your First Array, and (4) Check Element Existence in Arrays ). The rest of the topics we will cover in Week 5.**
  - **If you are getting an alert saying "Only available to subscribers" when trying to access the JS Deep Dive - Arrays content, you will need to be sure your are logged in to Scrimba with the email address we have on file for you, and that you have redeemed the link to free access you were emailed**

The following material is an excerpt from The Odin Project – Fundamentals Part 4.  That section also covers Array Methods and Test Driven Development which will be covered later in this class. For convenience we've copied the Loop, Array, and Knowledge Check information from the Fundamentals Part 4 section below.

Remember to please go to each link in this list and read through the content on that page. If there are links you are redirected to as you read/work through the content, follow those links as well and read the content there too.

# **Loops**

Computers don’t get tired, and they’re really, *really* fast! For that reason, they are well suited to solving problems that involve doing calculations multiple times. In some cases, a computer will be able to repeat a task *thousands* or even *millions* of times in just a few short seconds where it might take a human many hours. (Obviously, speed here depends on the complexity of the calculation and the speed of the computer itself). One way to make a computer do a repetitive task is using a **loop**.

1. Read this [MDN article](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code). It’s a longer one, but make sure you tackle the ‘Active Learning’ sections at the bottom of the page.
2. Once again, same info, slightly different context from [JavaScript.info](http://javascript.info/while-for). (Skim the info if you think you know it all, but **don’t forget the tasks at the end of the page**. You learn best by *doing*.)

# **Arrays**

Strings and numbers may be our building blocks, but as your scripts get more complex, you’re going to need a way to deal with large quantities of them. Luckily, JavaScript has a couple of data types that are used for just that. An Array is simply an ordered collection of items (Strings, numbers, or other things).

1. [This tutorial](https://www.w3schools.com/js/js_arrays.asp) is a great introduction.
2. [This article](https://www.w3schools.com/js/js_array_methods.asp) covers some of the most useful built-in array methods. These fundamentals are something you’ll use every day, so don’t rush too much and miss out!
3. [Web Dev Simplified video](https://www.youtube.com/watch?v=7W4pQQ20nJg) explains an overview of arrays in JavaScript in about 6 minutes.

## **Knowledge Check**

This section contains questions for you to check your understanding of the lessons from this week and last week on your own. If you’re having trouble answering a question, click it and review the material it links to.

- [What is an array?](https://www.w3schools.com/js/js_arrays.asp)
- [What are arrays useful for?](https://www.w3schools.com/js/js_arrays.asp)
- [How do you access an array element?](https://www.w3schools.com/js/js_arrays.asp)
- [How do you change an array element?](https://www.w3schools.com/js/js_arrays.asp)
- [What are some useful array properties?](https://www.w3schools.com/js/js_arrays.asp)
- [What are some useful array methods?](https://www.w3schools.com/js/js_array_methods.asp)
- [What are loops useful for?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code#why_bother)
- [What is the break statement?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code#exiting_loops_with_break)
- [What is the continue statement?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code#skipping_iterations_with_continue)



**Video URL:** No video available

**Code Examples:**

No code examples available

**External Links:**

No external links available

**Quizzes:**

No quizzes available

## Supplemental Videos

No supplemental videos available

## References

No references available

## Podcast URL

No podcast available