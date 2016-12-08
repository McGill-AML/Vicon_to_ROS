# Vicon_to_ROS
ROS package which receives Vicon data from the AML Windows XP computer and publishes a ROS PoseStamped topic.

Questions: gareth.dicker@mail.mcgill.ca

Tested stable on Ubuntu 14.04 with ROS Indigo but should be backward compatible to Hydro and Groovy.

# Linux Receiving Computer Instructions:

1. Make sure connected to SharfNahon Wifi Network
2. Create a folder in your catkin_ws/src called /simple_udp.
3. Unzip these files into catkin_ws/src/simple_udp.
4. Navigate to catkin_ws/src/simple_udp and run the command 'rosmake' (this is an older package). You should see 51 built 0 failures.
5. Navigate to catkin_ws and run 'catkin_make'. You should see this package is built.
6. To run the node, do 'roslaunch simple_udp vicon_udp.launch' from any folder. 
7. Do 'rostopic list' and 'rostopic echo vicon_pose' to validate the topic is active.

NOTE: This package requires you are properly streaming Vicon data from the AML Windows XP computer. 

# AML Windows XP Computer Instructions:
1. Open Vicon IQ
2. Select or edit Active Objects
3. Open C:\ViconUDPStreamer\ViconStreamer.conf
4. Change last row IP address to Linux Receiving Computer IP Address (make sure it is on the SharfNahon Wifi network!)
5. Run C:\ViconUDPStreamer\Vicon_UDP_stream.exe VERBOSE SYSTEM_TIME
