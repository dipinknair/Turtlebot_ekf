
# Turtlebot EKF
EKF ROS package to localize your robot inside a Gazebo environment. Drive the robot around in simulation and observe the `Odom` and `EKF` trajectories.   

<img src="images/turtlebot_ekf.png" alt="demo" width="500" height="280"/></a>

### Pre-reuisite
Ubuntu 16 and Ros Kinetic 

#### Step 1 Create a Catkin Workspace
```sh
$ mkdir -p /home/workspace/catkin_ws/src
$ cd /home/workspace/catkin_ws/src
$ catkin_init_workspace
$ cd ..
$ catkin_make
```

#### Step 2 Perform a System Update/Upgrade
```sh
$ apt-get update
$ apt-get upgrade -y
```

#### Step 3 Clone the Package in src
```sh
$ cd /home/workspace/catkin_ws/src
$ git clone https://github.com/dipinair/Turtlebot_ekf
```


#### Step 5 Install Packages Dependancies
```sh
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ rosdep -i install turtlebot_gazebo
$ rosdep -i install turtlebot_teleop
```

#### Step 6 Build the Packages
```sh
$ catkin_make
$ source devel/setup.bash
```

#### Step 7 Launch the main file
```sh
$ roslaunch main main.launch
```
Now, you should see Gazebo and rviz launching. Please note that Gazebo might take time to launch! 


### End Result
In the terminal, use the keyboard commands(u-i-o-j-k-l-m-,-.) and drive the robot around. The `red` trajectory represents the `Odom path` whereas the `green` trajectory represents the `EKF path`.


### Reference

This project has been done as part of Udacity Robotics software engineer nano degree programm
