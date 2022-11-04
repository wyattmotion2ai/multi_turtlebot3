

Setup turtlebots as found on noetic docs, setup docker image on server

On server:
```roscore```

on turtlebot1:
```ROS_NAMESPACE=turtlebot01 roslaunch turtlebot3_bringup turtlebot3_robot.launch multi_robot_name:="turtlebot01" set_lidar_frame_id:="turtlebot01/base_scan"```


if turtlebot2, on it:
```ROS_NAMESPACE=turtlebot02 roslaunch turtlebot3_bringup turtlebot3_robot.launch multi_robot_name:="turtlebot02" set_lidar_frame_id:="turtlebot02/base_scan"```


wait for them to fully launch...


Back on server:
```roslaunch turtlebot3_navigation robots.launch```