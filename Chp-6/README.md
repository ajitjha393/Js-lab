## CHAPTER 6 - IIFE

Hi Everyone! We are back with yet another episode of JS Lab. 

In this chapter, you will be learning everything about *"Immediately Invoked Function Expression"* a.k.a IIFE.

Demystifying IIFE 👇🏻

![image](https://user-images.githubusercontent.com/42679346/130602960-b6c671c8-22eb-4669-9c41-e4e7164aed8b.png)

 IIFE is a JavaScript Function that runs as soon as it is defined. It is a design pattern that essentially contains two parts:

- It is an anonymous function with its lexical scope enclosed within parenthesis ( ).
- Creates the immediately invoked function expression ( ).

### Why do we need IIFE:
We know that functions in JS have local scope. For eg: there are multiple .js files in your applications over a while. It's highly possible that functions with the same name exist across files.

In such scenarios, a single web page could include all these .js files, polluting the global scope by having two or more functions/variables with the same name.

### How to write IIFE:
IIFEs are very useful because they don't pollute the global object and they are a simple way to isolate variable declarations.

This is the syntax of IIFE:

![image](https://user-images.githubusercontent.com/42679346/130603375-4b9391b5-5cb0-4ac3-9120-10f8f26f03ba.png)

IIFEs can also be defined with arrow functions.

![image](https://user-images.githubusercontent.com/42679346/130603433-2437da6e-f27a-4be0-8e6c-8b770878c828.png)

Here is a comparison between a normal function definition and IIFE.

![image](https://user-images.githubusercontent.com/42679346/130603502-42cb1046-0f55-416d-ad05-eeaaa0d4cc93.png)


