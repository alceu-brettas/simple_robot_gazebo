# Simple Robot for Gazebo
A simple Robot with 2 whels (and a caster) made for Gazebo simulation in a ROS/Gazebo Trainning with The Construct this year (2022). The Robot have a differential control and a camera

# Requirements #
This package is compatible with ROS Noetic version (Ubuntu 20.04). Existing versions on the internet support at most until Gazebo 11.

# Download and Compiling #
```
$ cd <catkin_ws>/src
$ git clone https://github.com/alceu-brettas/simple_robot_gazebo.git
$ cd <catkin_ws>
$ catkin make
```

Here <catkin_ws> is the path of the catkin workspace. Please refer to the [tutorial](http://wiki.ros.org/ROS/Tutorials) about how to create a catkin workspace in ROS.

# Run
The simplest way is calling after you have built the workspace successfully. The robot is spawned in a empty world and have a GUI for controling the motors.

```
$ roslaunch robot_description world.launch
```
## Spawn in any Gazebo world

With any other gazebo world already openned, one can spawn the robot in origin position with the following command.

```
$ roslaunch robot_description spawn.launch 
```

To use the GUI for controlling the robor uses:

```
$ roslaunch robot_description control.launch 
```

## Using Rviz

One can visualize the robot in Rviz with the next command.

```
$ roslaunch robot_description xacro_rviz.launch 
```

# Camera View #
One can use [rqt_gui](http://wiki.ros.org/rqt_gui) to have an extensive amount of utilities for topic visualization and manipulation. To the camera imagem, there is the following command.
```
$ rqt_image_view
```
