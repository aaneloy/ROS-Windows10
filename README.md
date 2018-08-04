# ROS-Windows10
All the steps to use Robot Operating System(ROS) in windows 10. 

# What is ROS
[ROS](http://wiki.ros.org/ROS/Introduction) is an open-source, meta-operating system for your robot. It provides the services you would expect from an operating system, including hardware abstraction, low-level device control, implementation of commonly-used functionality, message-passing between processes, and package management. It also provides tools and libraries for obtaining, building, writing, and running code across multiple computers. ROS is similar in some respects to 'robot frameworks,' such as Player, YARP, Orocos, CARMEN, Orca, MOOS, and Microsoft Robotics Studio.

The ROS runtime "graph" is a peer-to-peer network of processes (potentially distributed across machines) that are loosely coupled using the ROS communication infrastructure. ROS implements several different styles of communication, including synchronous RPC-style communication over services, asynchronous streaming of data over topics, and storage of data on a Parameter Server. These are explained in greater detail in our Conceptual Overview.

ROS is not a realtime framework, though it is possible to integrate ROS with realtime code. The Willow Garage PR2 robot uses a system called pr2_etherCAT, which transports ROS messages in and out of a realtime process. ROS also has seamless integration with the Orocos Real-time Toolkit.

# Why ROS 

Some goals of the ROS framework:

* Thin: ROS is designed to be as thin as possible -- we won't wrap your main() -- so that code written for ROS can be used with other robot software frameworks. A corollary to this is that ROS is easy to integrate with other robot software frameworks: ROS has already been integrated with OpenRAVE, Orocos, and Player.

* ROS-agnostic libraries: the preferred development model is to write ROS-agnostic libraries with clean functional interfaces.
Language independence: the ROS framework is easy to implement in any modern programming language. We have already implemented it in Python, C++, and Lisp, and we have experimental libraries in Java and Lua.

* Easy testing: ROS has a builtin unit/integration test framework called rostest that makes it easy to bring up and tear down test fixtures.

* Scaling: ROS is appropriate for large runtime systems and for large development processes.

# Operating Systems
ROS currently only runs on Unix-based platforms. Software for ROS is primarily tested on Ubuntu and Mac OS X systems, though the ROS community has been contributing support for Fedora, Gentoo, Arch Linux and other Linux platforms.

While a port to Microsoft Windows for ROS is possible, it has not yet been fully explored. 


# Using Ros in Wondows 10:

# prerequisites:
```
Windows 10 anniversary update or build 1803 (older versions aren't bash enabled, so no hope to with with)
```

# Enable WAs
