# googlecartoinstaller
Simplified installer for Google Cartographer. This package is for educational and learning purpose only to simplify the installation process for the new machine. 

# Dependency 

1. ROS Noetic

# Installation

1. Create catkin_ws if you have not done this: 
```
cd ~
mkdir -p ~/catkin_ws/src
cd ..
catkin_make
```
Please ensure it is compiled successfully. 

2. Download and run the installer: 

Type N for Noetic of M for Melodic as instructed and enter Sudo password. 

```
cd ~
git clone https://github.com/aizzat/googlecartoinstaller
cd ~/googlecartoinstaller
chmod +x cartoinstallaizzat
./cartoinstallaizzat

#after finish installing run this:
source $HOME/catkin_ws/install_isolated/setup.bash
```
# To test run: 

Download and launch the 2D demo: 
```
wget -P ~/Downloads https://storage.googleapis.com/cartographer-public-data/bags/backpack_2d/cartographer_paper_deutsches_museum.bag
source $HOME/catkin_ws/install_isolated/setup.bash
roslaunch cartographer_ros demo_backpack_2d.launch bag_filename:=${HOME}/Downloads/cartographer_paper_deutsches_museum.bag
```


Download and launch the 3D backpack demo: 
```
wget -P ~/Downloads https://storage.googleapis.com/cartographer-public-data/bags/backpack_3d/with_intensities/b3-2016-04-05-14-14-00.bag 
source $HOME/catkin_ws/install_isolated/setup.bash
roslaunch cartographer_ros demo_backpack_3d.launch bag_filename:=${HOME}/Downloads/b3-2016-04-05-14-14-00.bag
 ```


