# ROS-Beginner : Chapter 1 Installing and Configuring ROS Environment

## Install ROS (Noetic)
Before starting these tutorials please complete installation.

## Managing Your Environment
If you are ever having problems finding or using your ROS packages make sure that you have your environment properly setup.
```shell
printenv | grep ROS

# Example Result :
ROS_VERSION=1
ROS_PYTHON_VERSION=3
ROS_PACKAGE_PATH=/opt/ros/noetic/share
ROSLISP_PACKAGE_DIRECTORIES=
ROS_ETC_DIR=/opt/ros/noetic/etc/ros
ROS_MASTER_URI=http://localhost:11311
ROS_ROOT=/opt/ros/noetic/share/ros
ROS_DISTRO=noetic
```

If you just installed ROS from apt on Ubuntu then you will have setup.
```shell
source /opt/ros/<distro>/setup.bash
```

If you installed ROS Noetic, that would be:
```shell
source /opt/ros/noetic/setup.bash
```

## Create a ROS Workspace
Create and build a catkin workspace:
```shell
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
```

Before continuing source your new setup.*sh file:
```shell
source devel/setup.bash
```

To make sure your workspace is properly overlayed by the setup script
```shell
echo $ROS_PACKAGE_PATH

# Result :
/opt/ros/noetic/share
```

---