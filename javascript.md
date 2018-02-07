# Notes

Tight coupling is a phrase that developers use to indicate code that is too dependent on the details of each other. The word "coupling" means the "pairing of two items together." In tight coupling, pieces of code are joined together in a way where changing one unintentionally alters the functioning of some other code:

In JavaScript, functions are first-class functions. This means that you can do with a function just about anything that you can do with other elements, such as numbers, strings, objects, arrays, etc. JavaScript functions can:

A function that returns another function is known as higher-order function

JavaScript manages memory with automatic garbage collection. This means that when data is no longer referable (i.e., there are no remaining references to that data available for executable code), it is "garbage collected" and will be destroyed at some later point in time.

### Applications of Closures

A closure refers to the combination of a function and the lexical environment in which that function was declared. Every time a function is defined, closure is created for that function. This is especially especially powerful in situations where a function is defined within another function, allowing the nested function to access variables outside of it. Functions also keep a link to its parent's scope even if the parent has returned. This prevents data in its parents from being garbage collected.

* Passing arguments implicitly.
* At function declaration, storing a snapshot of scope.

### IIFE

One of the primary uses for IIFE's is to create private scope (i.e., private state). Recall that variables in JavaScript are traditionally scoped to a function. Knowing this, we can leverage the behavior of closures to protect variables or methods from being accessed! Consider the following example of a simple closure within an IIFE, referenced by myFunction:

IIFE's ultimately use the returned functions to access private data within the closure. This works out very well: while these returned functions are publicly-accessible, they still maintain privacy for the variables defined within them!

Another great opportunity to use an IFFE is when you want to execute some code without creating extra global variables. However, note that an IIFE is only intended to be invoked once, to create a unique execution context. If you have some code that is expected to be re-used (e.g., a function meant to be executed more than once in the application), declaring the function and then invoking it might be a better option.

All in all, if you simply have a one-time task (e.g., initializing an application), an IIFE is a great way to get something done without polluting your the global environment with extra variables. Cleaning up the global namespace decreases the chance of collisions with duplicate variable names, after all.

### class

instanceOf confirmed that a specific constructor function did in fact create a specific object. We know this because we directly instantiated the dev object after invoking the Developer() constructor function.

call() is a method directly invoked onto a function. We first pass into it in a single value to set as the value of this; then we pass in any of the receiving function's arguments one-by-one, separated by commas.
