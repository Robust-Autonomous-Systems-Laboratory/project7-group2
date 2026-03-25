# EE5531 Project 7: Introduction to the ROS2 Navigation Stack

Group 2 - Ian Mattson and William Forney

# Introduction and Setup

In this project, the ROS2 Nav stack is used with the TurtleBot3 Burger to create a SLAM map in both a simple simultated enviornment and the EERC 722 Lab. Additionally, a more realistic simulated enviornment is mapped using the Clearpath Jackal simulation package. 

All parts of this project were completed using ROS2 Jazzy Jalisco on an Ubuntu 24.04 Noble Numbat operating system.

__TBD: Setup challenges and how we resolved them__


# Part 1 - TurtleBot3 Simulation

Part 1 introduces the Nav2 stack through the Turtlebot World simulation enviornment.  When first loaded, the map indicates open, drivable areas as white pixels and barriers, or non-drivable areas as black pixels.  Once the 2D pose estimate is set, cost color layering is applied. Teal areas indicate likely collision areas, followed by a red to blue gradient for all other areas, where red is higher cost (wall is close) and blue is lower cost (wall if far).  Areas between the nine columns are higher cost, so the path planned in Figure 1 planned around the all columns rather than travel between them. 

If the robot becomes stuck, it tries to rotate and try another approach, but if the goal is still unreachable, it fails the execution. A successful route naviation returns a "Goal Reached" message, illustrated in Figure 2.

![Part 1 Nav2 Goal in RViz with Path and Cost Map](./figures/part1_nav2_goal.png)

<u>Figure 1:</u> RViz screenshot illustrating the Turtlebot navigating from the initial starting location to a 2D nav goal, where the route is indicated as the pink line and the cost map is indicated with a gradient of blue (low cost) to red (high cost), with teal areas indicating likely collision areas.

![Part 1 Nav2 Goal Reached Message](./figures/part1_terminal.png)
<u>Figure 2:</u> Terminal confirmation of 2D nav goal reached as "Reached the Goal!" and "Goal Succeeded".


# Part 2 - Real-World Mapping of EERC 722

- Completed map screenshot/image
- Description of driving strategy
- Rviz point-to-point navigation in the room screenshot/screen recording
- map yaml and pgm files must be present in [maps](./maps/)


# Part 3 - Jackal Simulation

- Gazebo screenshot
- RViz nav view screenshot
- Brief comparison: what was different setting up to Nav2 for the Jackal vs the Turtlebot3
- map yaml and pgm files must be present in [maps](./maps/)



# AI Disclosure Statement

No AI tools were used in any part of this project