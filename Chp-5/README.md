## CHAPTER 5 - PROMISES

Promises are one of the ways by which we can deal with asynchronous operations in JavaScript. Many people struggle in understanding, how Promises work.

Demystifying Promises :

![image](https://user-images.githubusercontent.com/42679346/128611153-9c659e2f-cbca-4b1b-badf-9041cfdeaa9f.png)

### MDN Says:

It is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason.

Theoretically, JS promises are no different than the real life promises — when coupled with result oriented conditions.

In Other Words:

Promise is an action which guarantees a result in future, the result could be the expected one(positive) and if anything goes wrong, the result will be something which was not anticipated(negative). While doing the promise we also close on the conditions - what if


Promises in JavaScript is in one of these states: 
- Pending: initial state, neither fulfilled nor rejected
-  Fulfilled(resolved): meaning that the operation was completed successfully
- Rejected: meaning that the operation failed



### Example 1: 

John lives with his mom. He is a very good boy except he does not like to clean his room.

Everyday he seeks his mom's permission in evening to go out and play with his friends.

One day, in order to make John clean his room, his mom added a condition on him.


![image](https://user-images.githubusercontent.com/42679346/128611204-a653375e-3b48-40ed-bd2a-2ce3c464f9e8.png)


Two things will happen here
1) If John is able to clean his room(fulfilling the promise condition): He goes out for football.

2) But what if he does not clean(failing to complete the promise condition): he needs to do the laundry.

Let's see same situation in code base.

### Constructing Promise:

![image](https://user-images.githubusercontent.com/42679346/128611214-b8c2da72-a6b9-4c35-93c4-f2abbfaea4dc.png)

### Returning Promise:

![image](https://user-images.githubusercontent.com/42679346/128611222-88a3348b-7032-448b-b75e-34f4518ce323.png)

### Why do we use Promises:

Promise(s) is the antidote to Callback-hell. It’s a new way to introduce asynchronous callbacks without having to deal with ‘Pyramid of doom’.


