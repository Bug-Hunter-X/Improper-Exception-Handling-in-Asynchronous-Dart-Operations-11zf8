# Improper Exception Handling in Asynchronous Dart Operations

This repository demonstrates a common error in Dart: improper exception handling in asynchronous operations using `async` and `await`. The initial code lacks proper re-throwing of exceptions, resulting in silent failures.  The solution demonstrates the proper use of `rethrow` to propagate errors effectively. 

## Bug
The `bug.dart` file showcases the flawed exception handling.  The `fetchData` function handles the HTTP request and catches exceptions; however, it fails to propagate them up the call stack.  This means that an error will be printed to the console, but the program will continue to run, potentially leading to unexpected behaviour elsewhere.

## Solution
The `bugSolution.dart` file provides the corrected version of `fetchData`, incorporating `rethrow`.  This ensures exceptions are properly propagated, allowing for more robust error management within the application.