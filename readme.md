How to run?
==================

1) Calibrate camera or check if the file exists.
```
$ cd ~/.ros/camera_info && ls
	logitech.yaml
```

2) Launching usb_cam

	For local computer:

		$ roslaunch red_cvision usb_cam_local_0.launch 
	
	where "0" is a number of /dev/video*

	For computer of youbot:

		$ roslaunch red_cvision usb_cam_youbot_0.launch 
	
3) Launching CV program

	$ rosrun red_cvision talker.py -l 555

	where "-l 555" is distance in [mm] from camera to surface.

4) [just for check] Getting objects

For getting objects from frame of camera you need send to service /get_list_objects Empty message:

	$ rosservice call /get_list_objects "{}" 

5) [just for enjoy] See image

	$ rosrun image_view image_view image:=/see_main

Have fun!
