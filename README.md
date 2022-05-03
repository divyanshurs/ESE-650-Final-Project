# thegradreadme
# Leveraging mobile sensor suite for SLAM
## Team Members:
#### Divyanshu Sahu : Camera integration pipeline, ROS framework setup, ORB SLAM 2
#### Yug Ajmera : Camera callibration pipleine, Camera Imu Callibration framework, developing Mono-SLAM, inertial slam survey
#### Vanshil Shah : Imu integration pipeline and ORB SLAM 3

List of common errors and there solution while building the repository

- Open cv errors list(3.2.0)
https://stackoverflow.com/questions/46884682/error-in-building-opencv-with-ffmpeg
https://stackoverflow.com/questions/40262928/error-compiling-opencv-fatal-error-stdlib-h-no-such-file-or-directory

- Building orb slam with opencv (3.2.0)
Opencv not found
https://blog.csdn.net/gxsheen/article/details/79090454

- Slots reference error
https://github.com/UZ-SLAMLab/ORB_SLAM3/issues/387

- Misc issues
http://blog.leanote.com/post/gaunthan/ORB-SLAM2-compiling-problems

- Monochromatic clock steady clock
https://www.codeleading.com/article/98155731208/

- Adding path after building orb slam
export ROS_PACKAGE_PATH=${ROS_PACKAGE_PATH}:/home/divyanshu/ORB_SLAM/

##### Camera callibration using Boofcv
[BoofCv]
##### Camera callibration using kalibr
[kalibr]
#### Steps to run the camera imu pipeline
Make sure you have installed the following android APK : IP_camera_driver and ROS_sensor_driver
Edit the example.launch file in ip_camera_package accordingly
```
source devel/setup.bash
roslaunch ip_camera_driver example.launch
```

#### Steps to run orb slam 2 ros
```
 rosrun orb_slam2_ros Mono /home/divyanshu/ORB_SLAM/ORB_SLAM_2_appliedAi/src/orb_slam_2_ros/orb_slam2/Vocabulary
```

#### Steps to run orb slam 3
```
rosrun ORB_SLAM3 Mono /home/divyanshu/ORB_SLAM/orbslam3_ws/src/ORB_SLAM3/Vocabulary/ORBvoc.txt /home/divyanshu/ORB_SLAM/orbslam3_ws/src/ORB_SLAM3/Examples_old/Monocular/real.yaml
```

For running on the simulation
#### Steps to run the simulation
```
roslaunch box_bot_gazebo s.launch
roslaunch box_bot_gazebo main_bookstore.launch
rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/box_bot/cmd_vel
```




[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
[dill]: <https://github.com/joemccann/dillinger>
  [BoofCv]: <https://boofcv.org/index.php?title=Main_Page>
  [kalibr]: <https://github.com/ethz-asl/kalibr>
  [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
