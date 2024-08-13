# ROS-on-Jetson-Nano

Steps to Install ROS on Jetson Nano:


### 1.	Set Up Jetson Nano:

•	Flash the latest JetPack to an SD card and boot your Jetson Nano.

### 2.	Update the System:

```
sudo apt update
sudo apt upgrade
```
### 3.	Install Dependencies:

```
sudo apt install -y build-essential git curl
```
### 4.	Set Up ROS Repository:

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/ros-latest.list'
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
### 5.	Install ROS:

```
sudo apt update
sudo apt install ros-noetic-desktop-full
```
### 6.	Initialize rosdep:

```
sudo rosdep init
rosdep update
```
### 7.	Configure Environment:

```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```


You now have ROS installed on your Jetson Nano! You can start developing your robotics projects.
