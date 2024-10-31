Author Yifeng Gong
Email yxg553@gmail.com (Don't hesitate to contact me for any help)
Date 10/31/2024
System Ros2 Foxy

I recommend to learn how to use ros2 at https://docs.ros.org/en/foxy/Tutorials.html. There are many Youtube tutorials but I feel that this tutorial document is the best. 

How to use after installing ros2 foxy in terminal:
1. cd MRCrab_ws (Go to the MRCrab_ws file)
2. source install/setup.bash (Set up the ros2 environment. You have to source everytime when you open a new terminal)
3. cd launch (Go to the launch file)
4. ros2 launch MR_Crab_Launch.py (Run all nodes in one terminal based on this launch file. Otherwise you have to run 5 terminals to run 5 nodes)

The structure of the ROS2 controller:
1. GUI Node (ros2 run GUI GUI) (it contains a GUI, a current subscriber, a vision subscriber, a gait generate client, a gait control client)
2. Current Publish Node (ros2 run current_pubsub pub_curr)
3. Vision Publish Node (ros2 run camera_pubsub cam_publisher)
4. Gait Generate Service Node (ros2 run gait srv_gait)
5. Gait Control Service Node (ros2 run gait srv_control)
There are other nodes but only for testing.
6. Message interfaces are placed in MRCrab_ws/src/interfaces

All of Nodes are placed in MRCrab_ws/src. For example, the GUI node can be found in MRCrab_ws/src/GUI/GUI/GUI_node. There is no need to change any file in MRCrab_ws/build or install or log files. Once you change any node file such as MRCrab_ws/src/GUI/GUI/GUI_node. Remember to "colcon build" in /MRCrab_ws/ to rebuild the build/install/log files.
