# Motors and Motor Control

## Learning Objectives

By the end of this lesson, you will be able to:

- Explain the purpose of the Zumo's motors.
- Write code to move the robot forwards and backwards.
- Change the speed of the motors.
- Stop the robot safely.
- Predict how different motor settings affect movement.

---

## What Makes the Zumo Move?

Unlike a normal computer, a robot can move around and interact with the world. The Zumo 2040 moves using two motors. Each motor is connected to a track. The tracks grip the ground and help the robot move. The robot is powered by a rechargeable battery. The battery provides energy for the motors. When the motors spin, the tracks move. When the tracks move, the robot moves. Each motor can be controlled separately. This allows the robot to move in different ways.

This means:

| Motor Action | Result |
|--------------|---------|
| Both motors forwards | Robot moves forwards |
| Both motors backwards | Robot moves backwards |
| One motor faster than the other | Robot turns |
| One motor forwards and one backwards | Robot spins on the spot |

---

## Creating a Motor Object

### What is a motor object?
Before we can control the motors, we need something in our program that represents them.

In Python, we call this an object.

An object is just a way of grouping something in the real world with instructions for how to use it in code.

So instead of talking directly to the hardware all the time, we create a simple “handle” for it in our program.

### Why do we need it?
The robot has two motors, but the computer does not automatically know how to control them.

We need a way to say:

“This is the motor system”
“These are the commands I want to use”

The motor object acts like a bridge between your code and the real motors on the robot.

Once it exists, you can give it instructions like:

 - set speed
 - stop
 - change direction


```{hint}
Imagine a TV remote.

The remote is not the TV. But it lets you control the TV without touching the inside of it.

The motor object works in a similar way.

It is not the motors themselves. It is a tool in your code that lets you control them easily.
```

### Give it a go
We need to create a motor object.

```python
from zumo_2040_robot import robot

motors = robot.Motors()
```

The `motors` object allows us to control both motors.

---

## Moving Forwards

The following program makes the robot move forwards for two seconds and then stop.

```python
from zumo_2040_robot import robot
from time import sleep

motors = robot.Motors()

motors.set_speeds(1000, 1000)

sleep(2)

motors.set_speeds(0, 0)
```

### Understanding the Code

The line:

```python
motors.set_speeds(1000, 1000)
```

contains two values:

| Value | Controls |
|---------|---------|
| First number | Left motor |
| Second number | Right motor |

Because both values are positive and equal, the robot moves forwards in a straight line.

The line:

```python
motors.set_speeds(0, 0)
```

stops both motors.

---

## Motor Speed Values

Motor speeds can range from:

```text
-6000 to +6000
```

| Value | Effect |
|---------|---------|
| 6000 | Full speed forwards |
| 2000 | Medium speed forwards |
| 0 | Stop |
| -2000 | Medium speed backwards |
| -6000 | Full speed backwards |

```{tip}
You can use any number your like between +6000 and -6000 for the speed of each motor.

Positive values move the motor forwards.

Negative values move the motor backwards.

The sign (+ or -) controls the direction. The size of the number controls the speed.
```

---

## Try It Yourself

Before running each command, predict what will happen. You should carefully lift the robot up off of the desk, being careful to not touch the tracks while you experiment.

```python
motors.set_speeds(100, 100)
```

```python
motors.set_speeds(400, 400)
```

```python
motors.set_speeds(-200, -200)
```

```python
motors.set_speeds(0, 0)
```

Discuss your predictions with a partner before testing them.

---

## Investigation: How Speed Affects Movement

In this investigation, you will explore how motor speed affects how far the Zumo travels. You will change the speed of the motors and measure the distance the robot moves in a fixed time. This will help you understand the relationship between speed and movement.

## What you are trying to find out

You are investigating:

**Does increasing motor speed make the robot travel further in the same amount of time?**

## What you will need

- Zumo robot  
- Thonny (Python editor)  
- Tape measure or ruler  
- Open floor space  
- A partner (recommended)


## Important setup

Before you begin, make sure:

- The robot starts from the same position each time  
- The floor is flat and clear  
- You always run the test for the same amount of time (2 seconds)  
- The robot is pointing in the same direction each time  

Consistency is important. If you change the setup, your results will not be reliable.



## Your test program

You will use the same basic program each time. Only the speed value will change.

```python
from zumo_2040_robot import robot
from time import sleep

SPEED = 1000
motors = robot.Motors()

motors.set_speeds(SPEED, SPEED)
sleep(2)
motors.set_speeds(0, 0)
```

## What you will change

You will test different speeds.

For example:

- 1000  
- 2000  
- 3000  
- 4000  

You will change this line:

```python
SPEED = 1000
```

---

## Step-by-step method

### Step 1: Set up the robot

1. Place the robot on the floor.

2. Make sure it is facing straight ahead.

3. Open a new Editor by clicking File > New.

4. Copy and paste the code from above into the editor window.

3. Do not start the program yet.

---

### Step 2: Choose your first speed

Start with a low speed, such as:

```text
1000
```

Update your code:

```python
SPEED = 1000
```

---

### Step 3: Run the program

Click **Run** in Thonny.

The robot will move for 2 seconds and then stop.

Stand clear while it moves.

---

### Step 4: Measure the distance

Use a ruler or tape measure to measure how far the robot travelled.

Measure from the starting position of the robot **to** the stopping position of the robot  

Record your answer in a table.

---

### Step 5: Reset the robot position

Carefully place the robot back at the starting point.

Make sure it is in the same position and facing the same direction as before.

---

### Step 6: Repeat the test

Repeat the process for each speed value:

- 1000 
- 2000  
- 3000  
- 4000  

Each time:

- change the speed in your code  
- run the program  
- measure the distance  
- record your result  

---

## Results table

Fill in your results like this:

| Speed setting | Distance travelled (cm) |
|--------------|--------------------------|
| 100 | |
| 200 | |
| 300 | |
| 400 | |

---

## Things to think about while you work

- Does the robot always travel in a perfectly straight line?  
- Is it easy to measure the exact stopping point?  
- Are your results similar each time you repeat a test?  

---

## Questions

1. What happens to the distance when the speed increases?  
2. Does doubling the speed double the distance?  
3. Why might your results not be exactly the same each time?  
4. What factors might affect how far the robot travels (e.g. floor type, battery level)?  

---

## Extension challenge

Try predicting a result before testing it.

For example:

- If the speed is 2500, how far do you think the robot will travel?

Then test your prediction and compare it to your real result.

---



## Turning the Robot

Because each motor can be controlled independently, we can make the robot turn.

```python
motors.set_speeds(100, 300)
```

The right motor moves faster than the left motor.

The robot curves towards the slower side.

```{figure} ../../assets/differential_steering.png
---
width: 100%
name: differential-drive-turn
---
The robot turns because the motors are moving at different speeds.
```

---

## Prediction Activity

What do you think will happen?

```python
motors.set_speeds(300, 100)
```

Write down your prediction and then test it, using the Python program from before.

---

## Spinning on the Spot

The motors can also move in opposite directions.

```python
motors.set_speeds(200, -200)
```

One motor moves forwards while the other moves backwards.

This causes the robot to spin on the spot.

```{warning}
Always make sure the robot has enough space around it before testing turning or spinning movements.
```

---

## Mini Challenge: Robot Dance

Create a program that:

1. Moves forwards
2. Spins
3. Moves backwards
4. Stops

You can start with this example:

```python
from zumo_2040_robot import robot
from time import sleep

motors = robot.Motors()

motors.set_speeds(200, 200)
sleep(1)

motors.set_speeds(200, -200)
sleep(1)

motors.set_speeds(-200, -200)
sleep(1)

motors.set_speeds(0, 0)
```

### Challenge
Can you create a dance routine that lasts at least 10 seconds and uses five different movements?


---

## Key Vocabulary

```{list-table}
:header-rows: 1

* - Word
  - Meaning
* - Motor
  - A device that converts electrical energy into movement.
* - Speed
  - How fast a motor rotates.
* - Direction
  - Whether a motor rotates forwards or backwards.
* - Drive System
  - The motors, wheels and tracks that move the robot.
* - Independent Control
  - Each motor can be controlled separately.
```

---

## Check Your Understanding

1. Which motor does the first value in `set_speeds()` control?
2. What does a speed value of `0` do?
3. What is the difference between `200` and `-200`?
4. Why does the robot turn when the motors run at different speeds?
5. What happens when one motor moves forwards and the other moves backwards?

---

## Success Criteria

I can:

- [ ] Make the robot move forwards.
- [ ] Make the robot move backwards.
- [ ] Stop the robot.
- [ ] Change motor speeds.
- [ ] Make the robot turn.
- [ ] Explain why different motor speeds change the robot's direction.