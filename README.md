# ROS-Beginner : Chapter 2 Navigating the ROS Filesystem

## Prerequisites
For this tutorial we will inspect a package in ros-tutorials, please install it using
```shell
sudo apt-get install ros-<distro>-ros-tutorials
```

Replace distro (including the <>) with the name of your (ROS distribution)[https://wiki.ros.org/Distributions] (e.g. indigo, kinetic, lunar etc.)

## Quick Overview of Filesystem Concepts
* <b>Packages</b>: Packages are the software organization unit of ROS code. Each package can contain libraries, executables, scripts, or other artifacts.
* <b>Manifests (package.xml)</b>: A manifest is a description of a package. It serves to define dependencies between packages and to capture meta information about the package like version, maintainer, license, etc...

## Filesystem Tools
rospack allows you to get information about packages. In this tutorial, we are only going to cover the find option, which returns the path to package.

Usage:
```shell
rospack find [package_name]
```

Example:
```shell
rospack find roscpp
# Output :
# /opt/ros/noetic/share/roscpp
```

## Using roscd
roscd is part of the rosbash suite. It allows you to change directory (cd) directly to a package or a stack.
Usage:
```shell
roscd <package-or-stack>[/subdir]
```

To verify that we have changed to the roscpp package directory, run this example:
```shell
roscd roscpp
pwd
# Output :
# /opt/ros/noetic/share/roscpp
```

```shell
echo $ROS_PACKAGE_PATH
# Output : 
# /opt/ros/noetic/share
```

### Subdirectories
roscd can also move to a subdirectory of a package or stack.
```shell
roscd roscpp/cmake
pwd
# Output :
# /opt/ros/noetic/share/roscpp/cmake
```

## roscd log
roscd log will take you to the folder where ROS stores log files. Note that if you have not run any ROS programs yet, this will yield an error saying that it does not yet exist.
```shell
roscd log
# Output : 
# No active roscore
```

## Using rosls
rosls is part of the rosbash suite. It allows you to ls directly in a package by name rather than by absolute path.
Usage:
```shell
rosls <package-or-stack>[/subdir]
```

Example:
```shell
rosls roscpp_tutorials
# Output :
# rosls roscpp_tutorials
```

## Tab Completion
It can get tedious to type out an entire package name. In the previous example, roscpp_tutorials is a fairly long name. Luckily, some ROS tools support TAB completion.

---
