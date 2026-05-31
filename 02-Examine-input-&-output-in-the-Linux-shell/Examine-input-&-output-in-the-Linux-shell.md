# Google Cybersecurity Certificate - Lab 2: Examine input & output in Linux Shell

## Introduction
In this lab, I explored the fundamentals of the Linux command-line interface (CLI). Understanding how to navigate the shell, manipulate text, and perform basic operations is a critical foundational skill for cybersecurity analysts, as many security tools and server environments rely entirely on the CLI.

---

## Task 1: Using the `echo` Command
The `echo` command is used to print text arguments to the terminal. I practiced different ways to input string data.

### Basic Echo
First, I used `echo` without quotes to print a simple string.
![Using echo without quotes](<img width="882" height="92" alt="Image" src="https://github.com/user-attachments/assets/53389e1a-46ef-4eba-a3c4-7fc5b3159aa1" />)

### Echo with Quotes
Next, I used quotes around the text. While both methods work for simple text, using quotes is a best practice in Linux to ensure spaces and special characters are handled correctly.
![Using echo with quotes](<img width="883" height="73" alt="Image" src="https://github.com/user-attachments/assets/0d64cc53-0203-4a0f-a49e-64299942c723" />)

### Custom Text & Personalization
I then practiced passing specific strings, including my own name, into the command.
![Using echo with placeholder text](<img width="881" height="75" alt="Image" src="https://github.com/user-attachments/assets/1f633ea5-8f3e-4aa0-8fc7-5668f06d961d" />)
![Using echo with my name](<img width="883" height="75" alt="Image" src="https://github.com/user-attachments/assets/88a3c430-6c1f-46b8-ab99-fc393ebc546a" />)

> **💡 Pro Tip:** Get into the habit of always using double quotes `""` with `echo`. If you ever need to use environment variables (like `echo "Current user: $USER"`), double quotes will allow the shell to expand the variable, whereas single quotes `''` will print it literally as `$USER`.

---

## Task 2: Performing Calculations with `expr`
The `expr` (expression) command allows the shell to evaluate expressions, including basic math. 

### Syntax Requirements (My Key Learning Moment)
During this task, I learned that `expr` is highly sensitive to spacing. My first attempt failed because I did not include spaces between the numbers and the operator. Once I corrected the spacing, the calculation worked perfectly.
![Failed vs Successful Subtraction with expr](<img width="881" height="121" alt="Image" src="https://github.com/user-attachments/assets/a3381f4e-3927-4874-8c20-6ecaa633b5ec" />)

### Multiplication in `expr`
I also practiced multiplication. 
![Multiplication with expr](<img width="883" height="76" alt="Image" src="https://github.com/user-attachments/assets/1fd7bb7c-5229-4521-ac53-e8cfb1eb9d0d" />)

> **💡 Pro Tip:** When multiplying with `expr`, you must use a backslash before the asterisk (`\*`). In Linux, the asterisk `*` is a wildcard character. The backslash "escapes" it, telling the shell to treat it as a multiplication sign instead of a wildcard. 
> * Correct: `expr 5 \* 4`
> * Incorrect: `expr 5 * 4`

---

## Task 3: Managing the Terminal Screen
As a session goes on, the terminal can become cluttered with old commands, making it hard to focus.

### Before Clearing
Here is my cluttered terminal screen right before executing the `clear` command.
![Cluttered terminal with clear command typed](<img width="882" height="350" alt="Image" src="https://github.com/user-attachments/assets/821328eb-ae83-423c-ab3c-22a289bb14cf" />)

### After Clearing
After hitting `Enter`, the terminal screen reset, providing a clean workspace. Note that this doesn't erase your history; it just scrolls the old output out of view.
![Clean terminal screen](<img width="882" height="138" alt="Image" src="https://github.com/user-attachments/assets/8bc26260-f6ce-4092-90e2-27d7f2a54100" />)

> **💡 Pro Tip:** Instead of typing out `clear` every time, you can use the keyboard shortcut **`Ctrl + L`**. It instantly clears the screen without you needing to type a thing.

---

## Task 4: Independent Practice & Synthesis
To solidify my learning, I ran through a comprehensive review phase. I combined everything I learned into a single session, executing an `echo` statement followed by a full suite of arithmetic operations (addition, subtraction, multiplication, and division).

![Comprehensive review of echo and math operations](<img width="882" height="278" alt="Image" src="https://github.com/user-attachments/assets/46e295c3-f64a-4138-8fe1-686442d481ec" />)

---

## Conclusion
This lab successfully demonstrated the basics of interacting with the Linux shell. Overcoming the syntax error with `expr` taught me the importance of precision in command-line environments—a mindset that is essential when configuring security controls or analyzing logs.
