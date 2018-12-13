# Define Closure
A closure is the combination of a function and the lexical environment within which that function was declared.  This environment consists of any local variables that were in-scope at the time the closure was created.
OR


```
function makeFunc() {
  var name = 'Mozilla';
  function displayName() {
    alert(name);
  }
  return displayName;
}

var myFunc = makeFunc();
myFunc();
```
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures

# Define Mutable - immutable 

# What are primitive elements

# Self invoking function

# Hoisting
Variable and function declarations are physically moved to the top of your code
```
catName("Chloe");

function catName(name) {
  console.log("My cat's name is " + name);
}
THIS WORKS 
```
JavaScript only hoists declarations, not initializations. If a variable is declared and initialized after using it, the value will be undefined.
```
console.log(num); // Returns undefined 
var num;
num = 6;
```
https://developer.mozilla.org/en-US/docs/Glossary/Hoisting


# Differences between function .call .apply .bind

# 
