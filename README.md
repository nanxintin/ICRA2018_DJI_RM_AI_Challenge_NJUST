# ICRA2018_DJI_RM_AI_Challenge_NJUST
ICRA2018_DJI_RM_AI_CHALLENGE_NJUST is a stack for the research of [RoboMaster AI challenge](https://www.robomaster.com/zh-CN/resource/pages/729?type=announcementSub), developed by team Alliance at NJUST. This repository mainly focuses on the simulation part.

At the beginning of the project, we planned to create a stack of simulation environment to test our algorithm and train our deep reinforcement learning based decision making model. Then we would put it into practice. After weeks of brokenly developing, we basically got the simulation part done with some flaw. Considering our limited time and effort, we decide to make the simulation part an open-source software stack. It will be our great pleasure if the stack do something useful during your development.

In this project, we make integrated application of ROS(Kinetic) and GAZEBO to build the simulated model training platform.  

# Get  started
Robot simulation is an essential tool in every roboticist's toolbox. A well-designed simulator makes it possible to rapidly test algorithms, design robots, perform regression testing, and train AI system using realistic scenarios. Gazebo offers the ability to accurately and efficiently simulate populations of robots in complex indoor and outdoor environments. 

## Packages brief description
package	description	state
robots_description	main package of simulation environments	85% finished
infantry_teleop_tools	infantry teleoperation with joystick and keyboard	OK
infantry_2dnav	infantry navigation with the navigation stack	OK
Vision	armor detecting package(refer to RoboMaster	developing
	open-source code)
## Software Requirements
	• ROS kinetic (Ubuntu 16.04)
## Hardware
	• Processor: Intel® Core™ i5-6500 CPU @ 3.20GHz × 4 
	• NVIDIA GeForce GT 750M, 2 GB memory size
	• OS type: 64-bit
Tip: Recommend not to deploy this project with virtual machine.
Install dependencies for Ubuntu 16.04 kinetic
Install ROS
Please follow the installing and configuring ROS environment tutorial on ROS Wiki.
$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
$ sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
$ sudo apt-get update
$ sudo apt-get install ros-kinetic-desktop-full
$ sudo rosdep init
$ rosdep update
$ echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
$ source ~/.bashrc
$ sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential

$ mkdir -p ~/catkin_ws/src
$ cd catkin_ws/src/
~/catkin_ws/src$ catkin_init_workspace
~/catkin_ws/src$ cd ..
~/catkin_ws$ catkin_make
$ echo "source /home/cqw/catkin_ws/devel/setup.bash" >> ~/.bashrc

Third-party Library
$ sudo apt-get install ros-kinetic-joy
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-amcl
$ sudo apt-get install ros-kinetic-move-base
$ sudo apt-get install ros-kinetic-controller-manager
$ sudo apt-get install ros-kinetic-cv-bridge
$ sudo apt-get install ros-kinetic-gazebo-ros-pkgs ros-kinetic-gazebo-ros-control
$ sudo apt-get install ros-kinetic-ros-control ros-kinetic-ros-controllers

# Build and Install
~$ cd catkin_ws/src/
~/catkin_ws/src$ git clone 
~/catkin_ws$ catkin_make
# Run
$ roscore
$ roslaunch infantryb display.launch

## simulation part:
Tip: We set the "gui" parameter false as default in order to ease the computing load of GPU, if you want to get the gazebo view, you can change the false to true in the launch file.

$ roslaunch infantryb simulation_environments.launch


## armor detecting part:
$ rosrun infantry_vision image_prod_cons 




## joystick teleop part:
$ roslaunch joystick_teleop joystick_teleop.launch
 

## navigation part:
$ roslaunch infantryb gazebo_color.launch
$ roslaunch infantry_2dnav move_base.launch
 







# Documents
Please refer to the docs folder.
# Copyright and License
ICRA2018_DJI_RM_AI_CHALLENGE_NJUST is provided under the BSD license.
