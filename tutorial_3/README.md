# Tutorial 3: Turtlebot3 

# ROS Installation
## Pre-requites for this tutorial
Please, install Ubuntu 20.04 and ROS Noetic by following the instrcutions on http://wiki.ros.org/noetic/Installation/Ubuntu 

## Installation of your project repository
~~~~bash
source /opt/ros/melodic/setup.sh
~~~~

Move to anyfolder you want to place the class code. Then, you can create the workspace,
~~~~bash
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src/
catkin_init_workspace
~~~~

Let's copy the the class repo, install dependencies, and build it!
~~~~bash
git clone git@github.com:pidipidi/CS470_IAI_2022Fall.git
cd ..
rosdep install --from-paths src --ignore-src --rosdistro=noetic -y
catkin_make
~~~~
If you want catkin_build, you can use it instead of catkin_make.

Lastly, load the new environmental variables and also add to path the environmental setup to your bashrc
~~~~bash
source ./devel/setup.bash
echo 'source ~/catkin_ws/devel/setup.bash' >> ~/.bashrc
~~~~

You can verify your ROS install by confirming the environmental variables
~~~~bash
env| grep ROS
~~~~

Make sure that if ROS_MASTER_URI and ROS_ROOT, ETC are in your bashrc.
~~~~bash
export ROS_MASTER_URI=http://localhost:11311
~~~~


# Sub-tutorial Links
- [Tutorial ROS](https://github.com/pidipidi/CS470_IAI_2022Fall/blob/main/tutorial_3/README_ROS.md)
- [Tutorial Turtlebot3](https://github.com/pidipidi/CS470_IAI_2022Fall/blob/main/tutorial_3/README_TURTLEBOT.md)
