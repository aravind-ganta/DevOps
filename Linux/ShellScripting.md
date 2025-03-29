### Why Shell Scripting?
* When administering servers, you
need to execute tons of commands
* Instead of executing the command one by one, you can save the
commands in a file and execute that file
* Such file is called a shell script
* File extension is .sh
* Automate all your work:
    * Backup Scripts
    * Monitoring Scripts
    * Server Configuration Scripts
#### Uses
* Avoid repetitive work
* Keep history of configuration
* Share the instructions
* Logic & Bulk Operations

### How to execute Shell Scripts
#### Shell
* The program that interprets and executes the various commands that
we type in the terminal
* Translates our command that the OS Kernel can understand

#### Different Shell implementations
#### sh
* Bourne Shell - /bin/sh
#### Bash
* Bourne again shell - /bin/bash
* Improved version of sh
* Default shell program for most UNIX like systems
* Bash is a shell program and a programming language

* Shell and Bash terms are often used interchangeable
* All shell script files have the same .sh file extension

#### How OS knows which shell to use
```
#!/bin/sh
#!/bin/bash
#!/bin/zsh
```
* This is called "shebang"
#### Why?
* Because of the first 2 characters "#!"
* \# = in musical notation, also called "sharp"
* ! = also called "bang"
* Shebang became a shortening of sharp-bang

#### Make shell script executable
* To execute a shell script, you need to make it executable first, by adding executing permission

### Writing Shell Scripts
#### Variables
* Used to store data and can be referenced later
* Similar to variables in general programming languages
* Store output of a command in a variable: variable_name=$(command)

#### Conditionals
* Allow you to alter the control flow of the program 
* E.g. execute a command only when a certain condition is true

#### [ ... ] builtin command
* Square brackets enclose expressions
* It's a shorthand notation for the "test" command
    * if test -d "config" is the same

#### Boolean
* A datatype that can only have 2 values:
    * True
    * False
* Bash does have Boolean expressions in terms of comparison and conditions

#### File Test Operators
* Test various properties associated with a file

#### Relational Operators
* Works only for numeric values

#### String Operators
* Test strings for equality and more

#### Passing arguments to a script
* You can pass arguments when executing a script
* We can read these passed parameters using special variables

#### Positional Parameters
* Arguments passed to script are processed in the same order in which they're sent
* The indexing of arguments starts at 1: $1
* $*= represent all the arguments as a single string
* $#= Total number of arguments provided

#### Loops
* Enables you to execute a set of commands repeatedly
* There are different types of loops:
    * while loop
    * for loop
    * until loop
    * select loop
#### For Loop
* Operates on lists of items
* Repeats a set of commands for every item in the list
#### While Loop
* Executes a set of commands repeatedly until some condition is matched

#### Functions
* Enables you to break down the overall functionality of a script into smaller, logical code blocks
* This code block can then be referenced ("called")
anywhere in the script multiple times
* You can accept parameters in a function
* The parameters passed in are represented by $1, $2, et

#### Best Practices
* Don't use too many parameters
* Apply the Single Responsibility Principle:
A function should only do one thing
* Declare variables with a meaningful name for positional parameters within a function



