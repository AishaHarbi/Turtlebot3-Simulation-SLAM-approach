# Turtlebot3-Simulation-Slam-approach

### To install the required dependencies on Ubuntu 20.04 (Noetic)
#### run the following commands:
```ruby
cd [your workspace]
```
```ruby
git clone https://github.com/ros-perception/openslam_gmapping src/openslam_gmapping
```
```ruby
git clone https://github.com/ros-perception/slam_gmapping src/slam_gmapping
```
```ruby
rosdep install --from-paths src/ -i
```
```ruby
catkin_make -DCMAKE_BUILD_TYPE=RelWithDebInfo
```

### To start the simulation

#### run the following commands: 

First, to run the turtlebot3 gazebo:

```ruby
source /[your name]/home/[your workspace]/devel/setup.bash 
```
```ruby
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

![Screen Shot 2020-07-14 at 21 31 20](https://user-images.githubusercontent.com/45641051/87463006-75240b80-c619-11ea-8db4-e4253343bfa2.png)

 
#### to launch SLAM open a new terminal tab and run: 

```ruby
source /[your name]/home/[your workspace]/devel/setup.bash 
```

```ruby
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```


#### to remotely control the turtlebot3: 

```ruby
source /[your name]/home/[your workspace]/devel/setup.bash
```

```ruby
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

#### Finally to save the map: 

```ruby
rosrun map_server map_saver -f ~/map
```


#### the map after you move the turtlebot3 around its environment 

![Screen Shot 2020-07-14 at 21 31 08](https://user-images.githubusercontent.com/45641051/87463116-9b49ab80-c619-11ea-8769-eb197a68b30a.png)


