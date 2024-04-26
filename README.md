# ros2_basic

Study with ROS2 Programming

## Contents

- [Installation ROS2-humble](#Installation)  
Writing...

## Requirements

- OS: [Ubuntu 22.04 LTS - Jammy](https://releases.ubuntu.com/jammy/)
- C++
  - Clang: 11.4.0
  - GCC: 14.0.0
  - CMake: 3.22.1
- Python
  - Python3: 3.10.12
- ROS2
  - ROS2-humble

## Installation ROS2-humble

1. Open Your Terminal  

    ```
        locale  # check for UTF-8

        sudo apt update && sudo apt install locales
        sudo locale-gen en_US en_US.UTF-8
        sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
        export LANG=en_US.UTF-8

        locale  # verify settings
    ```

2. Setup Sources

   ```shell
    # Enable Ubuntu Universe repository
        sudo apt -y install software-properties-common
        sudo add-apt-repository universe

    # add GPG key
        sudo apt update && sudo apt -y install curl
        sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

    # add repository
        echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

    # Update & Upgrade
        sudo apt update && sudo apt upgrade
   ```

3. Install ROS2 packages

    ```shell
    # Install ROS2-humble-full
        echo "Install ROS2-humble-desktop!"
        sudo apt -y install ros-humble-desktop-full

    # Set_env
        source /opt/ros/humble/setup.bash

    # Install colcon
        sudo apt -y install python3-colcon-common-extensions
    ```

## Reference

[ROS2 Documentation: Humble](https://docs.ros.org/en/humble/index.html)
