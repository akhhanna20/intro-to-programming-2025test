# ## The fetch API

## Overview

No overview provided

## Learning Objectives

Learning objectives will be defined as the lesson progresses.

## Topics Covered

Topics will be covered as the lesson progresses.

## Status

pending

## Assignment

Assignment for Lesson 13

### Objective

No objective specified

### Expected Capabilities

Expected capabilities will be defined as the lesson progresses.

### Instructions

Instructions will be provided when the lesson is generated.

### Tasks

#### Task 1: Task 1

This week you'll have two parts to your coding assignment.  The first completes your work with your portfolio site by using API fetch to pull a list of all your GitHub repositories to your portfolio page.  The second part is an open API project to reinforce what you learn this week with fetch, and to give you another project for your portfolio.  

## Portfolio completion

<details>
<summary> Click here to expand your Portfolio completion assignment instructions </summary>
<br>
<h3>Get organized and write some code!</h3>
<ul>
<li>In your GitHub repository, if you have not yet merged your pull request from last week, merge your open lesson-12 pull request by going to the "Pull Requests" tab of your repository. Click on your open pull request, then click on the green 'Merge Pull Request" and confirm the merge. This will update your main branch with the work you did on your lesson-12 branch.</li>
<li>Open your code editor and, in the terminal, make sure you're on your main branch. If you're still on your lesson-12 branch, you can switch to your main branch by using the git command `git checkout main`.</li>
<li>Update your local main branch to include your lesson-12 work by pulling your changes from your GitHub repository main. Use the following git command in your terminal to do this: `git pull origin main`</li>
<li>Still in your terminal, create a new local branch to keep track of just the work you'll do for this assignment by running `git checkout -b lesson-13` in the terminal. Doing this also copies the lesson-12 work you merged to main and pulled to your local machine so now all your branches should be identical on your local machine.</li>
</ul>

### Assignment: Task List / Deliverables

#### Creating your fetch
- [ ] Open your `index.js` file, starting below the code from the previous lesson
- [ ] Using the Fetch API, create a "GET" request to `https://api.github.com/users/{GITHUB_USERNAME}/repos` where `{GITHUB_USERNAME}` is your username for your GitHub account
  - hint: the `fetch` function
  - hint: "GET" is the default method for `fetch`
- [ ] Chain a `then` method to your `fetch` call and pass it a function that returns the response JSON data

#### Handle your JSON data
- [ ] Chain another `then` method and pass it a callback function to parse the response and store it in a variable named `repositories`
  - hint: JSON.parse(this.response)
- [ ] Console.log the value of repositories to better see the data returned from your API fetch
- [ ] Save and refresh your browser _(or just check your browser for changes if using live extension)_
  - You should see the list of your GitHub repositories displayed in your console.

#### Handling errors
 - [ ] Chain a `catch()` function to your `fetch` call to handle errors from the server so the user would know what happened if your Projects section was empty.

#### Display Repositories in List
 - [ ] Create a variable names `projectSection`; using "DOM Selection" to select the projects section by id
 - [ ] Create a variable named `projectList`; using "DOM Selection" query the projectSection (instead of the entire document) to select the <ul> element
 - [ ] Create a for loop to iterate over your repositories Array, starting at index 0
   - [ ] Inside the loop, create a variable named `project` to make a new list item (li) element
     - hint: createElement method
   - [ ] On the next line, set the inner text of your project variable to the current Array element's name property
     - hint: access the Array element using bracket notation
   - [ ] On the next line, append the project element to the projectList element
     - hint: appendChild method
 - [ ] Save and refresh your browser _(or just check your browser for changes if using live extension)_
   - You should see your list of repositories beneath the "Projects" heading on your portfolio site
      
#### Style your Repository List
 - [ ] Open your `index.css` file
 - [ ] Add styling to your projects list, be sure to account for any changes you want in media queries
 - [ ] STRETCH GOAL: Use flexbox (or grid) to style your list of repositories

**_By the end of this assignment, you should have a working API fetch to your GitHub account and be able to see a list of your repository names in the Projects section of your portfolio.  Were there to be a server error during the API fetch, your site would return an error message.  Your project list should be styled using flexbos or grid._**
</details>

## Open API Project begins

<details>
<summary> Click here to expand your Open API Project assignment instructions </summary>
<br>
An "open source" means that the source code of something is freely available and can be redistributed and modified.  We have identified several options of open source APIs that allow you to use their data without paying for access to that data.  Use one of the following open source APIs to create a site that accesses a minimum of 2 data points. (Example: if using Open-Meteo, the weather API, you could display (1) the temperature and (2) the weather condition).  Take a look at the options below and decide which one(s) interest you the most.
**NOTE:** You have from now until the end of class to have your Open API Project meeting the requirements.  Think about what you want to build and how you want your site to look and then break the work into parts to pace yourself.

### Open Source API options:
 
* [Open-Meteo](https://open-meteo.com/) – a weather API
* [Swapi.Tech](https://www.swapi.tech/) – an API about Star Wars films
* [Marvel](https://developer.marvel.com/) – an API about the Marvel fandom
* [ARTIC](https://api.artic.edu/docs/#introduction) – an art API from the Art Institute of Chicago
* [TheDogAPI](https://thedogapi.com/) or the [TheCatAPI](https://thecatapi.com/) – APIs about (you guessed it!) Dogs or Cats
* [Soccer](https://api-sports.io/documentation/football/v3) - for all the Soccer lovers out there
* DEPRECATED, certificate expired - [SampleAPIs](https://sampleapis.com/api-list/coffee) – an API for coffee lovers

This week, just focus on accomplishing the following:
 - [ ] Familiarize yourself with the documentation of whichever API you decide to use
 - [ ] Create a new repository in GitHub specifically for your open API project and connect it to your local machine (you can look back at lesson 7 coding assignment instructions to refresh your memory if needed)

⚠️ **_NOTE:_** Be sure you are NOT in your portfolio folder when you clone your repository! Doing this will create a sub-repository which is a complicated problem to resolve. ⚠️ 

 - [ ] Create your basics (index.html, index.js, index.css) but don't go too in depth with any of them yet; just be sure your pages link correctly to each other
 - [ ] Repeat the portfolio part of the assignment above for this project to be sure that your fetch is working and that you're getting a response.  You don't need to display any of it yet, but you should at least be able to console.log the response so you can see what data you get back.  
 - [ ] Put a link to your Open API project repository in the readme.md file of your Portfolio project so your reviewer can easily find/look at your Open API project from your portfolio project.  You can add a link to your read me by using the following syntax:
`[My Open API Project](https://github.com/yourUsernameHere/yourname-open-api)` Put the words you want the link to be in hard brackets `[ ]` and the link to the repository in parentheses `( )` 

**_By the end of this assignment, you should have started on your Open API Project (create a repository, built your basics, and wrote the code for your API fetch to test what response you get back.  You should also see your Open API Project listed on your portfolio by the end of this part of the assignment._**
</details>

### Backup to the cloud
Once you've made the above changes to your index.js file, follow the below instructions to push a copy from your local machine like you did at the end of last assignment. You'll do this same process with your open API project to get any local work on that project backed up to your GitHub repository.  Make sure your code gets copied to GitHub by adding changes to staging, committing the staged changes, and pushing them from your local machine to GitHub:

- [ ] Check the status of the changes you just made (code changes to the index.js files) by running git status in your terminal
- [ ] Stage all your changes for commit by running `git add .` in your terminal
- [ ] Run `git status` again to see how things have changed. You should get a response indicating changes staged for commit.
- [ ] Create a commit message for reference. You can use a different message if you wish. Run `git commit -m "API fetch completed"`
- [ ] Push these changes to your GitHub repository from your local computer by running `git push`

### Submit Assignment
Now let's make sure that lesson branch will be reviewed.

- [ ] Go to your GitHub repository page in your web browser now, and you should see a "lesson-13 has a recent push" notice with a green "Compare & pull request" button. Click that button
- [ ] Feel free to put notes to yourself or notes for your reviewer in the description (be sure you're including any questions to your reviewer in your assignment submission form though!) and click the green "Create pull request" button.
- [ ] Copy the address of your pull request page (should look like https://github.com/yourUsername/name-classname/pull/8) and paste it into your assignment submission form.  **_NOTE: If you'd like your reviewer to check your open API project work in progress, submit the link in the "questions" field of your assignment submission form._**

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

### ## The fetch API

Go through **both** resources (Odin **and** Scrimba) for this topic as they will help you gain a more clear understanding of this topic.

Remember to please go to each link in this list and read through the content on that page. If there are links you are redirected to as you read/work through the content, follow those links as well and read the content there too.

- **[The Odin Project – JSON](https://www.theodinproject.com/lessons/node-path-javascript-json)**
- **[The Odin Project – Working with APIs](https://www.theodinproject.com/lessons/node-path-javascript-working-with-apis)**
- **[The Odin Project - Async and Await](https://www.theodinproject.com/lessons/node-path-javascript-async-and-await)**
- **[Scrimba - JS Deep Dive - Async JS - Make Network Requests with fetch()](https://v2.scrimba.com/javascript-deep-dive-c0a/~02p)**
- **[Scrimba - JS Deep Dive - Async JS - Challenge: Fetch API](https://v2.scrimba.com/javascript-deep-dive-c0a/~02q)**
- **[Scrimba - JS Deep Dive - Async JS - Promises with async-await](https://v2.scrimba.com/javascript-deep-dive-c0a/~02r)**
- **[Scrimba  - JS Deep Dive - Async JS - Catch Errors with async-await](https://v2.scrimba.com/javascript-deep-dive-c0a/~02s)**
- **[Scrimba - Introduction to ES6+ - Async & Await](https://v2.scrimba.com/introduction-to-es6-c0t/~0u)**

### The fetch API

At a high level, `fetch` is used to make HTTP requests on the browser. It uses `Promise`s to handle the asynchronous nature of HTTP requests and responses. `fetch` is used to formulate and send a request to a server and read the server response.

Since the `fetch` API is provided by almost all major browsers, you can use the `fetch` API by opening up the "Console" tab in Chrome or Firefox to use the built-in `fetch` function.

`fetch` is a function that can only be used in the browser's JavaScript runtime environment. Currently, it is not a built-in function on Node.js, the runtime environment you are using in VSCode.

```jsx
fetch('https://jsonplaceholder.typicode.com/posts/1')
  .then(response => {
    if (!response.ok) {
      throw new Error('Request failed');
    }
    return response.json(); // Parse the response as JSON
  })
  .then(data => {
    console.log(data); // Do something with the data
  })
  .catch(error => {
    console.error('An error occurred:', error);
  });
```

`fetch` has two parameters, url and options. The first parameter is required it defines the URL of the request that you want to send. If the URL is the only argument passed into the `fetch` function then a GET request will be made. 

The second parameter is optional it defines the other components of the request besides the URL:

- method - the method of the request (GET, POST, PUT, PATCH, DELETE)
- headers - an object whose key-value pairs are header names and values
- body - value should be a string of the body of the request

The `fetch` function returns a Promise that will be fulfilled when a response comes back from the server. The resolved value of the returned Promise is a [fetch Response object](https://developer.mozilla.org/en-US/docs/Web/API/Response) containing information about the response components.

Now watch these two videos on Fetch:

1. [Learn Fetch API in 6 minutes](https://www.youtube.com/watch?v=cuEtnrL9-H0&t=2s)
2. [GET data from API & display in HTML with JS](https://www.youtube.com/watch?v=zUcc4vW-jsI)

### The async and await keywords

The async keyword is applied to a function. On its own, the async keyword transforms the function so that when the function is invoked, the return value will be wrapped in a promise.

The async keyword works in tandem with the await keyword inside of your function body.

The await keyword allows you to treat asynchronous requests as if they were synchronous.

Using the await keyword before fetch() forces the execution of the code to pause until that asynchronous operation is finished. Once it is, you can then use the resolved response.

```jsx
async function fetchData() {
  try {
    const response = await fetch('https://jsonplaceholder.typicode.com/posts/1');
    
    if (!response.ok) {
      throw new Error('Request failed');
    }
    
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('An error occurred:', error);
  }
}

fetchData();
```

In this example, we define an **`async`** function called **`fetchData`**. Inside the function, we use the **`await`** keyword to make a GET request to the JSONPlaceholder API to fetch the post with an ID of 1. We also handle any potential errors using a **`try...catch`** block.

The response is first checked for its status using **`response.ok`**. If the response is successful, we use **`await response.json()`** to parse the JSON data. Finally, we log the data to the console.

Now watch these two videos on Async/Await:

1. [The Async Await Episode](https://www.youtube.com/watch?v=vn3tm0quoqE&t=413s)
2. [JS Async/Await Simply Explained](https://www.youtube.com/watch?v=wKY4-WMmbZw)


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