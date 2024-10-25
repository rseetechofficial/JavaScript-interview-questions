# JavaScript Interview Questions & Answers

   > Click :star: Please follow me on GitHub and LinkedIn [@RameshKumar](https://www.linkedin.com/in/ramesh-kumar-choudhary/) for more updates.


   ## JavaScript Coding Challenges and Interview Question list available here :-

   >1. Click here for [Javascript Basics Coding](https://github.com/rseetech/javascript-basics) more information.
   >  
   >2. Click here for [Javascript Coding Challenges](https://github.com/rseetech/javascript-coding-challenges) more information.
   >
   >3. Click here for [Javascript quick coding interview questions](https://github.com/rseetech/javascript-quick-coding-interview-questions) more information. 
   >
   >3. Click here for [Javascript interview asking output questions](https://github.com/rseetech/javascript-interview-asking-output-questions) more information. 


   ## React nterview Questions & Coding Project list available here :-

   >1. Click here for [React Interview Questions & Answers](https://github.com/rseetech/React-interview-questions) more information.
   >
   >2. Click here for [React Routing Axios Search Counter App Using MUI](https://github.com/rseetech/react-routing-axios-search-counter-app-using-mui) more information.
   >
   >3. Click here for [React Routing Pass data Child to Parent](https://github.com/rseetech/react-router-axios-pass-data-child-to-parent) more information.
   >
   >4. Click here for [React Create Tic Tac Toe Game](https://github.com/rseetech/react-create-tic-tac-toe-game) more information.


### Table of Contents

| No. | Questions                                                                              |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1  | [What is a promise ](#what-is-a-promise)      |
| 2  | [Why do you need a promise ](#why-do-you-need-a-promise)     |
| 3  | [What are the three states of promise ](#what-are-the-three-states-of-promise)       |
| 4  | [What is promise all ](#what-is-promise-all)     |
| 5  | [Event bubbling ](#event-bubbling)     |
| 6  | [How to Stop Event bubbling ](#how-to-stop-event-bubbling)     |
| 7  | [Event Capturing ](#event-capturing)     |

1. ### Differences between var, let, and const:

   | var                                                  | let                               |  const                    |
   | --------------------------------------------- | ----------------------------------- |----------------------------------|
   | The scope of a var variable is functional scope.           | The scope of a let variable is block scope.  | The scope of a const variable is block scope. |
   | It can be updated and re-declared into the scope.      | It can be updated but cannot be re-declared into the scope.  | It cannot be updated or re-declared into the scope. |
   | It can be declared without initialization.            | It can be declared without initialization.  | It cannot be declared without initialization. |
   | It can be accessed without initialization as its default value is “undefined”.| It cannot be accessed without initialization otherwise it will give ‘referenceError’.  | It cannot be accessed without initialization, as it cannot be declared without initialization. |
   | hoisting done, with initializing as ‘default’ value        | Hoisting is done, but not initialized (this is the reason for the error when we access the let variable before declaration/initialization  | Hoisting is done, but not initialized (this is the reason for the error when we access the const variable before declaration/initialization |

    **[⬆ Back to Top](#table-of-contents)**
    
2. ### ### What are the Differences between TypeScript and JavaScript?

    | TypeScript	                            | JavaScript                        |
    | ----------------------------------------- | ------------------------------------------- |
    | TypeScript is an Object-Oriented language | JavaScript is a Scripting language       |
    | It has a feature known as Static typing   | It does not have static typing            |
    | TypeScript gives support for modules      | JavaScript does not support modules     |
    | It supports optional parameter function   | It does not support optional parameter function  |

    **[⬆ Back to Top](#table-of-contents)**
    
2. ### Features of ES6

   Features of ES6

   1. let and const Keywords
   2. Arrow Functions
   3. Multi-line Strings
   4. Default Parameters
   5. Template Literals
   6. Destructuring Assignment
   7. Enhanced Object Literals
   8. Promises
   9. Classes
   10. Modules
   11. Spread / Rest Operator

   **[⬆ Back to Top](#table-of-contents)**
    
3. ### What is the rest parameter and spread operator in JavaScript ?

   In Javascript, both the spread operator and rest parameter have the same syntax which is three dots(…). Even though they have the same syntax they differ in functions.

   **Spread operator:** The spread operator helps us expand an iterable such as an array where multiple arguments are needed, it also helps to expand the object expressions. In cases where we require all the elements of an iterable or object to help us achieve a task, we use a spread operator.

   Note: There can be more than one spread operator in javascript functions.

   ```
      var array1 = [10, 20, 30, 40, 50];
      var array2 = [60, 70, 80, 90, 100];
      var array3 = [...array1, ...array2];
      console.log(array3);
   ```

   **Rest operator:** The rest parameter is converse to the spread operator. while the spread operator expands elements of an iterable, the rest operator compresses them. It collects several elements. In functions when we require to pass arguments but were not sure how many we have to pass, the rest parameter makes it easier. 

   Note: There must be only one rest operator in javascript functions.

   ```
      function average(...args) {
         console.log(args);
         var avg =
               args.reduce(function (a, b) {
                  return a + b;
            }, 0) / args.length;
         return avg;
      }
      console.log("average of numbers is : " + average(1, 2, 3, 4, 5));
      console.log("average of numbers is : " + average(1, 2, 3));
   ```

   **[⬆ Back to Top](#table-of-contents)**
    
1. ### What is a promise
   A promise is an object that may produce a single value some time in the future with either a resolved value or a reason that it’s not resolved(for example, network error). 
   
   It will be in one of the 3 possible states: **fulfilled, rejected, or pending.**

   The syntax of Promise creation looks like below,
   
      ```
         const promise = new Promise(function (resolve, reject) {
         // promise description
         });
         The usage of a promise would be as below,
         const promise = new Promise(
         (resolve) => {
            setTimeout(() => {
               resolve("I'm a Promise!");
            }, 5000);
         },
         (reject) => {}
         );

         promise.then((value) => console.log(value));
      ```

   **[⬆ Back to Top](#table-of-contents)**
   
2. ### Why do you need a promise

   Promises are used to handle asynchronous operations. They provide an alternative approach for callbacks by reducing the callback hell and writing the cleaner code.

   **[⬆ Back to Top](#table-of-contents)**
   
3. ### What are the three states of promise

   Promises have three states:

   i.	**Pending:** This is an initial state of the Promise before an operation begins

   ii. **Fulfilled:** This state indicates that the specified operation was completed.
   
   iii. **Rejected:** This state indicates that the operation did not complete. In this case an error value will be thrown.

   **[⬆ Back to Top](#table-of-contents)**

4. ### What is promise all

   Promise.all is a promise that takes an array of promises as an input (an iterable), and it gets resolved when all the promises get resolved or any one of them gets rejected. For example, the syntax of promise.all method is below,
   
   ```
   Promise.all([Promise1, Promise2, Promise3]) 
      .then(result) => {   console.log(result) }
      .catch(error => console.log(`Error in promises ${error}`))
   ```

   **[⬆ Back to Top](#table-of-contents)**

4. ### Async/await

   There’s a special syntax to work with promises in a more comfortable fashion, called `“async/await”`. It’s surprisingly easy to understand and use.

   #### await
   The await operator is used to wait for a Promise and get its fulfillment value. It can only be used inside an async function or at the top level of a module.

   ```
   function resolveAfter2Seconds(x) {
      return new Promise((resolve) => {
         setTimeout(() => {
            resolve(x);
         }, 2000);
      });
   }
   async function f1() {
      const x = await resolveAfter2Seconds(10);
      console.log(x); // 10
   }
   f1();
   ```

   **[⬆ Back to Top](#table-of-contents)**

5. ### What is an event loop in JavaScript ?

   Event loop: An event loop is something that pulls stuff out of the queue and places it onto the function execution stack whenever the function stack becomes empty.

   **[⬆ Back to Top](#table-of-contents)**

5. ### Event bubbling

   The bubbling principle is simple.

   When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.

   Let’s say we have 3 nested elements FORM > DIV > P with a handler on each of them:

   ```
   <style>
   body * {
      margin: 10px;
      border: 1px solid blue;
   }
   </style>

   <form onclick="alert('form')">FORM  // first 
      <div onclick="alert('div')">DIV  // Second
         <p onclick="alert('p')">P</p> // Third
      </div>
   </form>

   ```

   ![Alt text](bubbling.jpg)

   ![Alt text](image-7.png)


   The Event bubbling in JavaScript is a type of event propagation. The event triggers the innermost target element and consecutively triggers the parent element of the target element in the same hierarchy until it triggers the outermost element.

   It is a procedure where it starts from the element that triggered the event and then bubbles up to the ancestor elements in the hierarchy.   

   **[⬆ Back to Top](#table-of-contents)**

6. ### How to Stop Event Bubbling
   
   Event Bubbling is a default behavior for events. But in some cases, you might want to prevent this.

   Let's say, for example, from our HTML code, that you want the div to open a modal when it is clicked. For the button, on the other hand, you want it to make an API request when it is clicked.

   In this case, you may not want the modal to open when you click the button. You might want the modal to only open when you actually click it (and not when you click any of its children). This is where preventing event propagation comes in.

   To prevent event bubbling, you use the `stopPropagation` method of the event object.

   ```
      button.addEventListener("click", (event) => {
         // do anything with the event object
      }

      body.addEventListener('click', () => {
         console.log("body was clicked")
      })

      div.addEventListener('click', () => {
         console.log("div was clicked")
      })

      span.addEventListener('click', () => {
         console.log("span was clicked")
      })

      button.addEventListener('click', (event) => {
         event.stopPropagation()
         console.log("button was clicked")
      })

   ```

   **[⬆ Back to Top](#table-of-contents)**

7. ### Event Capturing

    **Event Capturing is opposite to event bubbling,** where in event capturing, an event moves from the outermost element to the target. Otherwise, in case of event bubbling, the event movement begins from the target to the outermost element in the file. Event Capturing is performed before event bubbling but capturing is used very rarely because event bubbling is sufficient to handle the event flow.

   ```
      <form onclick="alert('form')">FORM  // Third
         <div onclick="alert('div')">DIV  // Second
            <p onclick="alert('p')">P</p> // first
         </div>
      </form>

   ```

   There’s another phase of event processing called `“capturing”`. It is rarely used in real code, but sometimes can be useful.

   The standard DOM Events describes 3 phases of event propagation:

   **Capturing phase** – the event goes down to the element.

   **Target phase** – the event reached the target element.

   **Bubbling phase** – the event bubbles up from the element.

   Here’s the picture, taken from the specification, of the capturing (1), target (2) and bubbling (3) phases for a click event on a <td> inside a table: 

   **[⬆ Back to Top](#table-of-contents)**

8. ### Closure in JavaScript

   A closure is a feature of JavaScript that allows inner functions to access the outer scope of a function. Closure helps in binding a function to its outer boundary and is created automatically whenever a function is created. A block is also treated as a scope since ES6. Since JavaScript is event-driven so closures are useful as it helps to maintain the state between events.

   ```
      function init() {
         var name = "Mozilla"; // name is a local variable created by init
         function displayName() {
            // displayName() is the inner function, that forms the closure
            console.log(name); // use variable declared in the parent function
         }
         displayName();
      }
      init();
      
   ```
   **[⬆ Back to Top](#table-of-contents)**

10. ### Implementation of Queue data structure in Javascript

   In This article, we would be implementing Queue data structure in javascript. A Queue works on the FIFO(First in First Out) principle. Hence, it performs two basic operations which are the addition of elements at the end of the queue and the removal of elements from the front of the queue. Like Stack, Queue is also a linear data structure. 

   Note: Assuming a queue can grow dynamically we are not considering the overflow condition Now let’s see an example of a queue class using an array:- 

   To implement a queue data structure we need the following methods:

   enqueue : To add elements at end of the queue.
   dequeue: To remove an element from the front of the queue.
   peek: To get the front element without removing it.
   isEmpty: To check whether an element is present in the queue or not.
   printQueue: To print the elements present in queue.

   **[⬆ Back to Top](#table-of-contents)**

11. ### What is Array Destructuring in JavaScript?
   Destructuring the array in JavaScript simply means extracting multiple values from data stored in objects and arrays. The destructing assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables. We can extract a value from an array and put them into other variables. Array destructuring javascript is also used to assign and declare a variable. For destructing an array, we use the index value of that particular array.

   #### What is Destructuring?

   In general, destroying means to destroy or to reduce something to its small portions. By saying array destructuring javascript, we do not mean to destroy the array, but it means to break the array into simple fragments which can be used to assign a new variable. These fragments can be easily accessed and can be referenced by the variables. The destructuring of the array totally depends upon the coder and how much he wants to destroy or destruct the given array.
      
   **[⬆ Back to Top](#table-of-contents)**

11. ### Difference between Debouncing and Throttling:

   Below are the main differences between Debouncing and Throttling

   | Debouncing                                                        | Throttling                                                 |
   | ------------------------------------------------------------------| ------------------------------------------------------------------- |
   | Debouncing waits for a certain time before invoking the function again. | Throttling limits the number of times the function can be called over a certain period. |
   | Ensures that the function is called only once, even if the event is triggered multiple times.  | Ensures that the function is called at a regular interval, even if the event is triggered multiple times.  |
   | Useful when you want to delay the invocation of a function until a certain period of inactivity has passed.  | Useful when you want to delay the invocation of a function until a certain period of inactivity has passed.    |
   | Eg. You can debounce an async API request function that is called every time the user types in an input field. | Eg. You can throttle a slide change Function that is called every time the user clicks a button in a carousel.  |

   **[⬆ Back to Top](#table-of-contents)**
    
11. ### Difference Between Method Overloading and Method Overriding in Javascript

   #### JavaScript does not support overloading.

   JavaScript supports overriding, so if you define two functions with the same name, the last one defined will override the previously defined version and every time a call will be made to the function, the last defined one will get executed.

   #### Example of overriding functions in JavaScript

   ```
      function addNumbers(n1, n2, n3) {
         return n1 + n2 + n3;
      }
      function addNumbers(n1, n2) {
         return n1 + n2;
      }
      var sum = addNumbers(1, 2, 3);  
      console.log(sum); // 3 because 
   ```

   **[⬆ Back to Top](#table-of-contents)**

12. ### Differences between Arrow and Regular function

   There are certain differences between Arrow and Regular function, i.e

   1. Syntax
   2. No arguments (arguments are array-like objects)
   3. No prototype object for the Arrow function
   4. Cannot be invoked with a new keyword (Not a constructor function)
   5. No own this (call, apply & bind won't work as expected)
   6. It cannot be used as a Generator function
   7. Duplicate-named parameters are not allowed

   **[⬆ Back to Top](#table-of-contents)**

13. ### Shallow Copy and Deep Copy in JavaScript


   There are two ways to clone an object in Javascript:

   **Shallow copy:** means that only the first level of the object is copied. Deeper levels are referenced. A **shallow copy** is a copy that only goes one level deep. In other words, it copies the object and all its properties, but any nested objects or arrays will still reference the same memory location as the original object.

   **Deep copy:** means that all levels of the object are copied. This is a true copy of the object. A **deep copy** is a copy that creates a new object with new memory locations for all of its properties and nested objects or arrays. It means that if you make changes to the copied object or any of its nested objects or arrays, it will not affect the original object.

   ```
   let obj = {name: "Ramesh", profession: {des: "lead", location: "somewhere"}};

   const shallowcopy = {...obj};
   console.log(shallowcopy);

   const deepcopy = JSON.parse(JSON.stringify(obj));
   console.log(deepcopy);

   ```
   
   **[⬆ Back to Top](#table-of-contents)**