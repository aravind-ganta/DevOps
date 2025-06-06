### Environment Variables
* Environment variables are KEY=value pairs
* These variables are available system-wide
* Variables store information, which can be changed
* By convention, names are defined in UPPER CASE
* Allow you to customize how the system works and the behavior of the applications on the system

* There are 2 use cases for environment variables
#### OS stores information about the environment
* When you have multiple users on a computer, each user can configure its own environment/account by setting preferences
* OS stores all these configurations in environment variables
* Some examples:
    1. Default shell program of the user
    2. Current user's home directory
    3. Currently logged in user
#### Create our own environment variables
#### Use Case: Sensitive data for application
* If application needs some credentials, it's not secure to hardcode it directly in the source code
* Set these data as env vars on server
* By creating these env vars, we make them available in
the environment
* All apps and processes can now access these env vars
#### Use Case: Make application more flexible
* If your application connects to a database, you need different credentials for different dev, test and prod environments
* So you should not hardcode these values in the source code
* Instead one option is to set the different values as env vars on each server
* Now no need to change the application code, as the values are dynamically set

#### Set environment variables
* The export command is used to set
environment variables
> export MY_VAR="myvalue"
* Env vars created in this way are available only in the current session. If you open a new shell or if you log out all variables will be lost!

#### Display environment variables
* Print environment variable in terminal
> printenv MY_VAR

#### Persisting environment variables
* To make env vars persistent you need to define those variables in a shell configuration files
* These are shell specific configuration files
* E.g. if you are using bash, you can declare the variables in the ~/.bashrc file
* Variables set in this file are loaded whenever a bash login shell is entered
* source ~/.bashrc: To load the new env vars into the current shell session
* Shell config files are user specific
Set system-wide env vars in /etc/environment file

### PATH
* PATH is a environment variable
* Its value includes a list of directories to executable files, separated by :
* Tells the shell which directories to search for the executable in response to our
executed command
* When you run a command, the system will search those directories in this order and use the first found executable
* Example value:
> PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
