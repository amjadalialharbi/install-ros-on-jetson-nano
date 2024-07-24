# install-ros-on-jetson-nano
Steps to install ros on jetson nano

## introduction:
- ROS (Robot Operating System) on Jetson Nano helps in building and developing robotics software using the device's AI capabilities. ROS provides tools and libraries that enable communication between robot components, while Jetson Nano offers fast data processing using GPU technology. This combination is suitable for applications like computer vision and AI in robotics.

## how to install ROS on Jetson Nano:

### 1. Update the System:
   
   Ensure all packages are up to date.
   ```
   sudo apt update
   sudo apt upgrade
   ```

### 2. Add ROS Repository Key:
   
   Add the ROS GPG key to your system.
   ```
   sudo apt install curl
   curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
   ```
### 3. Add ROS Repository to Sources List:
```
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu
     $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   ```



### 4. Update Package Lists:
```
   sudo apt update
```

 ### 5. Install ROS:
   Choose the desired version. For the full desktop version of ROS (Desktop-Full Install):
   ```
   sudo apt install ros-melodic-desktop-full
   ```
### 6. Initialize rosdep:
```
   sudo rosdep init
   rosdep update
 ```

### 7. Set Up ROS Environment:
   Add ROS to your environment variables.
   ```
   echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   ```

### 8. Install ROS Build Tools:
```
   sudo apt install python-rosinstall python-rosinstall-generator python-wstool build-essential
 ```
### These steps will help you install ROS on your Jetson Nano. You can now start using ROS for your robotics projects.
