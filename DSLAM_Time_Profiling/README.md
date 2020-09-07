
# DSLAM Profiling Project

Summary
- Modified based on the [dslam release version](https://github.com/efc-robot/dslam_release).
- Add time profiling part

# Ready to run
Modified the time_profiling_node.h in the 'dslam_release/include/' & 'octomap_server/include' following the steps below
- change the '/home/jimmy/work/C_test/profiling' to any path you like. 
- setup a catkin_workspace and put this repo under the src directory.
- follow the instruction of [dslam release repo](https://github.com/efc-robot/dslam_release) to config the dslam_release_time_profiling package.
- view the result in the TIME_PROFILING_PATH directory specified in time_profiling_node.h The time cost for executing the callback func was given.

