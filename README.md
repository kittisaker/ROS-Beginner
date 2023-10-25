# ROS-Beginner : Chapter 2 Navigating the ROS Filesystem

## Prerequisites
For this tutorial we will inspect a package in ros-tutorials, please install it using
```shell
sudo apt-get install ros-<distro>-ros-tutorials
```

Replace '<distro>' (including the '<b>') with the name of your (ROS distribution)[https://wiki.ros.org/Distributions] (e.g. indigo, kinetic, lunar etc.)

## Quick Overview of Filesystem Concepts
* <b>Packages</b>: Packages are the software organization unit of ROS code. Each package can contain libraries, executables, scripts, or other artifacts.
* <b>Manifests (package.xml)</b>: A manifest is a description of a package. It serves to define dependencies between packages and to capture meta information about the package like version, maintainer, license, etc...

## Filesystem Tools
rospack allows you to get information about packages. In this tutorial, we are only going to cover the find option, which returns the path to package.

Usage:
```shell
rospack find [package_name]
```