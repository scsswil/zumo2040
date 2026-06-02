# Setting things up

## Introduction

Before we can start programming the Zumo 2040, we need to set everything up correctly. This means collecting the robot, checking that it is ready to use, installing the software we will use to write Python code, and learning how to connect everything together.

By the end of this section, you will be able to turn the robot on, write simple Python programs, and send them to the Zumo 2040 so it can run your instructions.

## Collecting and Preparing the Robot

Start by collecting a Zumo 2040 robot and a set of charged NiMH AA batteries. These batteries provide the power for the robot, so it will not work without them.

Turn the robot over and open the battery compartment. Check that the batteries are inserted correctly. Each battery must match the polarity, which means the positive (+) and negative (–) ends must line up with the symbols inside the holder. If the batteries are the wrong way round, the robot will not turn on.

Once the batteries are in place, close the battery cover securely. Make sure it is fully fastened so the batteries cannot move during use.

To turn the robot on, locate the power switch on the board. Switch it to the “on” position. You may see a small LED light turn on to show that the robot has power.

If nothing happens, check the batteries again. Most issues at this stage are caused by incorrect battery placement or low charge.

## Installing Thonny

:::{warning} 

If you are working on a School or University computer where you are not able to install software then you should not follow the instructions of this section. The software will have already been downloaded and installed for your use.
:::

To program the Zumo 2040, we will use a Python editor called Thonny. An editor like this is called an IDE, which stands for Integrated Development Environment. It is simply a program that helps you write and run code.

Go to the Thonny webpage and download the IDE for your operating systems.

[Thonny download](https://thonny.org/)


Once the download is complete, run the installer and follow the instructions on screen. The installation is usually straightforward and only takes a few minutes.

When installation is finished, open Thonny. It may take a moment to load for the first time.

## Introduction to the Thonny IDE

When you open Thonny, you will see a simple interface designed for beginners.

At the top is a menu bar. This contains options such as opening files, saving work, and running programs. Below this is the main area where you write your Python code. This is called the editor.

```{figure} ../assets/thonny.png
:label: thonny
:align: center

Thonny's simple user interface.
```

At the bottom right of the screen is the shell. This is where the computer shows messages and results from your code. It is also where you can test small pieces of Python interactively.

When you run a program, you will see the results appear in the shell. If there is a mistake in your code, error messages will also appear here. These messages help you understand what went wrong so you can fix it.

For the Zumo 2040, Thonny will also be used to send your code directly to the robot. Once everything is connected, you will be able to write code in the editor and run it on the robot itself.