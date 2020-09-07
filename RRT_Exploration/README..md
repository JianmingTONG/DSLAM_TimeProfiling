# Rapidly-exploration Random Tree (RRT) Deployment on single car in the unknown environment.
## Summary
This repo enables a single car to explore unknown environment autonomously using the RRT algorithm.

## Environment
Car: xtark robot with SLAMTech A1 RPLIDAR. (Supporting codes are stored in the xtark subdirectory.)
PC: 
- ubuntu 18.04
- ROS melodic
- [Original RRT code](https://github.com/hasauino/rrt_exploration)
Note: The debugged RRT code is located at the rrt_exploration_real_car subdirectory.

## Ready to run
1. setup a catkin_workspace and put this repo under the src directory.
2. Use catkin_make to build the directory.
3. setup the devel/setup.bash
4. run the following code in different terminal.
```
// New Terminal
roslaunch rrt_exploration_tutorials single_simulated_house.launch
// New Terminal
roslaunch rrt_exploration single.launch.
// Using Publish Point in RVIZ to click 5 points (the first points are to specify the range of exploration. the last point is the expected target location of the robot.)
```

Have Fun :)
