# The cp15_auxiliary_files repository

## Description

This respository contains files required by the checkpoint Nr 15 project.
Students must clone this respository into their ros2_ws workspace as instructed by the project.


## Main Launch
Terminal 1
ros2 launch rb1_ros2_description rb1_ros2_xacro.launch.py

## To test moving the robot
Terminal x
ros2 topic pub --rate 10 /rb1_robot/diffbot_base_controller/cmd_vel_unstamped geometry_msgs/msg/Twist "{linear: {x: 0.1, y: 0, z: 0.0}, angular: {x: 0.0,y: 0.0, z: 0.0}}"

## To list all ros2 controllers
ros2 control list_controllers --controller-manager /rb1_robot/controller_manager

## To list all ros2 controllers' hardware interface
ros2 control list_hardware_interfaces --controller-manager /rb1_robot/controller_manager

### Helper commands

#### Translate xacro to urdf
xacro xacro/rb1_ros2_base.urdf.xacro  robot_name:=rb1_robot > translated_rb1_ros2_base.urdf