# Cross-compilation assets

These are cross-compiling assets for ROS2.
Documentation is in the wiki: https://index.ros.org/doc/ros2/Tutorials/Cross-compilation


This version is intended to cross-build a lightweight (barebone) ROS2 for devices with the ARMv7 architecture

## How to build:

Detailed instructions are available on the [Cross Compilation Tutorial](https://index.ros.org/doc/ros2/Tutorials/Cross-compilation/)


    $ wget https://raw.githubusercontent.com/MehdiN/cross_compile/armhf/Dockerfile
    $ docker build -t ros2-crosscompiler:latest .
    $ docker run -it --name ros2_cc \
    -v /var/run/docker.sock:/var/run/docker.sock \
    ros2-crosscompiler:latest

The result of the build will be in `ros2_ws`:

    $ docker cp ros2_cc:/root/cc_ws/ros2_ws .


## TODO

 - [x] Customize cross-compilation files for armv7 architecture
 - [x] Discard the unnecessary packages for a barebone ROS2
 - [ ] Automate the cross-compilation for custom packages


## Status

| Packages  | Build Status| Target Running |
|:-------:|:--------:| :----------------:|
| ROS Core | Passing | TODO
| Exemples | TODO | TODO


## Usage


## Notes

### Missing packages from build:

| C++ | Python |
|:-------:|:--------:|
|`libtinyxml2.so.6`| catkin_pkg
| | pyparsing
| | em