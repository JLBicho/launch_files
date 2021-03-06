# launch_files
Aggregate of launch files for different projects

## Tested in:
- ROS Kinetic
- Turtlebot3

## Index
1. [WiFi in zone](#wifi-in-zone)
2. [Save and load path](#save-and-load-path)

# WiFi in zone
This launch file uses the nodes found in: 

- exploration: https://github.com/JLBicho/exploration
- move_wp: https://github.com/JLBicho/move_wp
- wifi_mapping: https://github.com/JLBicho/wifi_mapping

### PC
`roscore`

`roslaunch turtlebot3_navigation turtlebot3_navigation map_file:=<your_map_file>`

`roslaunch launch_files wifi_in_zone.launch`

### Turtlebot
`roslaunch turtlebot3_bringup turtlebot3_robot`

`rosrun wifi_mapping wifi_signals_srv`

### Use
1) Once everything has correctly started, go to RViz and add the topics '/points', '/path', '/wifi_strength' to see them.

2) Select points in the map to form the polygon (with RViz **Publish Point**).

3) Publish in the topic '/start' the string "start". The points and path will now be shown in RViz.

4) Publish in the topic '/command' the string "next". The robot will start moving autonomously to each point, and retrieving the WiFi signal strength in each point.

### Demo
[![YouTube video demo](https://img.youtube.com/vi/JihOmws5eDw/0.jpg)](https://www.youtube.com/watch?v=JihOmws5eDw)

# Save and load path
### (In progress)
This launch file uses the nodes found in: 

- move_wp: https://github.com/JLBicho/move_wp
- path_utils: https://github.com/JLBicho/path_utils

### PC
`roscore`

`roslaunch turtlebot3_navigation turtlebot3_navigation map_file:=<your_map_file>`

### Turtlebot
`roslaunch turtlebot3_bringup turtlebot3_robot`


### Use
1) 

### Demo
[![YouTube video demo](https://img.youtube.com/vi/_WrC5S0jUaw/0.jpg)](https://www.youtube.com/watch?v=_WrC5S0jUaw)
