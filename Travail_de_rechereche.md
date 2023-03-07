## Mon travail portera sur les exception en Python.
## Introduction
Software is a series of organized logical instructions, it often happens
that these instructions do not follow the logic (Division of a number by zero),
so in an error will be generated. these errors are called exception, 
they are of several types (the Exception provided by the language,
 custom exceptions...).

The purpose of the exceptions is to carry out processing
specific to the events that caused this exception.

## What is the Exception?
An exception is the interruption of program execution following a particular event.
i.e. even if a statement or an expression is syntactically
correct, it can cause errors during execution,
these errors detected during execution are called exceptions.
Exceptions are not a fatality, they give more
information about the error generated.
A short text to illustrate this introduction,
in this case divide a number by zero
![img2](img_Exception1.PNG)

The last line of the image names the class of the exception and the error message
this image also gives us the line where the error occurred...

## Exception handling
Exception management theory in Python revolves around handling unexpected errors or issues that occur during program execution. An exception is an event that disrupts the normal flow of a program, causing it to terminate immediately.

Python provides various built-in exceptions like TypeError, ValueError, NameError, IndexError, and so on which are raised when a program encounters an error.

The main objective of exception handling is to make the program more robust and ensure that it doesn't crash in the event of an error. Exception handling involves three main components:

1. Try: It is a block of code where you place the code that might raise an exception.

2. Except: It is a block of code where you handle the exception raised in a try block.

3. Finally: This block contains code that is executed irrespective of whether an exception occurs or not.

Here is an example of how exception handling works in Python:

```
try:
num = int(input("Enter a number: "))
result = 100 / num
print(result)
except ZeroDivisionError:
print("Cannot divide by zero!")
except ValueError:
print("Please enter a valid number!")
else:
print("No exceptions occurred.")
finally:
print("Program execution completed.")
```

In this example, we first take input from the user and convert it to an integer. Then we divide 100 by the input number and print the result. If the input is zero, we catch the ZeroDivisionError and print an appropriate message. Similarly, if the input is not a valid number, we catch the ValueError.

If no exception is raised, the else block is executed, where we print a message saying that no exception occurred. Finally, the finally block is executed, which prints a message indicating that the program has completed its execution.

Therefore, exception management theory in Python is essential for writing reliable and robust code that can handle unexpected errors gracefully.
An except clause can name multiple exceptions as a tuple in parentheses, for example:
![img2](img_Exception2.PNG)
the word pass means that the exception will not be treated
Exception can be used as a wildcard that catches (almost) everything. However, it is recommended that we be as specific as possible with the types of exceptions we intend to handle and allow any unexpected exceptions to propagate.

The most common Exception handling model is to print or log the exception and then rethrow it (allowing a caller to also handle the exception).
![img3](img_Exception3.PNG)
We can use else in a try, It is useful for code that needs to be executed if the try clause does not throw an exception. For example:
![img4](img_Exception4.PNG)
If a function is called in a try and this function generates an error
then this error will be catch  in the try.
![img5](img_Exception5.PNG)

you should know that all exceptions inherit from the class BaseException
![img6](img_Exception6.jpg)
