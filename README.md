# ROSInstallationOnJetsonNano
ROS Installation steps on jetson nano developer kit- Smart methods training":

1.	Plug in the jetson nano to the PC.
2.	Open the terminal.
3.	Let the jetson nano accepting the software: 
$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'   

4.	Adding a new apt key:
$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

5.	Update the index of the Debian packages:
$ sudo apt update

6.	Install the desktop ROS package:
$ sudo apt install ros-melodic-desktop

7.	Make the ROS environment variables load when executing a new shell session:
$ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc 
$ source ~/.bashrc

8.	Install the rosdep in order to install the system dependencies:
$ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
$ sudo rosdep init 
$ rosdep update

9.	Install the following dependencies:
$ sudo apt-get install cmake python-catkin-pkg python-empy python-nose python-setuptools libgtest-dev python-rosinstall python-rosinstall-generator python-wstool build-essential git

10.	Create the root folder and the source folderfor the catkin:
$ mkdir -p ~/catkin_ws/src 
$ cd ~/catkin_ws/ 

11.	Configure the catkin workspace:
$ catkin_make

12.	Update the .bashrc to add some information about the workspace:
$ echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc 
$ source ~/.bashrc
