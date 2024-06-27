# Breakout-room-1
### 1. What is scope in JavaScript, and why is it important?
Scope is what we access and where we can access it.
 It is crucial for determining the accessibility of variables and preventing conflict within variables.


### 2. Can you explain the difference between global scope and local scope?
Global scope refers to the context where variables, functions and objects are accessible from anywhere in your code. When a variables is decalred outside of any
finction or block, it is said to be in the global scope.

Local scope refers to where variables are declared within a function or block.

### 3.How does JavaScript handle scope in functions compared to block-level scope?
In fucntions, visibility ans accessibility of variables are within a function. So when a vriable is declred within a function it is only accessible within that function
and any nested functions.

The scope of varibales and functions are defined within a block of code such as a pair of curly braces. 

### 4. How do var, let, and const differ in terms of scope?he 
Let and const are block scope meaning they are only accessible within the block they are defined in but when they are declared outside any function or block, they 
behave as global variables.

Var is a fuction scope but when declared outside any function, it is also declared as a global variable.

### 5. What are the implications of declaring a variable without any keyword (i.e., no var, let, or const)?
Variables created without a const, let or var are always globally scoped. This can make your debugging process more complex.
### 6. What is the scope chain, and how does JavaScript use it to resolve variable access?
In JavaScript, the scope chain is like a series of nested boxes. Each box represents a scope, which is where variables are defined and can be accessed. When you try to use a variable, JavaScript first checks the innermost box (the current scope) to see if it's there. If not, it moves to the next outer box (the next scope out) and checks there. This process continues outward until it either finds the variable or reaches the outermost box (the global scope).

This chain helps JavaScript figure out which variable you're referring to based on where you're asking for it in your code. It ensures that functions can use variables from the places where they were defined, even if those places are outside the function itself. This way, your code stays organized, and variables are kept separate when they need to be, preventing mix-ups and making sure everything works smoothly together.

### 7. What are some differences between lexical scope and dynamic scope? Which one does JavaScript use?
Lexical Scope: This approach, used by JavaScript and many other modern languages, determines the scope of a variable based on where it is written in the code. When a function is defined, it captures the variables from its surrounding scope, forming a lexical environment. This means inner functions can access variables from their outer functions or global scope based on their nesting in the code. Lexical scope provides clarity and predictability, as variable access is determined statically, at the time of code writing.

Dynamic Scope: Unlike lexical scope, dynamic scope determines variable access based on the call stack at runtime. This means a function can access variables from wherever it was called, rather than where it was defined. Dynamic scope can lead to more flexible but potentially confusing code behavior, as variables can change based on the context of function calls during program execution.

JavaScript uses lexical scope, which helps developers write more maintainable and understandable code by clearly defining where variables are accessible based on their location in the code hierarchy. This ensures that variables are accessed predictably and avoids unexpected changes in variable values due to runtime call contexts, which dynamic scope might introduce.


### 8. What is a closure, and how does it relate to scope in JavaScript?

A closure in JavaScript refers to the combination of a function and the environment in which it was declared. It allows the function to access variables from its outer scope even after the outer function has finished executing. Essentially, a closure gives the inner function persistent access to the outer function's scope. This feature is particularly useful for maintaining state across multiple function calls or for creating private variables that are not accessible from outside the function. Closures are a powerful concept in JavaScript, enabling developers to write more modular and encapsulated code by controlling variable access and ensuring data integrity.