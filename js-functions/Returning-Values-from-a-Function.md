# Returning Values from a Function



```javascript
// Defining function
function getSum(num1, num2) {
 var total = num1 + num2;
 return total;
}

```

```javascript

// Displaying returned value

var result1 = getSum(6, 20);
console.log(result1) // 0utputs: 26
var result2 = getSum(-5, 17);
console.log(result2) // 0utputs: 12

```
 
To get the result for the above function, we need to console with the function name like we returned total so it will go and save in the function script and we need to call our function within the console and the value we returned here is a number.
 
A function can return a value back to the script that called the function as a result using the return statement. The value may be of any type, including arrays and objects. Whenever a function sees return the function will stop there only , it won’t execute other statements.


**Exercises:**

1. Write a short program for getting the total average of Marks that you got in maths and science, take them as 2 variables and return the average of both 2 variables?

Feedback after submit
```javascript
function averageOfSubjects(maths,science){
   return (maths+science)/2
}
console.log(averageOfSubjects(25,30));
 ```

2. What is the output of the following program?

```javascript
function insertingElement(arr){
   var a=5;
   arr.push(a);
   return arr;
   console.log(arr);
 
}
console.log(insertingElement([1,2,3,4]));
 
 
// Feedback after submit: [ 1, 2, 3, 4, 5 ]
```
3. Notice that the line console.log(arr) will not print anything as the function stops executing after the return statement.
```javascript
What is the error in the following code?
		function multiplyString(string,num){
   string*num;
}
 
console.log(multiplyString("kumar",2));
// Feedback after submit
// Undefined
```
 
We returned nothing that’s why when we consoled it also it was given undefined.