
# Go Chase It

The goal of this project is to build a mobile robot and make it chase a white colored 
ball in a simulated environment built in Gazebo.



## Description

The environment has been modeled in Gazebo. Since we are using
ROS, the robot is created in Unified Robot Description Format (URDF) which 
uses XML markup language.
## Build
Project was built and executed in Lubuntu Linux with CMake & g++/gcc, ROS and Gazebo installed.

Packages used are the my_robot package, which contains the world and the robot 
and the ball_chaser package which contains two ROS nodes for commanding the robot to chase the white ball.

Open the terminal and create the catkin_ws/src workspace and add the files.

Build with catkin:
```
catkin_make
source devel/setup.bash
```

Launch the world in Gazebo:
```
roslaunch my_robot world.launch
```

In a new terminal tab launch the ball chaser node:
```
roslaunch ball_chaser ball_chaser.launch
```

Now you can move the ball around in the robot's field of view for it to follow the ball.