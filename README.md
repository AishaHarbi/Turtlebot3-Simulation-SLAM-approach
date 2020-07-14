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

![Screen Shot 2020-07-14 at 20 34 40](https://user-images.githubusercontent.com/45641051/87462062-05615100-c618-11ea-84ef-253217b7b6bf.png)

 
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

![Screen Shot 2020-07-14 at 20 34 32](https://user-images.githubusercontent.com/45641051/87462180-304ba500-c618-11ea-8bed-9a0a755b198a.png)


