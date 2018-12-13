# Define Closure

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
