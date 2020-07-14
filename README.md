# Turtlebot3-Simulation-Slam-approach

### To install the required dependencies on Ubuntu 20.04 (Noetic)
#### run the following commands:

cd [your workspace]

git clone https://github.com/ros-perception/openslam_gmapping src/openslam_gmapping

git clone https://github.com/ros-perception/slam_gmapping src/slam_gmapping

rosdep install --from-paths src/ -i

catkin_make -DCMAKE_BUILD_TYPE=RelWithDebInfo

### To start the simulation: 

#### run the following commands: 

to run the turtlebot3 gazebo:

source /[your name]/home/[your workspace]/devel/setup.bash 

roslaunch turtlebot3_gazebo turtlebot3_world.launch

[a screenshot](https://imgur.com/pMLVPz2)
 
#### to launch SLAM open a new terminal tab and run: 

source /[your name]/home/[your workspace]/devel/setup.bash 


roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping


#### to remotely control the turtlebot3: 

source /[your name]/home/[your workspace]/devel/setup.bash


roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch


#### Finally to save the map: 

rosrun map_server map_saver -f ~/map
