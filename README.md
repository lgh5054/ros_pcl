# ros_pcl

## Requirements

### Environment
- Nvidia Jetson TX2 (tegra-ubuntu)
- ROS Kinetic Kame (ubuntu 16.04)
- PCL: 1.8.1
- CUDA(Optional)

### Install dependencies for ubuntu 16.04

```
sudo apt-get install libbullet-dev
```

```
cd ~
git clone https://github.com/orocos/orocos_kinematics_dynamics iso_ws/src
cd iso_ws/src
catkin_init_workspace
cd ..
catkin_make_isolated
source devel_isolated/setup.bash
```

### Build PCL (Point Cloud Library) ROS interface 

```
cd ~
git clone https://github.com/twailurus/ros_pcl.git
cd ros_pcl/src
git submodule init
git submodule update 
catkin_init_workspace
cd ..
catkin_make -j2
source devel/setup.bash
```

### How to Use

```
cd [your_workingspace]
```
Modify CMakeLists.txt
```
find_package(catkin REQUIRED COMPONENTS
  pcl_ros
  roscpp
  sensor_msgs
)
```
Remember also modify your package.xml

See also [ROS Document, pcl_ros](http://wiki.ros.org/pcl_ros)
