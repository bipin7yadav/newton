Understanding-the-Variable-Scope-in-functions_key1


```javascript
// Defining function

function greetWorld() {
 var greet = "Hello World!";
 console.log(greet);
}
greetWorld(); // Outputs: Hello World!
console.log(greet); // Uncaught ReferenceError: greet is not defined
```

Understanding-the-Variable-Scope-in-functions_key2

 
Understanding-the-Variable-Scope-in-functions_key3


Understanding-the-Variable-Scope-in-functions_key4


```javascript

var greet = "Hello World!";
// Defining function
function greetWorld() {
  console.log(greet);
}
greetWorld();  // Outputs: Hello World!
console.log(greet); // Outputs: Hello World!

```

Understanding-the-Variable-Scope-in-functions_key5
Understanding-the-Variable-Scope-in-functions_key6


Understanding-the-Variable-Scope-in-functions_key7


Understanding-the-Variable-Scope-in-functions_key8
