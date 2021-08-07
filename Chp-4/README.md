## CHAPTER 4 CALLBACKS

Hey folks! So far in JS Lab, we discussed how code gets executed and what exactly closure means in JS.
 
Moving ahead, another important topic in understanding JS is learning about its asynchronous capabilities.

Let’s discuss these today and look into callbacks.


![image](https://user-images.githubusercontent.com/42679346/128609841-3d888091-60d4-45a8-abde-c195d23f3b5d.png)

What are callbacks:

Before we throw some technical jargons at you , let me give you an analogy.

How does the postal service work ?

Say I wanted to send some message to my friend (Cool down Gen-z devs, We didn’t have phone back then).
So I write my message on a letter and give it to the postman. 
He than takes my letter and delivers it to the desired address. 
Once the letter reaches my friend , He can open it and read that letter and my message will be delivered. 

(Thank God Mobile phones were invented!)

This model here is what we refer to as ***callbacks***.

And the flow of information here is what we called ***asynchronous***.

### Technical Definition:

A callback is a procedure / method that is to be invoked at a later point of time.

Callbacks are what provides asynchronous functionalities to Javascript. It’s an integral part of building modern day web application

It involves passing a function as a parameter to another function which is then invoked in some other environment when a subscribed event occurs. 

PS: We can pass function reference as a parameter because they are basically objects under the hood.


### Example 1:

- We setup a ‘click’ listener on our button element and we want to execute some code every time a button is pressed.
- Here each button press is an event that occurs.

![image](https://user-images.githubusercontent.com/42679346/128609967-ffefb5e1-ccb2-438a-a233-089cacd101c7.png)


In order to execute some code for that we have registered a foo function which acts as a callback which gets invoked every time a button click happens. 

This asynchronous nature that callbacks provide us , makes it easy to structure our application based on event models.

### Example 2:

What if we want to delay some code executions and execute that after x unit time has passed.
Say we need to greet the user after 5s.
 
Usually, code can only get executed one by one, but if we want this required behavior. 
setTimeout can help us with that.

### setTimeout:

The function that we provide to setTimeout acts as a callback function which gets executed after delay time

Syntax: setTimeout(fn, delay)

![image](https://user-images.githubusercontent.com/42679346/128610005-9b618ab7-67b8-47b2-8c1b-111b5126f9de.png)


Callbacks are awesome and opens a whole new dimension of async JS to us.
But there might arise some problem when you have to execute some code only after previous timeout has occurred.

### Example 3

Say I want to print 
- 1 to console after 3s
- 2 to console after 6s
- 3 to console after 9s

What we can do is use nested setTimeout here as shown:

![image](https://user-images.githubusercontent.com/42679346/128610041-febeb665-0a61-4abf-a2eb-940fa2e02849.png)

Here you see how the nesting of callbacks becomes difficult to parse and maintain.

Since this used to occur so frequently developers have a name for this called as “Callback hell”.

To solve this we have "Promises" which we will see in next chap.


