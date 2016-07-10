zed_cpu_ros
===========
A simple zed camera driver which only use CPU and only publish left and right raw images and its camera info.

# Useage:
1. git the packge into your working space
2. find your zed calibration files in
    ```
    	cd /usr/local/zed/settings
    ```

	or download from:
	http://calib.stereolabs.com/?SN=XXXX

	Node: XXXX is your last four digit S/N of your camera, change it !!

3. put the .conf file into zed_cpu_ros/config folder

4. update launch file configuration file name in zed_cpu_ros.launch into your SNXXXX.conf
    ```
    roscd zed_cpu_ros/launch
    ```
5. launch the code
    ```
    roslaucnh zed_cpu_ros zed_cpu_ros.launch
    ```
## Launch file parameters

 Parameter                    |           Description                                       |              Value          
------------------------------|-------------------------------------------------------------|-------------------------           
 resolution                   | ZED Camera resolution                                       | '0': HD2K                   
 _                            | _                                                           | '1': HD1080                 
 _                            | _                                                           | '2': HD720                  
 _                            | _                                                           | '3': VGA                                    
 frame_rate                   | Rate at which images are published                          | int                                             
 left_frame_id                | Left Frame ID                                               | string        
 right_frame_id               | Right Frame ID                                              | string        
 config_file_location         | The location of ZED calibration file                        | string        
 show_image                   | Wether to use opencv show image                             | bool        

# TODO:

1. add the launch file for stereo_proc.
2. add the nodelet function.

# Transcend Robotics:
Patented articulated traction control ARTI technology for stair climbing and obstacle traversal without complex software or controls
http://transcendrobotics.com/

# Authour:
Di Zeng	