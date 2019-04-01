# Cross-compilation assets

These are cross-compiling assets for ROS2.
Documentation is in the wiki: https://index.ros.org/doc/ros2/Tutorials/Cross-compilation



This version is intended to cross-build a lightweight (barebone) ROS2 for devices implementing the ARMv7 architecture

## How to build:

Detailled instructions are available on the [Cross Compilation Tutorial](https://index.ros.org/doc/ros2/Tutorials/Cross-compilation/)


    $ wget https://raw.githubusercontent.com/MehdiN/cross_compile/armhf/Dockerfile
    $ docker build -t ros2-crosscompiler:latest .
    $ docker run -it --name ros2_cc \
    -v /var/run/docker.sock:/var/run/docker.sock \
    ros2-crosscompiler:latest



## TODO

 - [x] Customize current files for armv7 architecture
 - [x] Discard the unnecessary packages for a barebone ROS2
 - [ ] Automate for cross-building custom packages