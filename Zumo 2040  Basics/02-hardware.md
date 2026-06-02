# Hardware

The Zumo 2040 is a small robot made up of several different parts that work together. Each part has a specific job. When combined, these parts allow the robot to move, sense its surroundings, and respond to instructions written in code.

In robotics, we often describe these parts as hardware. Hardware simply means the physical components you can see and touch, as opposed to software, which is the code you write in Python.

Below is an overview of the main hardware components in the Zumo 2040 and what they are used for.

```{figure} ./assets/zumo_2040_front.jpg
:label: zumo_2040_front
:align: center

Front view of the Zumo 2040 robot.
```

## Microcontroller (the “brain” of the robot)

The microcontroller is a small computer built into the robot. In the Zumo 2040, this is based on the RP2040 chip. It acts as the robot’s brain, running the Python programs you write and controlling everything the robot does.

When your program runs, the microcontroller reads inputs from sensors, processes that information, and then sends signals to other parts of the robot such as the motors and LEDs. Without it, the robot would not be able to follow instructions or make decisions.

### What it is used for
 - Controlling movement
 - Making decisions based on sensor input
 - Running autonomous behaviours (robot actions without human control)


## Buttons

The robot includes small push buttons that allow simple interaction. These buttons can be programmed so that pressing them triggers actions, such as starting a program or switching between different modes of behaviour.

Although simple, buttons are useful for testing and controlling the robot without needing to connect it to a computer each time.

The robot has four buttons, but only three of them can be used for user input. User input is any information or action provided by a person (such as pressing a button or typing a command) that a computer or robot uses to decide what to do. They are located at the rear of the robot on the top of the robot. If you look carefully they are labelled "A", "B" and "C". 

The fourth button is labelled "Reset" and is located on the top of the robot towards the right side track. 

```{figure} ../assets/zumo_2040_top.jpg
:label: zumo_2040_top
:align: center

Top view of the Zumo 2040 robot.
```

You will learn how to used the buttons later on.

## Motors and Tracks

The Zumo 2040 moves using two electric motors, each connected to a set of rubber tracks similar to those on a tank. A motor converts electric energy into movement energy (kinematic energy). When the motors spin, they turn the tracks, allowing the robot to move forwards, backwards, or turn on the spot.

The motors are attached to the tracks from a sprocket (a wheel with teeth that mesh with the track). 

```{figure} ../assets/zumo_2040_side.jpg
:label: zumo_2040_side
:align: center

Side view of the Zumo 2040 robot.
```

The use of tracks instead of wheels gives the robot better grip and stability, especially on different surfaces such as smooth tables or competition arenas. By controlling how fast each motor spins, you can make the robot move in different directions or turn with different speeds.

You will learn how to use the motors later on.

### What they are used for
 - Driving in a straight line
 - Turning left and right
 - Competing in challenges such as sumo battles or obstacle courses


## Line Sensors (Reflectance Sensors)

On the underside of the robot are small sensors known as line sensors. These are also called reflectance sensors because they work by shining light onto the ground and measuring how much is reflected back.

Light-coloured surfaces reflect more light, while dark surfaces reflect less. By measuring this difference, the robot can detect changes in the surface underneath it. This is especially useful for following lines or detecting the edge of a sumo ring, where falling off the surface must be avoided.

The line sensors are located just behind the front scoop. There are five line sensors on the electronics behind the scoop. If you look carefully they are symmetrically placed, two are on the far left and right, and the remaining three are located around the center line. You will learn how to use these sensors later on.

```{figure} ../assets/zumo_2040_bottom.jpg
:label: zumo_2040_bottom
:align: center

Bottom view of the Zumo 2040 robot.
```

## Front Sensors (Proximity Sensors)

At the front of the Zumo 2040 are sensors designed to detect nearby objects. These are known as proximity sensors, meaning they can sense how close something is without needing to touch it.

These sensors allow the robot to detect obstacles or other robots in front of it. In competitions such as robot sumo, this is particularly important because it allows the robot to find and engage with an opponent.

The Zumo has three proximity sensors. One can be seen through the scoop at the front of the robot, and the other two can be seen just behind the scoop on the left and right sides of the robot. This allows the robot to detect objects approaching from the front or sides of the robot. The robot is not able to detect objects to its rear.

```{figure} ../assets/zumo_2040_front_on.jpg
:label: zumo_2040_front_on
:align: center

Front view of the Zumo 2040 robot looking at the scoop.
```

You will learn how to use the proximity sensors later on.


## LEDs (Light Emitting Diodes)

The Zumo 2040 also includes small lights called LEDs. An LED is a component that emits light when electricity passes through it. These can be controlled using code.

An RGB LED is a type of light that can produce different colours by combining three small LEDs inside it: red, green, and blue (that is what RGB stands for).

By changing how bright each of these three colours is, the robot can create a wide range of colours—for example, mixing red and green can make yellow, while all three together at different levels can produce colours like purple or white.

On the Zumo 2040, an RGB LED can be used to give visual feedback about what the robot is doing, such as showing different colours when it is starting a program, detecting a sensor event, or switching between modes.

The robot has 6 RGB LEDs, in addition to a few LEDs that indicate if the robot is turn on or off.

You will learn how to use the RGB LEDs later on.


## Buzzer

The robot includes a small component called a buzzer, which can produce simple sounds. These sounds are created by rapidly vibrating a small internal element when electricity is applied.

The buzzer is useful for giving audio feedback. This can be helpful when you cannot easily see the robot, or when you want to indicate events such as the start of a match or a completed task.

The noises you generate with the Buzzer can be quite annoying, so be careful not to annoy other people too much.

You will learn how to use the Buzzer later on.

## Battery Pack

The battery pack provides the electrical power that allows the Zumo 2040 to operate. Without it, none of the robot’s components—such as the motors, sensors, or microcontroller—would work.

The Zumo 2040 uses NiMH rechargeable AA batteries. NiMH stands for Nickel-Metal Hydride, which is a type of rechargeable battery commonly used in classroom electronics because it is reliable, safe, and can be reused many times. The robot is typically powered by four AA NiMH batteries, which supply enough energy for both movement and sensor operation.

To replace the batteries, the battery cover on the underside of the robot is opened. The old batteries are removed and replaced with fully charged ones. It is important to insert them correctly by matching the polarity, which means aligning the positive (+) and negative (–) ends of the batteries with the markings inside the holder. If batteries are inserted the wrong way, the robot will not turn on.

Because the robot is used for repeated activities and competitions, the NiMH batteries will need to be recharged regularly. Rechargeable batteries should always be charged fully before use to ensure the robot performs consistently throughout a session.

It is good practice to check battery levels before starting. If the batteries are running low, the robot may behave unpredictably, such as moving slowly, resetting during programs, or failing to respond correctly to sensors.