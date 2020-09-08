# Overview

This repo realizes controlling three robots to explore the unknown environment manually.

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