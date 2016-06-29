# Vicon_to_ROS
ROS package which receives Vicon data from the AML Windows XP computer and publishes a ROS PoseStamped topic.

Questions: gareth.dicker@mail.mcgill.ca

Tested stable on Ubuntu 14.04 with ROS Indigo but should be backward compatible to Hydro and Groovy.

Instructions:

1. Create a folder in your catkin_ws/src called /simple_udp.
1. Unzip these files into catkin_ws/src/simple_udp.
2. Navigate to catkin_ws/src/simple_udp and run the command 'rosmake' (this is an older package). You should see 51 built 0 failures.
3. Navigate to catkin_ws and run 'catkin_make'. You should see this package is built.
4. To run the node, do 'roslaunch simple_udp vicon_udp.launch' from any folder. 
5. Do 'rostopic list' and 'rostopic echo vicon_pose' to validate the topic is active.

NOTE: This package requires you are properly streaming Vicon data from the AML Windows XP computer. 
