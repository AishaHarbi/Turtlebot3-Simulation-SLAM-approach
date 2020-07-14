# Turtlebot3-Simulation-Slam-approach

### To install the required dependencies on Ubuntu 20.04 (Noetic)
###### run the following commands:

cd [your workspace]

git clone https://github.com/ros-perception/openslam_gmapping src/openslam_gmapping

git clone https://github.com/ros-perception/slam_gmapping src/slam_gmapping

rosdep install --from-paths src/ -i

catkin_make -DCMAKE_BUILD_TYPE=RelWithDebInfo

