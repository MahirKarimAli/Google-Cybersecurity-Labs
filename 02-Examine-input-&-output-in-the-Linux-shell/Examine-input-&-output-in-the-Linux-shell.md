# Google Cybersecurity Certificate - Lab 2: Examine input & output in Linux Shell

## Introduction
In this lab, I explored the fundamentals of the Linux command-line interface (CLI). Understanding how to navigate the shell, manipulate text, and perform basic operations is a critical foundational skill for cybersecurity analysts, as many security tools and server environments rely entirely on the CLI.

---

## Task 1: Using the `echo` Command
The `echo` command is used to print text arguments to the terminal. I practiced different ways to input string data.

### Basic Echo
First, I used `echo` without quotes to print a simple string.
![Using echo without quotes](<img width="882" height="92" alt="ss1" src="https://github.com/user-attachments/assets/e45ad1e3-e839-48e4-af40-c2662dc548d0" />
)

### Echo with Quotes
Next, I used quotes around the text. While both methods work for simple text, using quotes is a best practice in Linux to ensure spaces and special characters are handled correctly.
![Using echo with quotes](<img width="883" height="73" alt="ss2" src="https://github.com/user-attachments/assets/65a60058-2517-46b5-a75e-9c8b1e22e1f5" />)

### Custom Text & Personalization
I then practiced passing specific strings, including my own name, into the command.
![Using echo with placeholder text](<img width="881" height="75" alt="ss3" src="https://github.com/user-attachments/assets/c0a76345-0bde-4c9f-b315-0e77bbd64ed8" />)
![Using echo with my name](<img width="883" height="75" alt="ss4" src="https://github.com/user-attachments/assets/11e9b620-4d57-4cd0-be4c-d9226bcafb7a" />)

---

## Task 2: Performing Calculations with `expr`
The `expr` (expression) command allows the shell to evaluate expressions, including basic math. 

### Syntax Requirements (My Key Learning Moment)
During this task, I learned that `expr` is highly sensitive to spacing. My first attempt failed because I did not include spaces between the numbers and the operator. Once I corrected the spacing, the calculation worked perfectly.
![Failed vs Successful Subtraction with expr](<img width="881" height="121" alt="ss5" src="https://github.com/user-attachments/assets/43da4932-31bf-4eb4-aeae-3b3a08a6c2b0" />)

### Multiplication in `expr`
I also practiced multiplication. 
![Multiplication with expr](<img width="883" height="76" alt="ss6" src="https://github.com/user-attachments/assets/57fe41b2-3990-4f17-b484-87cc0586bd9a" />)

---

## Task 3: Managing the Terminal Screen
As a session goes on, the terminal can become cluttered with old commands, making it hard to focus.

### Before Clearing
Here is my cluttered terminal screen right before executing the `clear` command.
![Cluttered terminal with clear command typed](<img width="882" height="350" alt="ss7" src="https://github.com/user-attachments/assets/bb1f8a0e-6ddc-4eaf-b68c-991a52160b4a" />)

### After Clearing
After hitting `Enter`, the terminal screen reset, providing a clean workspace. Note that this doesn't erase your history; it just scrolls the old output out of view.
![Clean terminal screen](<img width="882" height="138" alt="ss8" src="https://github.com/user-attachments/assets/41448da8-f99c-401c-a1fd-10aaefca23a9" />)

---

## Task 4: Independent Practice & Synthesis
To solidify my learning, I ran through a comprehensive review phase. I combined everything I learned into a single session, executing an `echo` statement followed by a full suite of arithmetic operations (addition, subtraction, multiplication, and division).

![Comprehensive review of echo and math operations](<img width="882" height="278" alt="ss9" src="https://github.com/user-attachments/assets/64d0b339-94d8-41f3-953b-092fb18aab58" />)

---

## Conclusion
This lab successfully demonstrated the basics of interacting with the Linux shell. Overcoming the syntax error with `expr` taught me the importance of precision in command-line environments—a mindset that is essential when configuring security controls or analyzing logs.
