# Overview

This repo is simulation version of RRT Exploration for single robot or multiple robots.

## Environment
PC: 
- ubuntu 18.04
- ROS melodic

## Map Merge
The relative poses and transformations are manually setup in the .launch file. Maps from all robots are merged together using the mapmerge_node in the mapmerge package. With respect to the [multirobot_map_merge](https://github.com/hrnr/m-explore) package (This package uses OpenCV libraries to merge maps from all different robots. The origin of the odometry is the center of the input map, for which the origin will changes the location when receiving different maps. However, as for the real robot in the simulation environment or in the real world, the origin of odometry is fixed all the time. As a result, the merged map will be invalid.) The new map merge is modified from [mapmerge package](https://github.com/donghl17/RRT-Github-Test). Maps from different robots are merged using ros-based msg type and functions. 

## Ready to Run
- change the '/home/jimmy/work/C_test/profiling' to any path you like.
- setup a catkin_workspace and put this repo under the src directory.
- Run the following code in terminal

### Single Robot Simulation in house
```
// Terminal 1
roslaunch rrt_exploration_tutorial single_simulated_house.launch

// Terminal 2
roslaunch rrt_exploration single.launch

// click two points in RVIZ which are the diagonal points of the rectangle region to explore
// click one goal point in RVIZ to setup the goal of the robot.
```

### Multiple Robots Simulation in house (two robot)
```
// Terminal 1
roslaunch rrt_exploration_tutorial multiple_simulated_house.launch

// Terminal 2
roslaunch rrt_exploration two_robots.launch

// click two points in RVIZ which are the diagonal points of the rectangle region to explore
// click one goal point in RVIZ to setup the goal of the robot.

// You can also uncomment spawn-robot3 & transform between robot3 and robot1 in multiple_simulated_house.launch and then run the following code to start three robots simulation.
// Terminal 1
roslaunch rrt_exploration_tutorial multiple_simulated_house.launch

// Terminal 2
roslaunch rrt_exploration three_robots.launch
```


Have Fun :)