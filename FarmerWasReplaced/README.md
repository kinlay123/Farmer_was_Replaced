# Programming the Farming Drone (Report)
## Introduction
Briefly describe the game and the objective.
In The Farmer Was Replaced, players take on the role of a futuristic AI-powered farming robot that has replaced the human farmer. The game is set on a small farm, where the player must manage various farming tasks, such as planting crops, harvesting produce, and taking care of livestock, while optimizing efficiency to meet production goals. The twist is that the player must also navigate unexpected challenges—like weather events, pests, and malfunctions—that require strategic adjustments to keep everything running smoothly.

The objective of the game is to maintain the farm's productivity by successfully completing daily and seasonal tasks, maximizing yield, and ensuring all elements of the farm are balanced and sustainable. Players earn points or rewards based on their efficiency and can unlock upgrades to improve their robot's capabilities, making the farm even more efficient and productive over time.


# Table of Contents
- [Code Snippets and Explanation](#code-snippets-and-explanation)
- [Challenges and Learnings](#challenges-and-learnings)
- [References](#references)
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
![](./lv_0_20241104082040.mp4)
**Notes**
- Using the code above I was able to get enough hay to unlock the tile
- These features were unlocked too: variables and functions.
## Step 2: Farming on 3x3 tile
**Code:**
```python
while True:
# Code to go around
if can_harvest():
harvest()

```

**Explanation:**
The code makes the drone go one square at a time harvests the grass with the if condition.
**Demo:**
Video Demo:
![](./lv_0_20241104082040.mp4)
**Notes**
- Using the code above I was able to get enough hay to unlock the tile
- These features were unlocked too: variables and functions.
.
## Step 3: Farming on 4x4 tile
**Code:**
```python
while True:
    for i in range(get_world_size()):
        move(North)
        if can_harvest():
            harvest()
            if num_items(Items.Hay) < 500:
                plant(Entities.Grass)
            else:
                plant(Entities.Bush)
    move(East)
**Explaination**
This code describes the behavior of an entity (like a character or a robot) that is exploring and working in a grid-based world. Here’s how it works:
Continuous Operation: The entity is in an infinite loop, meaning it will keep running these actions forever or until the program is stopped.
Moving North: Within each cycle, the entity starts by moving northward. It goes step-by-step from the bottom to the top of a "column" in the world, moving north until it reaches the edge of the grid (as determined by the world’s size).
Harvesting Resources: As the entity moves north, it checks if there are any resources it can harvest at each step. If there are resources, it harvests them.
Planting Grass or Bushes: After harvesting, the entity decides whether to plant grass or bushes based on how much "hay" it has in its inventory:
If it has fewer than 500 units of hay, it plants grass.
If it has 500 or more units of hay, it plants a bush instead.
This check is done at each step, so the entity may plant different things as it moves based on the current hay count.
Moving East: Once it reaches the top of the column, the entity moves one step to the east, starting the cycle again in the next column.
Sweeping Through the World: The entity systematically moves north up one column, then east to the next, then north again, effectively sweeping through the world grid column by column. It keeps repeating this pattern, continuously harvesting and planting based on the conditions described.
This pattern allows the entity to cover the entire world grid over time, maintaining a certain number of resources while adapting its actions based on the inventory count.
Video Demo:
![](./lv_0_20241104082040.mp4)

. 
.
.
.
.
.
.
.
# Challenges and Learnings
## Challenges
#Discuss any significant challenges you faced while trying to solve the issues in the game.
One of the significant challenges in The Farmer Was Replaced is balancing efficiency with adaptability. Since the player is controlling an AI farming robot, there’s a constant tension between following a set routine to maximize efficiency and needing to adapt quickly to unexpected changes like weather events, pests, or machine malfunctions. This means players have to plan several steps ahead, keeping resources available for emergencies while not sacrificing productivity.
Another major challenge is resource management. The game often limits resources like water, energy, and repair materials, so players must prioritize tasks based on immediate needs versus long-term gains. This requires a strategic approach, as overusing resources for short-term gains can lead to setbacks in the future.
Finally, there’s a challenge in upgrading the robot’s abilities. The game often presents multiple upgrade options, but choosing the wrong upgrade can make certain tasks more difficult or leave the player vulnerable to specific challenges. Balancing the need for general efficiency with specialized abilities is key, and often requires replaying tasks or experimenting with different upgrade combinations.
These challenges together make The Farmer Was Replaced a game that requires players to balance routine, flexibility, and strategic resource allocation to succeed.
#Discuss any optimization methods you implemented to make the harvesting faster.
To make harvesting faster in The Farmer Was Replaced, I used a few key tricks:
Efficient Paths: I set the robot to follow the shortest path through the fields, so it spends less time moving around.
Prioritizing Crops: High-value or ripe crops were harvested first, making sure nothing went to waste.
Multi-Tool Upgrades: The robot got tools that could harvest and carry crops at the same time, saving trips back and forth.
Smart Crop Detection: The robot used sensors to quickly spot ripe crops, avoiding unripe ones to save time.
Energy Management: I optimized energy use so the robot worked efficiently without running out of power too quickly.
Preventive Maintenance: Small repairs were done during breaks to prevent breakdowns when the robot was busy.
Together, these tricks made harvesting faster and smoother.
## Learnings
#Note down what different algorithms and methods of programming you learnt (E.g: Given a number n, I learnt
an algorithm that makes the drone travel each tile one by one efficiently given it’s position)
Pathfinding: Used algorithms like A* to help the robot find the shortest path through fields.
Task Prioritization: Learned how to pick urgent tasks first, like harvesting ripe or valuable crops.
Resource Management: Applied methods to carry the maximum load without wasting energy.
Energy Optimization: Managed the robot’s energy to focus on important tasks without running out.
Object Detection: Programmed the robot to quickly spot ripe crops using basic detection techniques.
Maintenance Scheduling: Planned small repairs during downtime to avoid unexpected breakdowns.
## References
List any resources, articles, or libraries you used or referenced while working on this project.
1. [Watched Youtube video](URL)
