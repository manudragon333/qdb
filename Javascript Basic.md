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
A mutable object is an object whose state can be modified after it is created.

Immutables are the objects whose state cannot be changed once the object is created.


Mutable is a type of variable that can be changed. In JavaScript, only objects and arrays are mutable, not primitive values.

You can make a variable name point to a new value, but the previous value is still held in memory. Hence the need for garbage collection.

```
a={k1: 10};
b=a;
b.k1 = 20;
console.log(a.k1); // Will return 20; Coz b is assigned the memory reference of a not a copy of it / a is mutable.
```

https://developer.mozilla.org/en-US/docs/Glossary/Mutable

# How can you stop mutation of object
Object.freeze()

The Object.freeze() method freezes an object. A frozen object can no longer be changed i.e it becomes immutable.
```
const object1 = {
  property1: 42
};

const object2 = Object.freeze(object1);

object2.property1 = 33;
// Throws an error in strict mode; object2.property1 still remains 42
```

# What are primitive elements
A primitive (primitive value, primitive data type) is data that is not an object and has no methods. In JavaScript, there are 6 primitive data types: string, number, boolean, null, undefined, symbol (new in ECMAScript 2015).

All primitives are immutable, i.e., they cannot be altered. The variable may be reassigned a new value(a new memory reference is created, unlike mutable objects where memory reference is passed on), but the existing value can not be changed in the ways that objects, arrays, and functions can be altered(Coz memory reference is passed on).

# Self invoking function / IIFE (Immediately Invoked Function Expression)
A self-invoking expression is invoked right after its created/ is defined. This is basically used for avoiding naming conflict as well as for achieving encapsulation. The variables or declared objects are not accessible outside this function.
```
// Generally we return a Object / Function. For this ex. we return a variable.
var result = (function () { 
    var name = "Barry"; 
    return name; 
})(); 
// Immediately creates the output: 
result; // "Barry"
name; // throws "Uncaught ReferenceError". Variable is not accessible from the outside scope
```

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


# Ajax States

# Array functions - map, reduce, filter etc....

# Exception Handling (try, catch, finally, throw)

# Dom operations dynamically.