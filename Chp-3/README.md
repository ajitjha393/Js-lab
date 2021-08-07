## CHAPTER 3 - CLOSURES

Coding in JavaScript without an understanding of closures is like trying to speak English without an understanding of grammar rules — you might be able to get your ideas across, but probably a bit awkwardly.

So Let's start Demystifying Closures - 

![image](https://user-images.githubusercontent.com/42679346/128040634-7e20ebbb-f795-4122-85f4-6e0a29260006.png)

MDN docs says:

>A closure is the combination of a function bundled together  with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function.

In Simple words:
A function bundled together with its lexical environment. In other words, it is an inner function which has access to variable of outer function.

Note: Closure will remember the reference of a particular value in its lexical scope and not its value. 

Example:

![image](https://user-images.githubusercontent.com/42679346/128040891-d36eedfb-b58e-4d28-b41a-4551466515a9.png)

The amazing thing is, even if the outer function returns the inner function then also inner function will have access to outer function variables.1

In other programming languages if a function returns then it becomes ready for garbage collection or is completely removed from the heap, but in Javascript if there is closure then the parent function variables remain in the heap.

## Example: This is the interview question from Razorpay 2021

Can you try solving it ? 
Hint: You have to return a function which will take one parameter and you need to return a closure.

![image](https://user-images.githubusercontent.com/42679346/128041006-567ddd8a-868c-402d-9c86-be22c299703d.png)


If you carefully notice this solution and compare it with the definition of closure, you will notice  function which I have created returns the addition of N (parameter) and input (variable present in its lexical environment).

![image](https://user-images.githubusercontent.com/42679346/128041674-bbfee82a-5734-4de8-8930-ac80a5415011.png)


## Uses of Closure:

1) Module Design Pattern
2) Currying
3) setTimeouts
4) Iterators
5) Memoize
6) To maintain state in Async world

## Advantages of Closure:

1) Callbacks implementation in javascript is heavily. dependent on how closures work.
2) Mostly used in Encapsulation of the code.
3) Also used in creating API calling wrapper methods.

## Disadvantages of Closure:

1) Variables used by closure will not be garbage collected.
2) If closures will not be handled correctly it will result to memory leaks


## Bonus - What is Garbage Collector

It's basically a program run by JS Engine to monitor memory allocation and determine when a block of allocated memory is no longer needed and reclaim it.

## Whats Next: 

Thanks for reading this chapter on "Closures". In the next chapter of this series, we shall take a look at Callbacks.
Stay tuned and cheers! 

Content Credits:  
@smileguptaaa @jha_bisu
