# Fusion
Fusion of LiDAR and Camera 

We used
- vlp 16 lidar 
- logitech stream camera

## Preparation
YOLOv3 and tracking : 
LiDAR tracking :

## Fusion Result 
![](https://i.esdrop.com/d/ZklKfna5T3.jpg)

## Download the code
There is release version of Fusion code.
Paste it in /catking_ws/src/.

## Run 
in catking_ws

'''
catkin_make -DCMAKE_BUILD_TYPE=Release
source devel/setup.bash
rosluanch fusion_car_tracking fusion.launch
'''

Before run the fusion code, please check the yolov3 and lidar tracking code.
