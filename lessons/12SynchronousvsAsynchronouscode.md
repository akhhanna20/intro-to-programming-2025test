# # Synchronous vs. Asynchronous code

## Overview

No overview provided

## Learning Objectives

Learning objectives will be defined as the lesson progresses.

## Topics Covered

Topics will be covered as the lesson progresses.

## Status

pending

## Assignment

Assignment for Lesson 12

### Objective

No objective specified

### Expected Capabilities

Expected capabilities will be defined as the lesson progresses.

### Instructions

Instructions will be provided when the lesson is generated.

### Tasks

#### Task 1: Task 1

You were learning about asynchronous programming and promises this week. In our coding assignment though, we'll be building on our HTML and JavaScript skills by creating a form on our HTML page and use the JavaScript file to collect the information from the form and write it back to the HTML document.

### Get organized and write some code!
- [ ] In your GitHub repository, if you have not yet merged your pull request from last week, merge your open lesson-11 pull request by going to the "Pull Requests" tab of your repository. Click on your open pull request, then click on the green 'Merge Pull Request" and confirm the merge. This will update your main branch with the work you did on your lesson-11 branch.
- [ ] Open your code editor and, in the terminal, make sure you're on your main branch. If you're still on your lesson-11 branch, you can switch to your main branch by using the git command `git checkout main`.
- [ ] Update your local main branch to include your lesson-11 work by pulling your changes from your GitHub repository main. Use the following git command in your terminal to do this: `git pull origin main`
- [ ] Still in your terminal, create a new local branch to keep track of just the work you'll do for this assignment by running `git checkout -b lesson-12` in the terminal. Doing this also copies the lesson-11 work you merged to main and pulled to your local machine so now all your branches should be identical on your local machine.

### Assignment: Task List / Deliverables

#### Create a Message Form
- [ ] Open your `index.html` file
- [ ] Above the `<footer>` element, add an empty `<section>` element
- [ ] Inside the new `<section>` element, create a level-two heading that says "Leave a Message"
- [ ] After the heading, create an HTML `<form>` element with a `name` attribute that equals "leave_message"
- [ ] Inside the `<form>` element, add the following:
  1. `<input>` element with attributes: `type` "text", `name` "usersName", and `required` true
  2. `<input>` element with attributes: `type` "email", `name` "usersEmail", and `required` true
  3. `<textarea>` element with attributes: `name` "usersMessage" and `required` true
  4. `<button>` element that says "Submit" and has `type` attribute equal to "submit"
  5. Each form field should also have a corresponding `<label>` element
  6. (Optional) Use `<br>` elements to stack the form fields
- [ ] Save and refresh your browser _(or just check your browser for changes if using live extension)_
- [ ] Add navigation to the message form:
  - [ ] Add a link in your `<nav>` section that takes the user to the 'Leave a Message' section when clicked

#### Add Message List Section
- [ ] After the `<section>` element from the previous step, create a new `<section>` element with an `id` of "messages"
- [ ] Inside that element, create a level-two heading that says "Messages"
- [ ] After the heading, add an empty unordered list (`<ul>`) element
- [ ] Save and refresh your browser _(or just check your browser for changes if using live extension)_

#### Handle Message Form Submit
- [ ] Open your `index.js` file and start at the bottom
- [ ] Create a variable named `messageForm` that uses "DOM Selection" to select the "leave_message" form by `name` attribute
- [ ] Add an event listener to the `messageForm` element that handles the "submit" event
  - hint: `addEventListener` method
- [ ] Inside the callback function for your event listener, create three new variables (one for each of the three form fields) and retrieve the value from the event
  - hint: `event.target` is the form, `event.target.usersName` is the first input element
- [ ] Inside the callback function for your event listener, add a `console.log` statement to log the three variables you created in the previous step
- [ ] Save and refresh your browser _(or just check your browser for changes if using live extension)_
- [ ] Open the console in your browser if you haven't already by either right clicking on your page and select "Inspect" or by using the menu bar to open the Developer tools. 
 - [ ] Fill out the HTML form in your browser and hit "Submit"

> Note: at this point, you should notice that the browser is refreshing automatically when you submit your form which is **_not_** the desired behavior

- [ ] Inside the callback function, above the other code you just wrote, add a new line to prevent the default refreshing behavior of the "submit" event
  - hint: `preventDefault` method
- [ ] Save and refresh your browser _(or just check your browser for changes if using live extension)_
- [ ] Fill out the HTML form in your browser and hit "Submit"
  - You should see that the page **does not** refresh and your values are logged in the console

> Note: at this point, you should notice that the form is submitting properly but the form fields are not reset after submit

- [ ] Inside the callback function, on the very last line, add a new line of code to clear the form
  - hint: `reset` method
- [ ] Save and refresh your browser _(or just check your browser for changes if using live extension)_

#### Display Messages in List
- [ ] In the `index.js` file, start inside the event listener callback function on the line **above** where you reset the form
- [ ] Create a variable named `messageSection` and use "DOM Selection" to select the #messages section by `id`
- [ ] Create a variable named `messageList` and use "DOM Selection" to query the `messageSection` (instead of the entire `document`) to find the `<ul>` element
- [ ] Create a variable named `newMessage` that makes a new list item (`li`) element
- [ ] On the next line, set the inner HTML of your `newMessage` element with the following information:
  - `<a>` element that displays the "usersName" and is a clickable link to the "usersEmail" (hint: use the `mailto:` prefix)
  - `<span>` element that displays the "usersMessage"
- [ ] Create a variable named `removeButton` that makes a new `<button>` element
  - Set the inner text to "remove"
  - Set the `type` attribute to "button"
  - Add an event listener to the `removeButton` element that handles the "click" event
    - Inside the callback function, create a variable named `entry` that finds the button's parent element using DOM Traversal (hint: `parentNode` property)
    - Remove the `entry` element from the DOM (hint: `remove` method)
- [ ] Append the `removeButton` to the `newMessage` element
  - hint: `appendChild` method
- [ ] Append the `newMessage` to the `messageList` element
- [ ] Save and refresh your browser _(or just check your browser for changes if using live extension)_

#### Style your Message Form
 - [ ] Open your `index.css` file
 - [ ] Style your message form fields and buttons keeping in mind:
   - [ ] adequate specing so form fields aren't crowded
   - [ ] appropriate sizing in media queries so a user on a mobile device can easily touch/tap into the fields to type
   - [ ] button sizing to accomodate click and touch/tap interactions

#### Stretch Goals
These tasks are **entirely optional**, but if you'd like a challenge then do your best to complete each item.
- [ ] (Optional) Hide the #messages section, including the Messages header, when the list is empty
- [ ] (Optional) Create an "edit" button for each message entry that allows the user to input a new/modified message

**_By the end of this assignment, you should have a form in your HTML document with name, email, message fields and a submit button as well as a messages section.  The code you wrote in your index.js should handle the inputs the user enters into the form and display that information as a name you can click on to email the user and their message with a remove button to remove their message entirely.  You should have styling in your index.css file for your message form fields and/or section.  If you attempted stretch goals, you should also have a hidden Messages section unless there is a message and/or each message should have an edit button._**

### Backup to the cloud
Once you've made the above changes to your html file, follow the below instructions to push a copy from your local machine like you did at the end of last assignment. Make sure your code gets copied to GitHub by adding changes to staging, committing the staged changes, and pushing them from your local machine to GitHub:

- [ ] Check the status of the changes you just made (code changes to the index.html and index.js files) by running git status in your terminal
- [ ] Stage all your changes for commit by running `git add .` in your terminal
- [ ] Run `git status` again to see how things have changed. You should get a response indicating changes staged for commit.
- [ ] Create a commit message for reference. You can use a different message if you wish. Run `git commit -m "form and functionality added"`
- [ ] Push these changes to your GitHub repository from your local computer by running `git push`

### Submit Assignment
Now let's make sure that lesson branch will be reviewed.

- [ ] Go to your GitHub repository page in your web browser now, and you should see a "lesson-12 has a recent push" notice with a green "Compare & pull request" button. Click that button
- [ ] Feel free to put notes to yourself or notes for your reviewer in the description (be sure you're including any questions to your reviewer in your assignment submission form though!) and click the green "Create pull request" button.
- [ ] Copy the address of your pull request page (should look like https://github.com/yourUsername/name-classname/pull/7) and paste it into your assignment submission form.

### What next?
- If you're on track with class, wait to get feedback and/or the email notice that your assignment review is complete before confirming and merging your pull request to the main branch.
- If you're behind or are working ahead:
  - if you're confident your work is accurate, merge your pull request and continue working through class.
  - if you're not sure about your work this week, schedule a 1:1 session with a mentor and review your work together before merging.


```

```

### Submission Instructions

Please submit on time

### Checklist

Checklist will be provided when the lesson is generated.

### Check for Understanding

Understanding checks will be provided when the lesson is generated.

## Subsections

### # Synchronous vs. Asynchronous code

Go through **both** resources (Odin **and** Scrimba) for this topic as they will help you gain a more clear understanding of this topic.

Remember to please go to each link in this list and read through the content on that page. If there are links you are redirected to as you read/work through the content, follow those links as well and read the content there too.

- **[The Odin Project – Asynchronous Code](https://www.theodinproject.com/lessons/node-path-javascript-asynchronous-code)**
- **[Scrimba - JavaScript Deep Dive - Async JS - Fix Callback Hell with Promises](https://v2.scrimba.com/javascript-deep-dive-c0a/~02o)**
- **[Scrimba - Introduction to ES6+ - Promises](https://v2.scrimba.com/introduction-to-es6-c0t/~0q)**
- **[Scrimba - Introduction to ES6+ - Challenge: Promises](https://v2.scrimba.com/introduction-to-es6-c0t/~0r)**

## Synchronous vs. Asynchronous code

*Synchronous code* executes one code instruction at a time, in the order that the instructions are given. *Asynchronous code* executes multiple instructions simultaneously, and the order in which the instructions are completed isn't known. 

With asynchronous code, multiple tasks can be executed at the same time while tasks in the background finish. This is what we call *non-blocking* code. The execution of other code won't stop while an asynchronous task finishes its work.

```jsx
let greet_one = "Hello"
let greet_two = "World!!!"
console.log(greet_one)
setTimeout(function(){
    console.log("Asynchronous");
}, 10000)
console.log(greet_two);
```

In the above example, if you run the code on your machine you will see `greet_one` and `greet_two` logged even if there is code in between those 2 logs.

Now, setTimeout is asynchronous so it runs in the background, allowing code after it to execute while it runs. After 10 seconds, `Asynchronous` will print because we set a time of 10 seconds in setTimeout to execute it after 10 seconds.

1. Read this article about [synchronous and asynchronous](https://www.telerik.com/blogs/how-javascript-code-gets-executed-synchronous-asynchronous)

[Watch this video on Async vs Sync](https://www.youtube.com/watch?v=wYRw8f-wrco&t=253s)

## Promises

When it comes to handling asynchronous code, the go-to tool is something called a **promise**. This nifty object can handle async tasks and gives you a bunch of methods to neatly pluck out a single result.

Here's the deal: Asynchronous code can be a bit of a puzzle because it messes with the usual order of things. It can get pretty tricky in some situations.

But that's where promises come to the rescue! They're like a protective wrapper around async code. Promises are smart – they won't trigger the callback function until it's absolutely necessary. Plus, they hand you some nifty functions to deal with whatever outcome your async code delivers, whether it's a triumphant success or a less-than-ideal failure.

```jsx
const newPromise = new Promise((resolve, reject) => {
  // Your code here...
});
```

A new promise can be created using the **new** keyword with the [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/Promise) class. This will create an instance of a promise. Promises can be assigned to variables. The only argument to pass into the Promise constructor is a callback function that has two parameters: **resolve** and **reject.**

To manage asynchronous code, promises have **three states:**

- **Pending:** When a promise is first created, it has a status of *pending*.
- **Fulfilled:** When the promise has successfully finished running, it has a status of *fulfilled*. This means that it is ready to pass back a value.
- **Rejected:** If something goes wrong, the promise changes to a status of *rejected*. This means that something failed.

### Resolving Promises

Now that you've got the hang of creating promises, you might have noticed something missing – a way to snoop on a promise's mood, like whether it's feeling "pending," "fulfilled," or "rejected." There's also no direct way to peek at what the promise has decided to resolve to or why it's throwing a fit.

Unlike your typical JavaScript objects, promises are like chameleons. They can switch between their states (and values) from pending to fulfilled or rejected whenever they please. This means you've got to keep an eye on them.

So, here's the deal: Promises rely on callback functions to raise a flag when their state changes. 

When the promise is all smiles and gets resolved, it'll call the callback function hanging out in the **`then()`** method and share its resolved value. But if it's having a bad day and gets rejected, the **`catch()`** method swoops in, bringing along the rejected reason (aka, the error). 

It's like a promise's way of saying, "Hey, something happened, and here's what went down!"

### The then() method

When a promise is created, the asynchronous operation inside will be fulfilled as quickly as possible. However, there are no methods or properties available to directly access the resolved value of a promise.

The then() method accepts a callback function that is called whenever the promise is fulfilled. 

```jsx
// Creating a Promise
const myPromise = new Promise((resolve, reject) => {
  // Simulating an asynchronous task 
  setTimeout(() => {
    const data = "Here's the result!";
    resolve(data); // Resolving the promise with some data
  }, 2000); // Simulating a 2-second delay
});

// Using the Promise
myPromise.then((result) => {
  console.log("Promise resolved with data:", result);
}).catch((error) => {
  console.error("Something went wrong:", error);
});
```

1. We create a **`myPromise`** object using the **`Promise`** constructor. Inside the promise, we simulate an asynchronous task using **`setTimeout`**. After 2 seconds, the promise is resolved with the message "Here's the result!"
2. We use the **`then`** method to handle the resolution of the promise. When the promise is resolved, the provided callback function is executed, and it logs the resolved data.
3. If an error were to occur inside the promise (e.g., if we used **`reject`** instead of **`resolve`**), the **`catch`** method would handle the error and log it.

### **The catch() method**

The **`catch()`** method in JavaScript is like the safety net for promises. Just like how try/catch blocks work, if the **`catch()`** method doesn't throw an error itself, the function calling it won't know that something went wrong. In simple terms, the promise attached to **`catch()`** only becomes rejected if **`catch()`** encounters an error or returns a promise that also gets rejected. Otherwise, it resolves as if everything went smoothly.

![promise catch flow](https://raw.githubusercontent.com/Code-the-Dream-School/intro-to-programming-2024/41a41459613b5c8e6cc3f9171feebfc1837b0c8e/Screenshot%25202023-09-24%2520at%252010.19.29%2520PM.png)

1. Read [this article about Promises](https://javascript.info/promise-basics)
2. Read [this second article about Promises](https://dmitripavlutin.com/what-is-javascript-promise/)

Watch these two short videos on JavaScript Promises:

1. [JS Promise in 100 Seconds](https://www.youtube.com/watch?v=RvYYCGs45L4)
2. [Async JS: Promises](https://www.youtube.com/watch?v=slIJj-zbs_M)


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