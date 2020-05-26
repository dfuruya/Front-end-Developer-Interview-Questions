# Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Testing Questions](#testing-questions)
  1. [Performance Questions](#performance-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?
* What excites or interests you about coding?
  As cliche as this sounds, I love taking on technical challenges, and the joy I experience when I solve it. My father is an engineer himself (mechanical engineer), who is now a professor at Harvey Mudd College. As a young child, I was always fascinated by how he would show me interesting science demonstrations, such as putting a toy boat in the bathtub, and just adding liquid bodywash into the tub to propel the boat. It was these sorts of gems that he exposed me to that spurs the curiosity in me over how things work in this world. 
  
* What is a recent technical challenge you experienced and how did you solve it?
  Yesterday, I was working on a UI codebase built in React and Redux. In terms of data/state management, there is a mix of Redux as well as passing state through props. 
  With a traditional React app (no Redux, no context API) using props to pass data/state, there are obvious flaws. One common flaw is where you have a deeply nested chain of components, and one of the descendent components "clips" certain props (through filtering props received from its parent, or changing the data and passing it with the same props name, etc), which can occur in multiple components down the chain. As a result, a descendant component may have received "altered" data or even data that is "assumed" to be the same as what started from the root parent. Furthermore, if a new component were introduced as a child component along that chain, and requires that props data that was omitted, then we are either forced to either attach that prop for every component down the chain from where it was omitted, or store/retrieve it via Redux. This adds more overhead to the components, and at some point, may be difficult to maintain bloated components. 
  On the other end of the spectrum, an app can be architected solely using Redux for any state mgmt, but that often is not the case for most applications, where there are many direct parent-child compositions that does not warrant wrapping both components with the Redux provider, as that adds more overhead via extra process of the parent component saving state to the store, then having that state being pulled down into the child component. 
  
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
  - UI: a11y (Accessibility): making sure that your site is following WCAG standards and is easily navigable using assistive technologies such as screen readers. This can be achieved within:
    - HTML markup using WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications) specifications
      - Dynamic & interactive elements (pop up alerts, etc)
      - Javascript
      - Non text elements (audio/video) should have text alternatives such as captions/transcripts
      - Images should have descriptive alt text d)
    - Focus management (focus traps, etc)
    - Color contrasts
  - Security: proper authentication and authorization system in place
    - Auto time out of sessions (within a reasonable time frame)
    - Conceal password field entry
    - Encrypt passwords (never send via plain text)
    - MFA (Multi-Factor Authentication)
  - Security: guard against XSS
    - Sanitize input fields
  - Performance: think about scalability in terms of components and data
    - Use appropriate data structures (objects vs arrays, etc)
    - Minimizing cloning/copying of data
    - Lazy loading of (UI) components
    - Caching
    - Critical CSS (consider only above-the-fold elements)
    - 
  - 
* Talk about your preferred development environment.
* Which version control systems are you familiar with?
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* How would you optimize a website's assets/resources?
* How many resources will a browser download from a given domain at a time?
  * What are the exceptions?
* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?

#### HTML Questions:

* What does a `doctype` do?
* What's the difference between full standards mode, almost standards mode and quirks mode?
* What's the difference between HTML and XHTML?
* Are there any problems with serving pages as `application/xhtml+xml`?
* How do you serve a page with content in multiple languages?
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
* What is progressive rendering?
* Have you used different HTML templating languages before?

#### CSS Questions:

* What is the difference between classes and IDs in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
* Describe z-index and how stacking context is formed.
* Describe BFC(Block Formatting Context) and how it works.
* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
* What are your favourite image replacement techniques and which do you use when?
* How would you approach fixing browser-specific styling issues?
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Are you familiar with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Describe pseudo-elements and discuss what they are used for.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

#### JS Questions:

* Explain event delegation
  - Event delegation is a pattern that is used to take advantage of the concept of "bubbling". When an event occurs somewhere on the DOM (`onclick`, etc), that even will "bubble" up from the target child node, up through its ancestors in the DOM tree. If we have multiple siblings or children, instead of attaching an event handler for each node, we can "delegate" dealing with that event by attaching a single event handler to that common parent ancestor node, and checking the `event.target` to see which node that event originated from.
* Explain how `this` works in JavaScript
  - The `this` keyword refers to the lexical execution context (global, function, or eval) at call time.
  - A property of an execution context (global, function or eval) that, in non–strict mode, is always a reference to an object and in strict mode can be any value.
* Explain how prototypal inheritance works
  - In JS, every object has a pointer to either a parent object (or `null`), where it inherits its properties and methods. (For more detail, [see this gist](https://gist.github.com/dfuruya/6e5a1031316c70596f3cfe254cab7b8f))
* What is an IIFE? What is it used for?
  - IIFE stands for Immediately Invoked Function Expression. Before `let` and `const`, because `var` has no block-level scope, IIFE was invented as a way to emulate private variables. By placing parenthesis around an anonymous function declaration, we are effectively creating a momentary scope that vanishes once it is invoked. 
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  - Function `foo` is a function declaration. 
  * What needs to be changed to properly make it an IIFE?
    - Make the function anonymous and wrap the declaration (or the entire expression) in parenthesis: `(function(){ })();` or `(function(){ }());`
* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  - `null`: intentional absence of a value
  - `undefined`: variable has been declared, but has not been initialized/assigned a value
  - undeclared: a variable has not been declared, and will throw an error if that non-existant variable is referenced/evaluated
  * How would you go about checking for any of these states?
  - `null`: `var === null`
  - `undefined`: `typeof var === 'undefined'`
  - undeclared: use a `try..catch` block and check if variable has been declared
* What is 'Strict Mode', and how would you use it?
  - It is a way to opt in to a restricted variant of JS (or conversely opting out of writing "sloppy" JS). It changes JS semantics to entire scripts or to individual functions in the following ways:
    - forcing some silent errors to be thrown
    - fixes code mistakes that make it difficult for JS engines to perform optimizations
    - prohibits some syntax likely to be defined in future versions of ES
* Name the types of scopes in JS and describe them.
  - Global: if a variable is declared outside all functions or curlies (`{}`), it is defined in the global scope. It is good practice to avoid global variables, as there is a potential risk of naming collisions.
  - Local: there are two kinds of local scopes: 1) function and 2) block scope. 
    - For more info on these scopes, [see this gist](https://gist.github.com/dfuruya/7c001a6c247bca1bcbae654746e3a62a)
* What is the difference between declaring variables using `var`, `let` and `const`?
  - [see this gist](https://gist.github.com/dfuruya/7c001a6c247bca1bcbae654746e3a62a)
* What is a closure, and how/why would you use one?
  - A closure is the lexical scope in which an outer function has access to an inner function's variables even after it has returned control. For more info, [see this gist](https://gist.github.com/dfuruya/7c001a6c247bca1bcbae654746e3a62a)
* What's a typical use case for anonymous functions?
  - Since anonymous functions can't be accessed after its initial declaration, it is normally used as an argument to other functions, or as a closure (IIFE, etc)
* Describe the `new` keyword.
  - The `new` keyword creates an instance of a user-defined object or `class` functions. For more info, [see this gist](https://gist.github.com/dfuruya/b86ff0fd70fe0722ec18d325201d7e85)
* What's the difference between `.call` and `.apply`?
  - `.call`: takes `this` as the first argument, and a **C**omma-separated list of arguments after that
  - `.apply`: takes `this` as the first argument, and arguments as an **A**rray after it
* Explain `Function.prototype.bind`.
  - The `.bind` method creates a new function that, when called, has its `this` keyword set to the the provided value, along with a comma-separated list of arguments as the arguments passed to the function at call time. 
* When would you use `document.write()`?
  - Since `document.write` will clear a document's content, and parse the stringified argument that is passed in, there is a potential performance hit. In this case, using DOM manipulation would be better suited. A reasonable use case for `document.write` is conditionally loading a local, cached version of a 3rd party script in case a CDN is unavailable:
  ```html
  <!-- Grab Google CDN's jQuery, with a protocol relative URL; fall back to local if offline -->
  <script src="//ajax.googleapis.com/ajax/libs/jquery/1.6.3/jquery.min.js"></script>
  <script>window.jQuery || document.write('<script src="js/libs/jquery-1.6.3.min.js"><\/script>')</script>
  ```
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain Ajax in as much detail as possible.
* What are the advantages and disadvantages of using Ajax?
* Explain how JSONP works (and how it's not really Ajax).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* Difference between document load event and document DOMContentLoaded event?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is `"use strict";`? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

#### Testing Questions:

* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?

#### Performance Questions:

* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
* What are the differences between Long-Polling, Websockets and Server-Sent Events?
* Explain the following request and response headers:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
* What are HTTP methods? List all HTTP methods that you know, and explain them.

#### Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

#### Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Who inspires you in the front-end community?
* Do you have any pet projects? What kind?
* What's your favorite feature of Internet Explorer?
* How do you like your coffee?


#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).
