# Niryo One ROS stack

(Niryo One : [https://niryo.com](https://niryo.com/?utm_source=github))

![niryo one rviz simulation](https://niryo.com/wp-content/uploads/2017/12/ros_rviz_niryo_one.png)

This repository contains all ROS packages used on Niryo One (Raspberry Pi 3 - Xubuntu for ARM).

## How to use Niryo One with a graphical interface ?

You can [download Niryo One Studio](https://niryo.com/download/?utm_source=github) (Linux, Windows and MacOS compatible).

## How to install Niryo One ROS packages on your computer (x86) - Simulation Mode

Requirements :
* Ubuntu 16.04
* ROS kinetic  (other versions are not supported)

First install ROS kinetic "Desktop-Full" (tutorial [here](http://wiki.ros.org/kinetic/Installation/Ubuntu)).

You'll need to install some additional ROS packages :
```
sudo apt-get install ros-kinetic-robot-state-publisher ros-kinetic-moveit ros-kinetic-manipulation-msgs ros-kinetic-rosbridge-suite ros-kinetic-joy ros-kinetic-ros-control ros-kinetic-ros-controllers
```
Create a catkin workspace and clone Niryo One ROS stack :
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
git clone https://github.com/NiryoRobotics/niryo_one_ros.git .
```
Build the packages :
```
cd ~/catkin_ws
catkin_make
```
Don't forget to use those commands before you try to launch anything (you can add them in your .bashrc) :
```
source /opt/ros/kinetic/setup.bash
source ~/catkin_ws/devel/setup.bash
```
You can now launch Rviz with Niryo One :
```
roslaunch niryo_one_description display.launch
```

Niryo One ROS packages have been developed with **ROS kinetic, on Ubuntu 16.04**. Other ROS versions and OS distributions are not supported.

## Niryo One ROS Stack documentation

Here's a global overview of the Niryo One ROS Stack :

![niryo one ros stack - global overview](https://niryo.com/wp-content/uploads/2017/12/niryo_one_ros.png)

**You can find more specific and detailed info in each package's README.**

If you have a question and you don't find the answer here or on our [FAQ](https://niryo.com/niryo-one-faq/?utm_source=github) page, please send us an email at support@niryo.com.

Thank you !
