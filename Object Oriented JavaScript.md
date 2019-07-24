# What is a constructor function.

JavaScript uses special functions called constructor functions to define and initialize objects and their (prototype) properties.

# Define Encapsulation, NameSpace, Abstraction, Inheritance, Polymorphism, ?

# Factory Functions in JavaScript?

# Find prototype of object
```
Object.getPrototypeOf(obj);
obj.prototype;


```

# Find constructor of object
```
obj.constructor; // OR : obj.constructor.name;
obj instanceof ConstructorFunctionName
```

The `instanceof` operator tests whether the prototype property of a constructor appears anywhere in the prototype chain of an object.

# What is Property Shadowing
When we have own property and prototype property with same name. Both exists but, Precedence is given to own property while accessing. This is called Property Shadowing.
```
let myFun = function(){
  this.a = 1;
  this.b = 2;
}
myFun.prototype.b = function(){ return this.a+this.b; };

obj = new myFun();

console.log(obj.b); // Outputs 2 tough we also have b prototype property.

```
