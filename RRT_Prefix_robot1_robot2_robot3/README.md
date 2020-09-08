# Overview

This repo realizes controlling three robots to explore the unknown environment manually. All robots are named robot1/robot2/robot3 instead of robot_1/robot_2/robot_3. 

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
```
roslaunch rrt_exploration_tutorial mutliple_simulated_largeMap.launch
// use RVIZ Goal button to select the goal point of different robots to start exploration.
```
Have Fun :)

## Todo 
Fixed the existed bug as follows:
```
// temrinal 1
roslaunch rrt_exploration_tutorial mutliple
[ERROR] [1599358014.226781998, 4461.600000000]: The goal pose passed to this planner must be in the robot_2/map frame.  It is instead in the robot_1/map frame.
[ERROR] [1599358014.226809777, 4461.600000000]: The goal pose passed to this planner must be in the robot_3/map frame.  It is instead in the robot_1/map frame.
```
