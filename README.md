# Research Track II - Assignment 2: Jupyter Integration with ROS

## Overview

This project integrates ROS (Robot Operating System) with Jupyter notebooks to provide real-time visualization and control of a robot. It includes functionalities for setting and cancelling goals, tracking the robot’s position and velocity, and visualizing goals' statuses and robot trajectories. The system uses ROS topics and services for communication and `ipywidgets` along with `matplotlib` for visualization.

## Dependencies

- **ROS**: Requires ROS with necessary packages (e.g., `nav_msgs`, `geometry_msgs`, `sensor_msgs`, `assignment_2_2022`).
- **Python Libraries**:
  - `rospy`
  - `actionlib`
  - `matplotlib`
  - `ipywidgets`
  - `numpy`
  - `tf`
  - `math`

## Installation and Setup

1. **ROS Setup**: Ensure you have a ROS environment set up and the necessary ROS packages installed.
2. **Python Libraries**: Install the required Python libraries using pip:
   ```bash
   pip install matplotlib ipywidgets numpy
   ```
3. **Jupyter Notebook**: Install Jupyter Notebook if you haven’t already:
   ```bash
   pip install notebook
   ```
## Running the Notebook

1. **Start ROS Master**: Open a terminal and start the ROS master:
   ```bash
   roscore
   ```
2. **Run the Notebook**: Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
   Open the notebook file and run the cells sequentially.
   ```
   ## Key Components

### Node Initialization

- **Initializes** a ROS node named `user_input`.
- **Subscribes** to various ROS topics (e.g., `/odom`, `/scan`, `/reaching_goal/result`).
- **Sets up** publishers and action clients.

### Goal Status Check

- **Monitors** the status of goals (whether they are cancelled or reached) and updates lists and widgets accordingly.

### Visualization

- **`Visualiser` Class**: Handles plotting of robot path, current position, target positions, and goal statistics.
  - Uses `matplotlib` for plotting.
  - Animated plots are updated in real-time.

### Odometry Callback

- **Processes** odometry data to update position and velocity widgets.
- **Publishes** custom `Position_velocity` messages.

### Goal Setting and Cancellation

- **Provides** widgets for setting and cancelling goals.
- **Updates** ROS goals and handles button interactions.

### Laser Scanner

- **Processes** laser scan data to display minimum distance and angle information.

### Widgets

- **Current Position and Velocity**: Displays current position and velocity of the robot.
- **Goal Setting**: Sliders and buttons to set or cancel goals.
- **Laser Scanner**: Displays distance and angle from the laser scanner.

## Usage

1. **Set Goals**: Adjust the sliders and click the 'SET GOAL' button to set a target position for the robot.
2. **Cancel Goals**: Click the 'CANC GOAL' button to cancel the current goal.
3. **View Data**: Observe real-time updates on the robot's position, velocity, and the trajectory plot.
4. **Laser Data**: Check laser scanner data for distance and angle information.

## Example

```python
# Example of setting a goal
x_position.value = 5.0
y_position.value = 3.0
setting_button_clicked(setting_button)
```

# RT2_assignment3.pdf
In the RT2_assignment3.pdf, it is described:

---

**Research Track II - Assignment 3 Overview**

For this assignment, we were required to perform a statistical analysis based on the robotics simulator developed in the first assignment of Research Track I. This involved comparing my implementation with that of a colleague, Pisano Davide (S4363394). The simulator, designed to operate in a 2D environment, was tasked with pairing silver tokens next to golden ones. 

Our experiments focused on modifying the visual aspects of the arena to assess the performance of two different robotic controllers. By analyzing the results from both implementations, we aimed to identify any significant performance differences and evaluate the relative strengths and weaknesses of each approach.

---



   
