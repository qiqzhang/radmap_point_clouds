# Merging the bags
1. Place port.bag, starboard.bag, imu.bag into a folder
2. roslaunch radmap_preprocess lasers.launch 
3. rosrun  rosrun radmap_preprocess lasers 
4. python [insert path]/src/bag_merge_radmap.py

# Coordinate frame calibration
1. velodyne_calib.m
2. fill in calibrated_tf.launch

# Play the bags
1. rosparam set use_sim_time true
2. roslaunch radmap_preprocess calibrated_tf.launch
3. rosbag play -- clock 
4. rviz