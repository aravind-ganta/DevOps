### Introduction to Vi and Vim

#### What is it
* Vi and Vim are built-in text editors in Linux
* Vi is by far the most distributed and used text editor in Linux
* Vim (Vi IMproved) is improved version of Vi
* Built to make creating and changing any kind of text very efficient
* Depending on your Linux distro, Vim may or may not be installed

#### Use cases for using text editor in CLI
* Small modifications can be faster, especially when you are currently working in the CLI
* Faster to create and edit at the same time
* Supports multiple formats
* When working on a server
* Git CLI - writing the Git commit message
* Display Kubernetes configuration files
* Quickly editing one line or character in a file

* Vim has 2 modes:
    * Insert Mode
    * Command Mode

#### Command Mode:
* This is the default mode
* You can't edit the text
* Whatever you type is interpreted as a command
* Navigate, Search, Delete, Undo etc.

#### Insert Mode:
* Allows you to enter text
* Pressing Escape, switches you back to command mode

### Basic Linux Commands
* Every program has: Input and Output
* The output from one program can become the input of another command

#### "pipe" command: |
Pipes the output of the previous command as an input to the next command

#### "less"
* Displays the contents of a file or a command output, one page at a time
* Allows you to navigate forward and backward through the file
* Mostly used for opening large files, as less doesn't read the entire file, which results in faster load times

#### "grep"
* Searches for a particular pattern of characters and displays all lines that contain that pattern
* Example usage is to use the grep command in combination with pipe
> history | grep sudo

#### "redirect" operator: >
* Takes the output from the previous command and sends it to a file that you give

#### Standard Input and Output
* Every program has 3 built-in streams:
* Standard streams are streams of data that travel from where a program was executed, to the places where the program is processed and then back again




