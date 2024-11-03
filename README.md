# SWE_CAP2_GAME_AUTOMATION
# Programming the Farming Drone (Report)
## Introduction
The Farmer Was Replaced is a simulation game where you program a drone using a simple, Python-like language to automate various farming tasks.
. Instead of manually performing repetitive tasks, you write code to control the drone, making it plant, water, and harvest crops.
. As you optimize your code, you can unlock new technologies and improve your farm's efficiency.
. It's a fun way to learn programming and problem-solving while enjoying the satisfaction of watching your automated farm in action.


# Challenges Faced:
-Tracking down and fixing errors in the automation scripts was tricky, especially as the complexity of the tasks increases.

-Finding the most efficient way to perform tasks requires a lot of trial and error, as well as a solid understanding of algorithms and problem-solving.

# Learning Opportunities:
-Writing and debugging code in the game helps improve your overall programming abilities, particularly in languages similar to Python.
- The game encourages creative thinking and problem-solving, which are crucial skills in programming and beyond.


# Code-Snippets-and-Explanation
Write and explain your code along with recordings.
## Step 1: Farming on 1 tile
**Code:**
```python
while True:
if can_harvest():
harvest()
```

**Explanation:**
The code runs an infinite number of times and harvest the grass with the if condition.
**Demo:**
Video Demo:
![](c:\Users\dellb\Downloads\step1.mp4)
**Notes**
- Using the code above I was able to get enough hay to unlock the tile.
- These features were unlocked too: variables and functions.

## Step 2:
**Code:**
```python
while True:
    if num_items(Items.Hay) < 200:
        if can_harvest():
            harvest()
    elif num_items(Items.Wood) < 200:
        if can_harvest():
            harvest()
            plant(Entities.Bush)
    move(North)


**Explanation:**
 The code makes the drone move one square at a time, harvesting resources if their count is below 200, and then continues moving north.

**Demo:**
Video Demo:
![](step1.mp4)

**Notes**
-Using the automation script, the drone successfully maintained the resources, ensuring hay and wood levels were above 200.
-Unlocked the next tile, leading to additional features and functionality.

## Step 3: 
while True:
    if num_items(Items.Hay) < 400:
        if can_harvest():
            harvest()
        if get_ground_type() != Grounds.Turf:
            till()
    elif num_items(Items.Wood) < 200:
        if can_harvest():
            harvest()
        plant(Entities.Bush)
    elif num_items(Items.Carrot) < 200:
        if can_harvest():
            harvest()
        if num_items(Items.Carrot_Seed) == 0:
            # Add additional actions if no Carrot Seeds (example placeholder)
            pass
    move(North)



**Explanation:**
Infinite Loop: Runs continuously.

Conditions:
Checks if the number of Hay is less than 400. If so, it harvests and tills if the ground type isn’t Turf.

Checks if the number of Wood is less than 200. If so, it harvests and plants a Bush.

Checks if the number of Carrots is less than 200. If so, it harvests and checks for Carrot Seeds.

Movement: After managing resources, the drone moves north.

**Demo:**
Video Demo:
![](c:\Users\dellb\step3.mp4)

**Notes**
Using this script, the drone efficiently maintains resource levels (Hay, Wood, and Carrots).

This automation helps to keep resources balanced and unlock new features by maintaining resource thresholds.



## Step 4: 

    if num_items(Items.Hay) < 400:
    if can_harvest():
        harvest()
    if get_ground_type() != Grounds.Turf:
        till()
    elif num_items(Items.Wood) < 200:
        if can_harvest():
         harvest()
    plant(Entities.Bush)
    elif num_items(Items.Carrot) < 200:
        grow_carrot()
        move(North)
    if get_pos_y() == 0:
        move(East)


**Explanation:**
 The code manages different resources (Hay, Wood, and Carrots) by harvesting or growing them as needed and adjusts the character's position based on certain conditions.

If Hay is below 400, it checks to harvest and tills the ground if needed.

If Wood is below 200, it checks to harvest and plants a Bush.

If Carrots are below 200, it grows a Carrot and moves north.

If the y-coordinate is 0, it moves east.

**Demo:**
Video Demo:
![](c:\Users\dellb\step4.mp4)

**Notes**
Using this script, the drone efficiently maintains resource levels (Hay, Wood, and Carrots).

This automation helps to keep resources balanced and unlock new features by maintaining resource thresholds.

## Step 5: 

def grow_tree():
if can_harvest():
    harvest()
if get_pos_x() + get_pos_y() * 2 == 0:
   plant(Entities.Tree)
``` 

**Explanation:**
The function grow_tree():

Harvests trees if possible.
Plants a tree if the specified condition involving coordinates is met.
This code snippet might be used within a loop or called repeatedly to manage tree growth and harvesting dynamically based on position and conditions.

**Demo:**
Video Demo:
![](c:\Users\dellb\step5.mp4)

**Notes**
Using this script, the drone efficiently manages tree growth, ensuring a steady supply of wood resources.

This automation maintains a balanced resource flow by harvesting trees when ready and replanting them at specific positions, helping to achieve resource thresholds and unlock new features.


## References
List any resources, articles, or libraries you used or referenced while working on this project.
1. [Youtube](https://youtu.be/F5bpI_od1h0?si=sUcWAuCjsFp4gR3J)
2. [Youtube](https://youtu.be/U3qZtQ9CBgA?si=-97VD9XC8jCi9eqV)
3. ...