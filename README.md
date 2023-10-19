# ROS-Python-Utilities
This repository hosts a collection of Python utility scripts and tools for simplifying common tasks in the Robot Operating System (ROS). 

# odom_to_path.py (ROS Odometry to Path Converter)

This Python script is designed to convert ROS `nav_msgs/Odometry` messages into `nav_msgs/Path` messages. It subscribes to a ROS odometry topic and publishes a ROS path topic. This conversion is useful for visualizing and tracking the odometry information in RViz, making it easier to monitor and analyze robot or vehicle movement.

[![odom_to_path](https://img.youtube.com/vi/4Y9ndViLJgQ/0.jpg)](https://www.youtube.com/watch?v=4Y9ndViLJgQ)

## Usage

To use this script, follow these steps:

1. Modify these lines to specify the actual names of your ROS topics in the script:

   ```python
   self.gt_path_pub = rospy.Publisher("path_topic_name", Path, queue_size=2)
   self.gt_poses = rospy.Subscriber('odom_topic_name', Odometry, self.gtcallback)

Replace "odom_topic_name" with the name of your ROS odometry topic and "path_topic_name" with the name of your ROS path topic.
