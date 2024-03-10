# Serial Communication Library

[![Build Status](https://travis-ci.org/wjwwood/serial.svg?branch=master)](https://travis-ci.org/wjwwood/serial)*(Linux and OS X)* [![Build Status](https://ci.appveyor.com/api/projects/status/github/wjwwood/serial)](https://ci.appveyor.com/project/wjwwood/serial)*(Windows)*

This is a cross-platform library for interfacing with rs-232 serial like ports written in C++. It provides a modern C++ interface with a workflow designed to look and feel like PySerial, but with the speed and control provided by C++. 

This library is in use in several robotics related projects and can be built and installed to the OS like most unix libraries with make and then sudo make install, but because it is a catkin project it can also be built along side other catkin projects in a catkin workspace.

Serial is a class that provides the basic interface common to serial libraries (open, close, read, write, etc..) and requires no extra dependencies. It also provides tight control over timeouts and control over handshaking lines. 

### Documentation

Website: http://wjwwood.github.io/serial/

API Documentation: http://wjwwood.github.io/serial/doc/1.1.0/index.html

### Dependencies

Required:
* [cmake](http://www.cmake.org) - buildsystem

### Install

Get the code:

    git clone https://github.com/GoLeRobotics/serial.git

Build:

    mkdir build
    cd build
    cmake ..
    make -j4

Install:

    sudo make install
    # or
    sudo checkinstall # if checkinstall is installed via apt

### Reference from another CMake Project
```
find_library(LIBSERIAL serial)

add_executable(<PROJ_NAME> <PROJ_SOURCE>)
target_link_libraries(<PROJ_NAME> LIBSERIAL)
```


### License

[The MIT License](LICENSE) - Original License by W. Woodall

### Authors

William Woodall <wjwwood@gmail.com>
John Harrison <ash.gti@gmail.com>
-- CMake modification part: Hosik Chae <hosik@golerobotics.com>

### Contact

William Woodall <william@osrfoundation.org>
