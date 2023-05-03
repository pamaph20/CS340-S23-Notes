##  Lecture 17

#  3/15/2023

****How do we make software work with partially implemented features?****

 - Why is this a problem we need to solve?
         - CI/CD + big feature
 - Possible Soutions:
         - Not release version (break CI/CD)
         - No way to access the feature
 - Decided upon solution:
         - Write code that doesn't break build
         - Slowly code it up with things that work
         - Hide it from user until finished
***
**Control flow graphs**



    def foo(a,b,c,d,e,f):
    if a < b:
            This
        else:
                That
        if c < d:
                Ed
        else:
                Lisa
        if e < f:
                CS
        else:
                DS
![Control Flow Graph Diagram](https://lucid.app/documents/view/c24df2e7-6935-4313-bc04-faddc4528b9a)

 - 6 branches
 - 2 tests needed for branch coverage
         - foo(1,2,3,4,5,6)
         - foo(6,5,4,3,2,1)
 - Path coverage is more strict than branch coverage, If thre are n sequential (serial) if statements:
         - 2n branch edges
    -  2 tests to cover branches
    -  2^n tests to cover paths
***
**Automated test generation to increase our coverage**

 - How do we check this output?
 >#### Oracle problem
>Difficulty and cost of determining the correct output and input
>
>### Implicit oracle
>don’t crash, terminate in n minues, don’t leak secrets

2 approaches - Think really hard and write down the tests or try random things and see what paths are covered

Thinking hard:
>### Path predicate
>A path predicate (path condition or path constraint) is a boolean formula over program variables that is true when the program executes a given path
>-   Ex: lets say we want the path False False True
>a >= b and c >=d and e < f
>We could assign the values:
    2, 1, 3, 2, 3, 4

Try random things and see what happens:
-   Directed automated random testing (DART)
        - Ex: Wolfram Mathematica
-   Fuzz testing - mutate a given input and see what happens

***
