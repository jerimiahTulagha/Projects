# Shell Scripting Implementation.

Shell scripting helps you automate repetitive tasks. we can simply write as script that does the job of cloning 1000 repositories, we call it ones the job is done. We have the advantage of using it whenever we are signed same task.

- Bash scripting are essentially a series of commands and instructions that are executed sequentially in a shell. You can save a shell script by saving a collection of command text in a files with .sh extention. This scirpt can be executed directly from the command line or called from other scripts.

## Variables 
- Bash allows you to to define and work with variables. Variables can store data of various types such as numbers,strings and arrays. You can assign values to variables using the = operator, and access their values using the variable name preceded by a $ sign.

### Assigning value to a variable.
name="jay"
now to call name,

echo $name

![name](./img/01.%20name.png)

## Control flow
Bash provides control flow statements like if-else, for loop, while loop, and case statement to control the flow of execution  in your script. These statements allow you make decisions, iterates over lists and execute different commands based on conditions.

![if-else](./img/0.2%20iteration.png)

## Command substitution.
Allows you to capture the output of a command and use it as value within your script.

Using backstick or $()syntax for command substitution.

![command](./img/03.%20current-date.png)

## Input and Output.
Bash provides various ways to handle input and output. You can use the read command to accept user input, and output text to the console using the echo command.

![input-Output](./img/0.4%20hello-world.png)

## Functions
Bash allows you to define and use functions to group related commands together. Functions provides a way to modularize your code and make it more reusable. You can define functions using the function keyword or simply declaring the function name followed by parenthesis.

![functions](./img/0.5%20Define.png)

## First shell scripting.
Creating a directory where all our files will be stored, then creating a file where we'll write our .sh script and execute.

![first-script](./img/0.6%20first-execution.png)

## Directory manipulation and navigation.
This script will display the current directory we created called my-directory, where all our files will be stored, then a file as well called navigating-linix-filesystem.sh.

![directory-manipulation](./img/0.7%20Directory-manipulation.png)


## File operation and sorting
Here we will be writing a simple shell script that focuses on file operations and sorting.

![sorting](./img/0.8%20sorting.png)

## Working with numbers and calculations.

This script defines two variables num1 and num2 with numeric value,perform basic aritmethic operations (addition,subtraction,multiplication,division and modulus), and displays the results.

![calculation](./img/0.9%20calculations.png)

## File backup and timestamping.
This shell scripting is focused on file backup and timestampting. it is important to backup our database and other storage devices.

![backup](./img/10.%20backup.png)