# ros_pcl

## Requirements

### Environment
- ROS Melodic Morenia (Ubuntu 18.04)
- PCL: 1.9.1
- CUDA(Optional)

### Install dependencies for Ubuntu 18.04

```
rosdep install -y --from-paths src --ignore-src --rosdistro $ROS_DISTRO
```

### How to Build
```
git clone https://github.com/twailurus/ros_pcl.git
cd ros_pcl/src
git submodule init
git submodule update 
catkin_init_workspace
cd ..
catkin_make
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
