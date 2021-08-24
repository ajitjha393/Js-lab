## CHAPTER 7 - Array and Array Methods

Programming is all about data manipulation.

Hence it becomes essential to understand how we store them and how we apply various operations to that data
Thus today we will be discussing Arrays and useful operations that you can perform on them.

![image](https://user-images.githubusercontent.com/42679346/130608542-a70a17c3-7fbd-4d51-8c67-aa2cc0a68055.png)

So far we know how to store data in a variable 
Say a number -> let number = 5 

But how do you store a bunch of data together as a collection say (4,5,6,7,8)?

This is where Array comes in!

An array is a Data Structure that stores and represents a collection of data in the form of a list.

It stores data as elements in a sequential manner and retrieves them back via index position when you need them.

Example 1:

![image](https://user-images.githubusercontent.com/42679346/130608741-941e6d37-7945-4c2d-961f-367b70648675.png)

Now I can access each of these via square bracket syntax `[]`

- listOfMovies[0] // 'Inception'
- listOfMovies[1] // 'Fight Club'
- listOfMovies[2] // 'The Matrix'
- listOfMovies[3] // 'Memento'

Array Data Type is characterized by the length property present. 

listOfMovies.length // 2

Since JS is a dynamically typed language, arrays can be a collection of elements of any type 

Example 2:

![image](https://user-images.githubusercontent.com/42679346/130608833-6b384faf-2cfc-4606-9d1d-1ddf19c015f8.png)

### Create a new array:
There are various ways of creating a new Array but the most common ways are: 

1) Square Bracket Syntax 

2)   new Array()

3) Array.of (Similar to Array constructor)

4) Array.from (Used to create a list like an object to actual Array)

![image](https://user-images.githubusercontent.com/42679346/130608904-0e20672f-f8ec-494c-ba90-dd82e83e97c1.png)

### Useful Array Methods:
1) push() – Insert an element at the end of the array.

2) unshift() – Insert an element at the beginning of the array.

3) pop() – Remove an element from the end of the array.

![image](https://user-images.githubusercontent.com/42679346/130608960-77986a36-293d-42ac-adb0-dd0f9de0c7a4.png)


4) shift() – Remove an element from the beginning of the array.

5) slice() – Create a shallow copy of an array.

6) length – Determine the size of an array.

![image](https://user-images.githubusercontent.com/42679346/130609013-ff1f4901-5da6-4b99-b350-b1af75798759.png)


### Array Iterator Methods:
These are very useful methods that allow us to iterate over each element of the array and perform transformations, filtering out stuff, and more in a streamlined manner.

Below are the most widely used methods:  
1. map
2. filter
3. reduce
4. some
5. find


>Note: All the above-mentioned methods are first-class functions that take another function as an argument wherein we specify the logic to iterate and apply in that function.

### Map:

The map() method returns a new array by iterating through the elements and applying the provided transformation function.

Example: Let's map out a num array to its corresponding squared array

![image](https://user-images.githubusercontent.com/42679346/130609174-24eea0fe-5625-4a75-a086-e80445ff72cc.png)

### Filter:
The filter() method returns a new array with all the elements that satisfy the condition mentioned in the predicate function.
 
Example:

![image](https://user-images.githubusercontent.com/42679346/130609225-d86f9efb-f087-4b6a-a875-9cf1c820a0cd.png)


### Reduce:

The reduce() method applies a reducer function on each of the elements and returns an output value.
Reducer function accepts 2 arguments `acc` which stores accumulated value till current execution and `curr` stores current element value.

![image](https://user-images.githubusercontent.com/42679346/130609290-04ccec83-2723-4811-a029-72f008529338.png)

### Some:
The some() method returns a boolean value depending upon whether the predicate condition is being satisfied (true) or not (false).

![image](https://user-images.githubusercontent.com/42679346/130609369-f72c11b0-b82c-42bb-836d-f869b490be93.png)

### Find:
It returns the first matched element from the array that satisfies the condition in the function.

Example - Let's return the age of the first person that is greater than 30.


![image](https://user-images.githubusercontent.com/42679346/130609435-c6d2351f-c5e7-421a-81e4-7691a1005e81.png)

### More Array Methods:

![image](https://user-images.githubusercontent.com/42679346/130609467-575496b4-88dc-44df-a16d-4961ec362946.png)

