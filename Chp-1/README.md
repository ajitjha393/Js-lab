## CHAPTER 1 - JS CODE EXECUTION

Many of us might know how to write a program in JavaScript and don't exactly understand how it works under the hood.

So let's explore this today!

How our JS code gets executed what are the different phases and steps that come into play.

![image](https://user-images.githubusercontent.com/42679346/126876041-c107ca41-331f-49b2-9969-4306fcf865a4.png)


### Definition of JavaScript:

JS is a single-threaded, lightweight, dynamically interpreted, and just-in-time compiled programming language with first-class functions.

Let’s deconstruct each of these building components of JS:

> **_Single threaded_**

JS Can only execute one thing at a time (Will discuss this in detail below :- )

> **_Lightweight_**

It is called a lightweight lang because it does not come with many type constructs and syntactic requirements.

Everything is a object in JS which makes it easy and flexible to use and understand.
This feature makes JS a multi-paradigm language.

> **_First class fn:_**

JS is a higher-order first class functional programming language because we can pass around function and return a function from anywhere in our code
This is possible in JS because everything including functions is an Object.

> **_JIT_**

Just in time aka JIT compilation
Unlike other statically typed languages like C / C++
JS does not gets compiled beforehand instead it undergoes JIT compilation.

This basically means that the code is compiled in the memory just before it gets executed.

This is what makes JS dynamic because it is decided at the time of execution that what type a variable will store and it can change during the course of program.

You may ask Why is this important ?

- It’s because our browser’s JS engine can only execute machine level code not the source code we provide.
- It converts our source code to bytecode inside the memory and feeds it to the JS engine to execute that code

### What are JS engines ?

- These are responsible for executing our JS code and interacting with the surrounding Environment APIs.
- Each Browser vendor have their own engine that follows Ecmascript guidelines.
  Example : V8 (Chrome) SpiderMonkey (Firefox) Nitro (Safari)

### What is execution context?

An execution context is an abstract concept of an environment where the Javascript code is evaluated and executed. Whenever any code is run in JavaScript, it’s run inside an execution context.

When a JavaScript Engine executes a script, it creates execution contexts. Each execution context has two phases.

- The Creation Phase
- The Execution Phase

Let's take an example to understand it.

![image](https://user-images.githubusercontent.com/42679346/126876053-d455a66e-c83f-4c6b-9513-159618be3dc1.png)


### The Creation Phase:

When a script executes for the first time, JavaScript Engine creates a global execution context. During the creation phase following tasks are performed:

#### Task 1:

Creation of a global object i.e. "window" in the browser (or in "global" node).

#### Task 2:

Creation of a "this" object binding that points to the global object created above.

#### Task 3:

Setting up a "Memory Heap" for storing variables and function reference.

#### Task 4:

Storing the function declarations in the memory heap and variables within the global execution context with the initial values as undefined.

![image](https://user-images.githubusercontent.com/42679346/126876059-1bdcb9a8-2539-4fa9-9034-aa1679a51572.png)


### The Execution Phase:

During the execution phase the JavaScript Engine executes the code line by line. In this phase, it assigns values to the variables and executes the function calls.
Note: For every function call, the JavaScript Engine creates a new Function Execution Context.

![image](https://user-images.githubusercontent.com/42679346/126876063-c4f40ee3-dff2-4cd5-8a51-199b1ca74088.png)

### Function Execution Context vs Global Execution Context:

The Function Execution Context is similar to the Global Execution Context but instead of creating the global object, it creates the arguments object that contains a reference to all the parameters passed into function.
