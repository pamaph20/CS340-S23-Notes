# February 22, 2023 
## _New Testing Metrics_
### Objective: Today we learn about different kinds of testing metrics that we can use to ensure the best quality.
***
Review from last class:
+ **Unit Testing** is when you test  indivual chunks of source code to determine that it works in isolation from the rest of the program. Some adavntages of this testing metric is as follows:
* since it is in small chunks it's easier to understand what is going on in that specfic section.
* we test features in isolation so it can be easier to locate a bug.
+ because it is small testing becomes faster.

*** 
+ building on this idea, we can begin to discuss something called: **Test Driven Development**
**Test Driven Development** is when you write the test file before you even write the new feature. Which works great in conversation with unit testing. For example:
+ Write a unit test for a new feature 
    + _your test will fail at this point
+ write code that the unit test are testing for 
+ run all available unit test 
    + fix any regressions 

+ **Now**, after all this can you go back and add a new feature.

***

* While Unit Testing is great, it fails when trying to see the "big picture". 
    + What happens when we combine unit tested features into a larger program?
* This is where **Integration Testing** comes in...
    + **Integration Testing** is one step ahead of unit testing because individual software modules are combined and tested as a group

    + This is a perfect segue to our next metric of testing: **System Testing**.
    + **System Testing** is end to end integration testing. We evaluate how the various components of an application interact together in the full, integrated system or application. 
+ Another kind of testing that caluates how does a system preform under typical resource usage is **Load Testing**
    + (typical users, request/hour, etc...)
+ Going one step further, **Stress Testing** is to see how far we can push a program until it breaks _(hehe)_.

*** 
_What are some challenges of testing? How do we work around them?_
+ different hardware configurations
    - what if the tool is broken?
        - what if the _test_ is broken?
- cost/speed (external APIs)
    - **Mocking** is a common tool in software engineering when it comes to this challenge. Mocking is used to simulate objects that mimic the behavior of real objects in a controlled way. 
        + i.e. crash dummies
    - In software, thesr mock objects are sometimes also called **stubs**. 
        - bits of code with some interdace as the real code but return dummy data

#### **Example 1**
+ Web app that uses chat bot for interactions
    - API could still be under development or cost per quary
        - write stubs that return hardcoded results

#### **Example 2**
+ Code where certain kinds of failures might happen sporadically (disk full, condition dropped, corruption)
    + errors " don't happen" in development
        + use testing frameworks/mocking frameworks that can trigger these transcient errors

***
+ This brings us to our new topic: **_Quality of Test and Test Suite_**
+ "Testing Quality Assurance accounts for 25-35% of IT budgets _(2015 -2019)_" - KA

+ If testing is the best way to gain confidence but is expensive, how do we ensure that we are testing in a efficent manner?

+ _Till Next time.._

# February 22, 2023 
## _New Testing Metrics_
### Objective: Today we learn about different kinds of testing metrics that we can use to ensure the best quality.
***
Review from last class:
+ **Unit Testing** is when you test  indivual chunks of source code to determine that it works in isolation from the rest of the program. Some adavntages of this testing metric is as follows:
* since it is in small chunks it's easier to understand what is going on in that specfic section.
* we test features in isolation so it can be easier to locate a bug.
+ because it is small testing becomes faster.

*** 
+ building on this idea, we can begin to discuss something called: **Test Driven Development**
**Test Driven Development** is when you write the test file before you even write the new feature. Which works great in conversation with unit testing. For example:
+ Write a unit test for a new feature 
    + _your test will fail at this point
+ write code that the unit test are testing for 
+ run all available unit test 
    + fix any regressions 

+ **Now**, after all this can you go back and add a new feature.

***

* While Unit Testing is great, it fails when trying to see the "big picture". 
    + What happens when we combine unit tested features into a larger program?
* This is where **Integration Testing** comes in...
    + **Integration Testing** is one step ahead of unit testing because individual software modules are combined and tested as a group

    + This is a perfect segue to our next metric of testing: **System Testing**.
    + **System Testing** is end to end integration testing. We evaluate how the various components of an application interact together in the full, integrated system or application. 
+ Another kind of testing that caluates how does a system preform under typical resource usage is **Load Testing**
    + (typical users, request/hour, etc...)
+ Going one step further, **Stress Testing** is to see how far we can push a program until it breaks _(hehe)_.

*** 
_What are some challenges of testing? How do we work around them?_
+ different hardware configurations
    - what if the tool is broken?
        - what if the _test_ is broken?
- cost/speed (external APIs)
    - **Mocking** is a common tool in software engineering when it comes to this challenge. Mocking is used to simulate objects that mimic the behavior of real objects in a controlled way. 
        + i.e. crash dummies
    - In software, thesr mock objects are sometimes also called **stubs**. 
        - bits of code with some interdace as the real code but return dummy data

#### **Example 1**
+ Web app that uses chat bot for interactions
    - API could still be under development or cost per quary
        - write stubs that return hardcoded results

#### **Example 2**
+ Code where certain kinds of failures might happen sporadically (disk full, condition dropped, corruption)
    + errors " don't happen" in development
        + use testing frameworks/mocking frameworks that can trigger these transcient errors

***
+ This brings us to our new topic: **_Quality of Test and Test Suite_**
+ "Testing Quality Assurance accounts for 25-35% of IT budgets _(2015 -2019)_" - KA

+ If testing is the best way to gain confidence but is expensive, how do we ensure that we are testing in a efficent manner?

+ _Till Next time..