# Lecture 10: Software Testing
### 2/20/23

## Overview
This lecture contains information about how we might go about assessing the internal and external quality of a piece of software through software testing

---

## Software Testing

> #### Definition
> __internal quality__ is developer-facing quality

> #### Definition
> __external quality__ is customer-facing quality

## Testing a Python list
If we were to try and create tests for a list in python, what might we test?
- Does it append correctly?
    - After appending, does the rest of the list stay the same?
- Does it "pop" correctly?
    - After popping, does the length of the list change?
    - After popping, what happens when we try to access the most recently removed item?
- This can get complicated really quick.

> #### Definition
> __Software testing__ is an investigation conducted to provide stakeholders with information about the quality of the software product or service under review


- Typically, tests involve input data and comparisons with output data.
- Testing gives you confidence that your implementation adheres to your specification.

## Testing in Project 1
- We compared provided program's output to expected output.
    - Did this by running the program with provided inputs.

> #### Definition
> an __oracle__ gives us the right answer to a given input

---

## Types of Software Testing
In this lecture, we will discuss regression testing, system testing, and unit testing.

---

## Regression Testing

Testing for regressions in the source code.
> #### Definition
> A __regression test__ is a test that exposes a particular bug, and is used to ensure that future implementations of the software still fix this bug

- "I swear I saw this and fixed this before"
- When a developer fixes a bug, they can add a regression test that exposes this bug to make sure it stays fixed.

---

## System Testing

> #### Definition
> Testing an end-to-end system for correctness is called __system testing__

---

## Unit Testing

> #### Definition
> testing individual chunks of source code to determine that they work is called __unit testing__
- A unit might be a function, module, class, etc.
- Unit tests are very common.
- As such, unit test frameworks are very common.
    - Junit (Java), unittest (python), etc.
    - Unit tests look like other code.
    - Provides special functions/methods to return a boolean or certain failure assertions.

> #### Definition
> a test case __discoverer__ finds all unit tests in the code based on a special naming scheme

> #### Definition
> a test case __runner__ chooses which tests to execute

> #### Definition
> A __test case__ performs three operations in isolation: (1) establish some precondition, (2) perform an operation, (3) assert postconditions

> #### Definition
> A __test fixture__ surrounds a test case to provide code that is run before and after each test case

- Test fixtures are often used for set up (before) and clean up (after).