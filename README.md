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

# [ROS Tutorials](http://wiki.ros.org/ROS/Tutorials)

# prerequisites to use ROS in Windows 10:
```
Windows 10 anniversary update or build 16215 or later 
(older versions aren't bash enabled, so no hope to with with)
```

# Install the Windows Subsystem for Linux
Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:

**1. Open PowerShell as Administrator and run:**
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
**2. Restart your computer when prompted.**

# Install your Linux Distribution of Choice
To download and install your preferred distro(s), you have three choices:

1. Download and install from the Windows Store (see below)

2. Download and install from the Command-Line/Script [(read the manual installation instructions)](https://docs.microsoft.com/en-us/windows/wsl/install-manual)

3. Download and manually unpack and install (for Windows Server - [instructions here)](https://docs.microsoft.com/en-us/windows/wsl/install-on-server)


# Install from the Microsoft Store

This section is for Windows build 16215 or later. 
Follow these steps to [check your build](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#check-your-build-number). 
For earlier versions of Windows 10, follow these instructions using [lxrun.](https://docs.microsoft.com/en-us/windows/wsl/install-win10#for-anniversary-update-and-creators-update-install-using-lxrun)

1. **Open the Microsoft Store and choose your favorite Linux distribution.**

![store](https://user-images.githubusercontent.com/18008644/43679334-6cc56a0a-9845-11e8-939b-26542fee0abb.png)

The following links will open the Windows store page for each distribution:

* [Ubuntu](https://www.microsoft.com/en-bd/p/ubuntu/9nblggh4msv6?rtc=1)

* [OpenSUSE](https://www.microsoft.com/en-bd/p/opensuse-leap-42/9njvjts82tjx?rtc=1)

* [SLES](https://www.microsoft.com/en-bd/p/suse-linux-enterprise-server-12/9p32mwbh6cns?rtc=1)

* [Kali Linux](https://www.microsoft.com/en-bd/p/kali-linux/9pkr34tncv07?rtc=1)

* [Debian GNU/Linux](https://www.microsoft.com/en-bd/p/debian-gnu-linux/9msvkqc78pk6?rtc=1)



2. **From the distro's page, select "Get"**

![ubuntustore](https://user-images.githubusercontent.com/18008644/43679426-de0bf610-9846-11e8-93f9-e4e4bb68e7ac.png)



So, Your Distro is now ready, next step is to install and create ubunru environment and run ROS

# Initializing a newly installed distro
