# Unhandled Exceptions in Asynchronous Dart Code

This repository demonstrates a common error in Dart's asynchronous programming: silently swallowing exceptions in `async` functions.  The `bug.dart` file shows the problematic code, while `bugSolution.dart` provides the corrected version.

The error occurs when an exception is caught but not properly handled, often leading to unexpected behavior.  The solution involves using `rethrow` to propagate the exception to the calling function where it can be handled appropriately.

## How to Reproduce
1. Clone this repository.
2. Run `bug.dart` and observe the lack of error output, even on a network failure.
3. Run `bugSolution.dart` and observe proper error handling and informative output.