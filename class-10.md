# Debugging

<!-- from JavScript&JQuery by Jon Duckett -->
## Error Handling and Debugging

knowing the order of execution is an important step in finding the source of an error, as some tasks cannot be completed until other tasks have run.

the JavaScript interpreter uses execution contexts. There is one global execution context and functions each create a new execution contexts, each of these correspond with variable scope.

the interprester processes one line of code at a time, and when a statement needs data from another function, it stacks on top of the current task.

Whenever a new script enters the execution context, there are two phases of activity

- prepare - the new scope, variables, arguments, and functions are created
- execute - it can assign values to variables, reference functions, run their code, and execute statements

each execution context had its own variables and can access its parents variables.

if a statement generates an error, it throws an exception an the interpreter stops to look for exception handling code, so if you are expecting there to be an issue, you can create a series of statements to handle errors and inform the user what went wrong. Error objects can help you find where your mistakes are and the browser will let you read them. The different error types are:

- error - generic error
- SyntaxError - syntax has not been followed
- ReferenceError - tried to reference a variable that has not been declared
- TypeError - an unexpected data type
- RangeError - numbers not in an acceptable range
- URLError - URL methods used incorrectly
- EvalError - eval() used incorrectly

to deal with errors you can either debug the script to fix them or handle them gracefully for things you cannot control.

debugging is about deduction to eliminate potential causes of error.

- where is the problem?
- what exactly is the problem?

you can pause the execution of a script using breakpoints and check the values stored in variables at that exact point or you could set multiple breakpoints and step through your code to see where a problem is occurring. You can also create a breakpoint in the code itself using `debugger`.

if you know your code might fail you can use try catch finally, or you can throw an error yorself before the interpretor creates them using `throw new Error('message')`.

- try - specify the code you think might fail with a `try` block
- catch - if the try block throws an exception, catch steps in with an alternative set of code
- finally - the contents of finally will run whether try fails or succeeds

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
