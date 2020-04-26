# launch_files
Aggregate of launch files for different projects

## Tested in:
- ROS Kinetic
- Turtlebot3

# wifi_in_zone.launch

This launch file uses the nodes found in: 

- explotation: https://github.com/JLBicho/exploration
- move_wp: https://github.com/JLBicho/move_wp
- wifi_mapping: TO BE UPLOADED

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


