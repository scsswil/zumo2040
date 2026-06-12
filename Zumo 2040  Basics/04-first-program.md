# Your first Program in Thonny

:::{admonition} 
**Learning outcomes**

By the end of this activity, you will be able to:

 - Open and use the Thonny IDE.
 - Write a simple Python program.
 - Run a program and view its output.
 - Save a Python file.
 - Make small changes to a program and observe the results.
:::

## Introduction

Before we can program the Zumo 2040, we need to learn the basics of writing and running Python code. In this activity, you will create your first Python program using Thonny.

The program will display a message on the screen. Although it is very simple, it introduces the same process that programmers use every day: write code, run it, observe the result, and make improvements.

## What is a Program?

A program is a set of instructions that a computer follows.

Computers cannot think for themselves. Instead, they follow instructions exactly as they are written. These instructions are written using a programming language such as Python.

In this activity, we will use Python to tell the computer to display a message.

### Step 1: Open Thonny

1. Plug the Zumo 2040 into your computer using the provided USB-C cable.

2. Open the Thonny IDE on your computer.

3. When Thonny starts, you should see a large empty editor area at the top of the window and a shell at the bottom.

```{figure} ../assets/thonny.png
:label: thonny
:align: center

Thonny's simple user interface.
```

The Thonny interface showing the editor and shell.

The editor is where you write your code. The shell is where Python displays messages and results.

### Step 2: Write Your First Program

1. Click File > New.

2. Click inside the editor and type the following code:

```python
print("Hello, world!")
```

Take care to type the code exactly as shown, including the brackets and quotation marks.

3. Click File > Save, when prompted save the file on to the RP2040 device.

### Step 3: Run the Program

1. Click the green Run button at the top of the window.

You can also press F5 on your keyboard.

Python will run the program and display the result in the shell.

You should see:

```Hello, world!```

Congratulations! You have just run your first Python program.

#### How Does It Work?

The word print is a Python function.

A function is a command that tells Python to perform a specific task. The `print()` function tells Python to display some text.

The text we want to display is placed inside quotation marks:

```python
print("Hello, world!")
```

Anything inside the quotation marks is shown exactly as written.

### Step 4: Change the Message

1. Try changing the text inside the quotation marks. Remember to save your work after you have made a change.

For example:

```python
print("My name is Alex")
```

or

```python
print("I am learning robotics")
```

2. Run the program again and observe what happens.

Questions
 - What happened when you changed the text?
 - Did Python display exactly what you typed?
 - What happens if you remove one of the quotation marks?


#### Challenge Activity

1. Can you create a program that displays three different messages?

For example:

```python
print("Welcome to robotics!")
print("This is my first Python program.")
print("The Zumo 2040 is ready.")
```

3. Run the program and observe the output.

#### Challenge Questions
 - What happens when you add more `print()` statements?
 - Does Python display them in the same order that you wrote them?

Going Further

Programmers often use `print()` while developing programs. It is a useful way to check that a program is working correctly and to display information to the user.

Throughout the rest of this course, you will use `print()` to display information from sensors, check values stored in variables, and help debug your robot programs.

##  Conclusion

In this activity, you wrote and ran your first Python program using Thonny. You learned how to use the editor, run code, view output in the shell, and save your work.

Although the program was simple, it introduced the basic workflow used throughout this course:

 - Write code.
 - Run the code.
 - Observe the result.
 - Make improvements.

In the next activity, you will learn more about Python and begin using it to control the Zumo 2040.