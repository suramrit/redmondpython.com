# Introduction to Python

# Schedule

- Overview
- Python Features
- Installation
- Using the Interpreter
- Tracebacks
- Comments
- Review
- Exercises
- Additional Resources

# Overview

Python is an easy-to-write, easy-to-read interpreted scripting language. "Hello world!" looks like this:

```py
>>> print("Hello world!")
Hello world!
```

Here's a more complex example (an application to send an email).

1. Import some code.
2. Create an SMTP object to connect with a server.
3. Log in to the server.
4. Create our message.
5. Send the message.

```py
import smtplib
server = smtplib.SMTP('smtp.gmail.com', 587)
server.login("youremailusername", "password")
msg = "/nHello!"
server.sendmail("you@gmail.com", "yourFriend@hotmail.com", msg)
```
The purpose of this example is to show you what you can accomplish in a few lines.

# Python Features

- Open source (anyone can see all of the underlying code)
- Object-oriented (everything in Python is an object)
- Platform-independent
- Strongly typed (no need to define a variable's data type)
- Minimalist design philosophy
  - Emphasizes cleanliness and readability
  - Minimal semicolons and brackets

What can you do with Python?

  - Interact with files on your computer
  - Automate workflow
  - Build and deploy APIs
  - Build games
  - Interact with web services

# Installation

First, you might already have Python3 installed (Python2 is retiring in 2020).

1. Open a terminal or command prompt.
2. Type `python` and hit **ENTER**.

Installing Python is easy. See [this page](https://www.redmondpython.com/setup/) for instructions.

# Using the Python Interpreter

Now that we have Python installed, let's open the interpreter:

1. Open a terminal or command prompt.
2. Type `python` and hit **ENTER**.

Your prompt should look something like:
```
Python 3.6.4 (default, Jan  3 2018, 12:27:09)
[GCC 4.2.1 Compatible Apple LLVM 9.0.0 (clang-900.0.39.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
You'll know you're in the interpreter when you see `>>>`. The interpreter is ready for your input. This is what is meant by "interpreted." There is no compiling in Python. You can just run the code.

Type `exit()` or hit `ctrl+d` to exit. Everything you entered in that previous session is lost between sessions.

<!-- Commenting out for now, let's use this in a later lesson

# Interactive Mode vs. Script Mode

There are two "modes" in which we can run Python. Open the interpreter again by running:
```
$ python
```
This is "Interactive Mode." This means we're feeding lines directly into the Python interpreter and it's interpreting the code live.

We'll run larger scripts later in "Script Mode." In that mode, you'll put your code in a file and pass it at the command line like this:
```
$ python myScript.py
```
For now, let's stick with Interactive Mode. -->

# Basic Operations

The purpose of this next section is **not** to teach you the basics of Python, but rather, get you comfortable entering data into the interpreter.

Open the Python interpreter and type the following lines, noting the output:
```
>>>2 + 4
>>>5 - 1
>>>3 * 4
>>>10 / 2
```
This is how easy it is to interact with the interpreter. This also introduces you to some basic math operations available to you in Python, like addition, subtraction, etc. We'll expand on this later.

Next, let's briefly introduce variables. Like other languages, Python variables store values--numbers, text, lists, etc. Let's create a few variables that store some simple integers.
```
>>>x = 4
>>>y = 2
>>>print(x + y)
```
Above, we assigned "4" to the variable x and "2" to y, and then call the "print" function to print the sum. Note that we don't have to declare our variables as "integers." Python is strongly typed and interprets a variable's type at runtime.

Try entering some strings of text:
```
name = "Your Name"
print(name)
print("Your Name")
```
One more thing to note. For now, our variables will start with a lowercase letter. We'll be expanding on variables and functions in a later lesson.

>*Remember*: Once you close the interpreter, all of this data is lost.

# Tracebacks

When you make a mistake, Python generates a traceback to tell you what went wrong.

Open the interpreter and run:
```py
>>> a = "John"
>>> a + 2
```
We see the following error:
```py
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: must be str, not int
```
The above traceback tells us the following:

- The name of the file where the error occurred: "<stdin>"
- The line number containing the error: 1
- The name of the module (if applicable)
- The error type: TypeError [(Full list of error types here)](https://www.tutorialspoint.com/python/standard_exceptions.htm)
- What's wrong: we tried to do something on one data type (an int) that Python will only let us do to a string

# Comments

Single line:
```
# Here is a code in python
name = "Your Name"
print(name)
print("Your Name")
```
This is an in-line comment:
```
name = "Your Name"
print(name) # Prints name
print("Your Name")
```
Here is a multiline comment
```
'''
This is a multiline comment for longer comments that you want to put in your code. Commenting code is important when you're sharing code with multiple people.
'''
name = "Your Name"
print(name)
print("Your Name")
```

# Review of Key Points

1. Python is open source.
2. Python is platform independent.
3. Python is minimalist.
4. Access the interpreter by running `$ python`.
5. You do not compile a Python program before you run it--you just run it. This is what is meant when people say Python is "interpreted."

# Exercises

TBD

# Additional Resources

- [Python Guide for Beginners - Non-Programmers](https://wiki.python.org/moin/BeginnersGuide/NonProgrammers)
- [Python Guide for Beginners - Programmers](https://wiki.python.org/moin/BeginnersGuide/Programmers)
- [Coding Bat](https://www.codingbat.com/python)
- [Hacker Rank](https://hackerrank.com)
- [Try Git](https://www.codeschool.com/courses/try-git)
