#Thread of Execution & the Call Stack

	- [x] JavaScript is a single-threaded language.
	- [x] Single sequential flow of control.
	- [x] JavaScript is a synchromous language with asynchronous capabilities.
	- [x] A thread has a call stack and memory.

					THREAD OF EXECUTION
							|
							|
						Operation 1    { console.log(1); }
							|
							|
						Operation 2    { console.log(2); }
							|
							|
						Operation 3    { console.log(3); }
							|
							|
				Call Stack 		Memory Help



# CALL STACK:

	- [x] Stack of functions to be executed.
	- [x] Manages execution contexts.
	- [x] Stacks are LIFO { last in first out }.


# EXECUTION CONTEXT:

	When we run any JavaScript, a special enviroment is created to handle the transformation & execution of code. This is called Execution context.
	It contains the currently running code and everything that aids in its execution

	There is a global execution context as well as a function execution context for every function invoked.

#Execution Context Phases

## Memory Creation Phase:

	1. Create the global object ( browser = window, Node.js = global).
	1. Create the 'this' object and bind it to the global object.
	1. Setup memory heap for storing variables and function references.
	1. Store functions and variables in global execution context and set to "undefined".

## Execution Phase:
	1. Execute code line by line.
	1. Create a new execution context for each function call.
	

# Hoisting:
	
	Hoisting is often referred to as the process where the interpreter appears to **move the declaration of functions and variables** to the top of their scope prior to the execution of the code.

	This is a pretty elementary explanation of hoisting. Now that you understand the global execution context **creation phase**, you can understand how hoisting works


# Memory Management
	
	Low-level languages like C and C++ require you to allocate and free up memory manually. This is makes them much more difficult to work with.

	Higher level languages like JavaScript, Python and C# automatically allocated memory when objects are created and frees it when they are not used anymore.

	This process is called garbage collection.


# Data Types
	
## Primitive Types

	Stored directly in the 'stack', where it is accessed from
		string | number | Boolean | Null | Undefined | BigInt

## Reference Types

	Stored in the heap and accessed by reference
		Arrays | Functions | Objects


# JS Engine

	- [x] Software component that executes JavaScript code.
	- [x] The first engines were simple interpreters, but modern engines are also responsible fot optimizations, such as JIT ( Just In Time ) compilation.
	- [x] Each browser uses a specific JavaScript engine.


# Compiling vs Interpreting

	- [x] Compiled languages are compiled directly to machine code all at once.
	- [x] Interpreted languages are interpreted line by line.
	- [x] Combined languages have a slow write-time and fast run-time and interpreted languages have the opposite.

