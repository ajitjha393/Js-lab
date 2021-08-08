## CHAPTER 2 - HOISTING IN JS

A lot of people would tell you that "Hosting" meaning variables physically moved to the top. 

For many Beginners, it seems like some spooky weird stuff is happening behind the scenes but don't quite understand it.

What do you think? Is moving on top is Hosting or its something different. 

Lets Demystify this in our today's chapter -

![image](https://user-images.githubusercontent.com/42679346/127195623-65e9a553-7f5a-4928-b687-2ec50e73033b.png)

MDN Docs says :
> Variable and function declarations are physically moved to the top of your code, but this is not in fact what happens.
>  Instead the variables and function declarations are put into memory during compile phase, but stays exactly where you typed them in your code

### What Actually Happens:

To fully understand hoisting,  you should know how code is executed in JavaScript. 

If you don't know, check it out : [How JS code is Executed](https://twitter.com/smileguptaaa/status/1418976271913021440?s=20)

### Example 1:

Can you try guessing  the output for this code ? or Will you get any errors by writing it in such a way?

![image](https://user-images.githubusercontent.com/42679346/127196176-48fb02a5-f423-41e4-ba4d-03947acd2afa.png)


### Solution:

![image](https://user-images.githubusercontent.com/42679346/127196203-3793c92a-1864-4214-93af-e08791c1e31a.png)

### Explanation:

Here, although the variable "greeting" is used before it is declared, you won't see any errors due to the concept of hoisting.

### Behind the Scene:

When I ran this code, what will happen is: ( as mentioned above) code execution takes place in 2 steps.

During the creating phase of global execution context the JS Engine places the variable greeting in the memory and initialises its value to "undefined".

Similar to variables, functions are also hoisted in JavaScript.

Here is an example:

![image](https://user-images.githubusercontent.com/42679346/127196785-e0d4edb7-cea1-4f2f-bd5a-410302a559c0.png)


### Example 2:
Can you guess what will happen here:

![image](https://user-images.githubusercontent.com/42679346/127196893-64a855d1-2f96-4179-8aed-ffc6fb832b83.png)


Solution:

![image](https://user-images.githubusercontent.com/42679346/127196967-aa623879-9113-44f9-b39a-9854bd82180e.png)

So what just happened? Didn't I say that functions are also hoisted just like variables. 

I still stand by my statement, both variables and functions are hosted.

If you carefully see the example 2, I wrote a function expression and not function.


There is a significant difference between function and function expression. This I will discuss in my upcoming tweets.

For now, just remember: 
- Functions and Function Expressions are different. 
- Functions can be hoisted and Function Expressions don't.


### Question Time:

Are let and const variable declarations also hoisted?

It's a myth, that let and const are not hoisted.  In reality they are hoisted. 

For the ES6 features like let and const the creation phase works quite differently

It still goes through the code and allocates spaces for variables but the initializer sets the variable with a special mode called TDZ (Temporal Dead Zone) which means the variable exists but they cannot be accessed before their declarations.

### TDZ: 

It is a behaviour in JS that occurs when declaring a variable with let and const. In ES6, accessing a let or const before its declaration cause ReferenceError. The time span when that happens between the creation of variable binding and its declaration is The Temporal Dead Zone.

To Sum up in case of:
1) var, let and const  - Hoisting ✅
2) Functions -  Hoisting ✅
3) Function Expressions - Hoisting ❎
4) Arrow Functions - Hoisting ❎

### Whats Next: 
Thanks for reading this thread on "Hoisting". In the next tweet of this series, we shall take a look at Closures
Stay tuned and cheers! 





