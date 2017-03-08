## 1 task

Example:

```javascript
var makeFunction = function () {
    var addOne = function (x) {
        return x + 1;
    };
    return addOne; // return the function
};
// makeFunction is a function with no arguments

var f = makeFunction();
// f is a function that takes one argument

var y = f(3);
// now y is 4
```

Create a function that will always return a number multiply on 3!

Write a JavaScript program to calculate the factorial of a number using 1 task, but ask user for a number to get factorial from using prompt() function.

Then give an answer to user after calculation is finished using alert(number);

## 2 task

Make this syntax possible: var a = add(2)(3); //5

```javascript
var add = function () {
    // your code
};

console.log(add(2)(3)); // 5

```

## 3 task 

Transform array of numbers to array of functions that will alert that digits:

```javascript
 
var numberArray = [1, 2, 3, 4, 10, 5, 6, 7];

// in result we will have: [function (){...}, function (){...}, function (){...}, function (){...}]
```
