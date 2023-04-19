# Lecture 10: Software Testing
## 2/20/23

Remember: 
- __internal quality__: developer-facing quality 
- __external quality__: customer-facing quality

## Testing a Python list
If we were to try and create tests for a list in python, what might we test?
- Does it append correctly?
    - after appending, does the rest of the list stay the same?
- Does it "pop" correctly?
    - after popping, does the length of the list change?
    - after popping, what happens when we try to access the most recently removed iten?
- This can get complicated really quick

# Software Testing
__Def__: an investigation conducted to provide stakeholders with information about the quality of the software produt or service under review.
- typically, tests involve input data and comparisons with output data
- testing gives you confidence that your implementation adheres to your specification

## Testing in Project 1
- compared provided program's output to expected output
    - by running the program with provided inputs
    - **oracle**: gives us the right answer to a given input


# Types of Software Testing
- __Regression Testing__: test for regressions in source code
    - "I swear I saw this and fixed this before"
    - When a developer fixes a bug, they also add a __regression test__ that specifically exposes the bug
    - This ensures that future implementations still fix this bug
- __System Testing__: test an end-to-end system for correctness
- __Unit Testing__: test individual chunks (units!) of source code to determine that they work
    - unit: function, module, class, etc.


# Unit Testing
- Unit tests are very common
- As such, unit test frameworks are very common 
    - Junit (Java), unittest (python), etc.
    - Unit tests look like other code
    - Provides special functions/methods to return a boolean or certain failure assertions

- Test case **discoverer**: finds all these unit tests in the code (based on a special naming scheme)
- Test case **runner**: chooses which tests to execute
- **Test case**
    - perform the following in isolation:
    1. Establish some precondition
    2. Perform an operation
    3. Assert postconditions
- **Test fixture**: surrounds a test case to provide code that is run before and after each test case
    - often used for set up (before) and clean up (after)