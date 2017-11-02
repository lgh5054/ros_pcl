# ros_pcl

## Requirements

### Environment
- ROS Kinetic Kame (Ubuntu 16.04)
- PCL: 1.8.1
- CUDA(Optional)

### Install dependencies for Ubuntu 16.04

```
sudo apt-get install libbullet-dev
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
