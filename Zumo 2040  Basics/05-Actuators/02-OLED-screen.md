# OLED Screen on the Zumo 2040

The Zumo 2040 has a small screen called an **OLED display** on the top between the tracks. This screen lets the robot show simple messages, numbers, and feedback. It is one of the most useful ways for a robot to “talk back” to us.

---

## Learning Outcomes

By the end of this lesson, you will be able to:

- Explain what the OLED screen does.
- Display text on the screen using Python.
- Show numbers and messages from your program.
- Use the screen to help debug (check) what your robot is doing.
- Combine movement and screen output in a simple program.

---

## What is the OLED screen?

The OLED screen is a very small display built into the robot.

It can show; Words, Numbers and Simple symbols. It cannot show detailed images or videos (easily). Instead, it is used for short messages. Think of it like a tiny digital notepad attached to your robot.

## Why do we use it?

When a robot is running code, we cannot always see what it's internal state is.

The OLED screen helps us by showing information such as:

- “I am moving”
- Speed values
- Sensor readings
- Test messages

It is especially useful when something goes wrong. Instead of guessing, we can make the robot show us what is happening.


## How the OLED screen works

The screen is controlled using code. You send a message from your program to the screen. The screen then displays it. It is like sending a text message to the robot’s display.

## Setting up the screen

Before using the screen, we need to create a screen object in our code in a similar way to how we created a motor object to control the motors.

```python
from zumo_2040_robot import robot

display = robot.Display()
```

Now we have a variable called `display`. This is what we use to control the screen.

---

## Showing a message

To show text on the screen, we write:

```python
display.text("Hello", 0, 0)
display.show()
```

This will display the word **Hello** on the screen. You must call the `show()` function to cause the screen to update and display whatever you have instructed it to. The second and third parameters are coordinates on the screen where the text should be printed. The second parameter is the x, or horizontal, coordinate. The third parameter is the y, or vertical coordinate. The origin, of the coordinate corresponding to (0,0) is the top left hand corner of the screen.

---

## Clearing the screen

Once you have written text to the screen the text will display forever, until you instruct the screen to clear itself. To do this we tell the screen to **fill** itself with a colour. As the screen is monochrome (Black/White), we set it to fill the screen with the black colour. 

```python
display.fill(0)
display.show()
```

## Showing numbers

We can also show numbers on the screen using formatted print statements in Python.

```python
display.text(f"{3.142}", 0 , 0)
```

This is useful when testing motor speeds or sensor values.

---

## Example: Robot saying what it is doing

Here is a simple program that shows messages while the robot moves:

```python
from zumo_2040_robot import robot
from time import sleep

motors = robot.Motors()
display = robot.Display()

display.text("Ready",0,0)
display.show()
sleep(1)


display.fill(0)
display.text("Moving")
display.show()

motors.set_speeds(200, 200)
sleep(2)

motors.set_speeds(0, 0)

display.fill(0)
display.text("Stopping")
display.show()
sleep(1)

display.fill(0)
display.show()
```

---

## What is happening in this program?

The robot:

1. Shows “Ready”
2. Waits for 1 second
3. Shows “Moving”
4. Drives forwards
5. Stops
6. Shows “Stop”
7. Clears the screen

This helps us understand what the robot is doing step by step.

---

## Key Ideas

- The OLED screen is a simple display on the robot.
- It helps the robot communicate with us.
- We use it to show messages, numbers, and status.
- It is very useful for testing and debugging code.

---

## Check Your Understanding

1. What can the OLED screen show?
2. Why is it useful when writing robot programs?
3. What does `display.fill()` do?
4. How can the screen help you fix problems in your code?
