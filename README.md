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
echo "source ~/iso_ws/devel_isolated/setup.bash" >> ~/.bashrc
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
echo "source ~/ros_pcl/devel/setup.bash" >> ~/.bashrc
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

See also [ROS Document, pcl](http://wiki.ros.org/pcl/Overview)
