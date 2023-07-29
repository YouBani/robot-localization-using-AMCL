# robot-localization-using-AMCL

The project's objective is to enable the robot to autonomously navigate through a familiar 2D map. This is achieved by employing the AMCL package for localization. The user has the option to set navigation goals via the move_base package or manually control the robot's movement using the teleop node. The repository consist of the following:

* `my_robot` which includes robot model, gazebo world and a 2D map
* `map_server`, `amcl` and `move_base` ROS packages
## Prerequisites
Install dependencies using the following commands:
``` sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get install ros-<your distro>-map-server
sudo apt-get install ros-<your distro>-amcl
sudo apt-get install ros-<your distro>-move-base
```
## Launch
* Launch the simulation 
``` roslaunch my_robot world.launch
```
* Launch the amcl launch file
``` roslaunch my_robot amcl.launch
```
* Launch the teleop script
``` rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
You could control the robot by keyboard commands now.
