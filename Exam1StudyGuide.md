# Exam 1 Study Guide
## For exam on 01/03/2023

## Topics
- Software vs. programs
- Time allocation to various SE tasks
- Linux / command line
    - typlica program / commands
    - loops / conditions
    - file path (basename & dirname commands)
    - scripting (shabang / permissions)
    - text editors (nano and vim)
- Version Control Systems
    - centralized vs. distributed
    - deltas vs. snapshots
    - get basics -> staging & working directory
    - commit histories
    - branching, tags, head
    - rebase, merge
    - remote / pull requests / forks
    - commit messages best practices
- Quality Assurance & Testing
    - internal vs. external quality
    - rice's theorem & limits of assesment 
    - unit, system, integration, and load testing
    - test driven development
    - test cases 
    - mocking

## Notes

_Software vs. Programs_

- program: collect of instructions or ordered operations for a computer to preform a function or task
- software: collection of programs procedures, data, or instructions that work together to provide a specified functionality
- Similarities and differences:
    - similarities: programming languages, coding
    - differences: public, size, security, usability, quality control

_Time allocation to various SE tasks_

- 70 - 90% of the budget / time is spent on maintenance

_Linux / command line_
- _typlica program / commands_
- _loops / conditions_
- _file path (basename & dirname commands)_
- _scripting (shabang / permissions)_
- _text editors (nano and vim)_


- Command lines give access to run tools under the hood
- Shell is a program that exposes an OS' services to a human user or other programs
- A shell script is a text file containing commands for a shell to execute
    - The first line starts with a "shabang" or "#!/bin/bash"
- Useful commands:
    - chmod: a command to change permissions
        - chmod +x \<file>: is used to make a file executable
    - ls: list the content in a directory
    - pwd: present working direcotry
    - cd: change directory
    - curl: transfer from URL
    - mkdir: make directory
    - less: open file
    - man: help manual
    - ssh: secure shell, allows remote acces to shell on another computer
    - basename: extracts only the file name
    - dirname: extracts only the file path
    - "|" (pipe): take output from one program as input to a second program
    - xargs: popes but as command line arguments
    - cut: delimiter to break up lines
    - wc: word count

- For loop: 
```
for i in {0..100}
    do
    ...
    done
```
- Conditionals:
```
if [-f name]
    then
        ...
    else
        ...
fi
```
    - f is used for files
    - d is used for directories
    - z is to check for empty fiels

- Redirecting
    - \>: overwriting the target file
    - \>>: appends to the target file
    - 2>: sends the error output
    - 1>: sends the standard output

- Text editors: nano, vi(m), emacs
    - vi commands:
        - i; insert mode
        - :q! force quit, no ! for quit
        - :w write the file
        - \<escape> leave insert mode



## Curent progress level


- Version Control Systems
    - centralized vs. distributed
    - deltas vs. snapshots
    - get basics -> staging & working directory
    - commit histories
    - branching, tags, head
    - rebase, merge
    - remote / pull requests / forks
    - commit messages best practices
- Quality Assurance & Testing
    - internal vs. external quality
    - rice's theorem & limits of assesment 
    - unit, system, integration, and load testing
    - test driven development
    - test cases 
    - mocking