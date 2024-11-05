# Mobile Robot with Robotic Arm Project

This repository contains a ROS2-compatible mobile robot project equipped with a robotic arm. The project includes URDF and Xacro files to define the robot's base and arm, along with configurations for visualizing and simulating the entire system in RViz. This setup is ideal for learning robotic modeling and visualization, and it provides a robust foundation for developing ROS2-based mobile manipulator applications.

## Table of Contents
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Files and Directories](#files-and-directories)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Robot Base and Arm Model**: A complete mobile manipulator, including both a mobile base and a multi-joint robotic arm, defined in URDF and Xacro for modular and flexible configuration.
- **Joint and Link Control**: Predefined configurations for controlling and visualizing the arm’s movement and each joint’s range.
- **Sensor Modeling**: Integrates common sensors, such as LiDAR and cameras, to support navigation and object detection.
- **RViz Visualization**: Configurations for visualizing the full robot with base, arm, and sensors in RViz, complete with interactive markers for arm manipulation.
- **ROS2 Integration**: Fully compatible with ROS2, allowing for navigation, manipulation, and sensor data processing.

## Requirements
- **ROS2**: Tested with ROS2 Humble.
- **RViz**: For 3D visualization of the robot, arm, and sensors.
- **Xacro**: Used for modular URDF creation and parameterization.

## Installation
1. Ensure that ROS2 is installed on your system. Follow the [ROS2 installation guide](https://docs.ros.org/en/ros2).
2. Clone the repository into your ROS2 workspace:
   ```bash
   cd ~/ros2_ws
   git clone https://github.com/yourusername/mobile_robot_arm_project.git
   ```
3. Build the workspace:
   ```bash
   colcon build
   ```
4. Source the workspace:
   ```bash
   source ~/ros2_ws/install/setup.bash
   ```

## Usage
1. **Launch the Mobile Robot and Arm in RViz**:
   After sourcing the workspace, run the following command to launch the robot model with the arm in RViz:
   ```bash
   ros2 launch mobile_robot <node_name>
   ```

2. **Control the Robotic Arm**:
   - Use interactive markers in RViz to control the arm’s joints.
   - Or, adjust joint configurations in the `.xacro` files to set predefined positions.

3. **Add Sensors or Modify the Robot Arm**:
   - Customize the robotic arm or add additional sensors by modifying the URDF and Xacro files in the `urdf/` directory.

## Files and Directories
- **`urdf/`**: Contains URDF and Xacro files defining both the mobile base and the robotic arm. Edit these files to adjust robot dimensions, add or remove components, or modify the arm's reach and joints.
- **`launch/`**: Launch files to initiate RViz with the robot and arm models.
- **`config/`**: Contains RViz configuration files to load the full robot model with sensors and arm into RViz for visualization.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
