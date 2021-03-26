# Fusion
Fusion of LiDAR and Camera 

We used
- vlp 16 lidar 
- logitech stream camera

## Preparation
[YOLOv3 and tracking](https://github.com/DGIST-ARTIV/Lidar)
[LiDAR tracking](https://github.com/DGIST-ARTIV/VISION/tree/master/%EA%B0%9D%EC%B2%B4)

## Fusion Result 
![lidar-camera fusion](https://user-images.githubusercontent.com/42258047/112603687-b03d3680-8e58-11eb-8b0b-a8c307c6f01a.gif)

## Download the code
There is release version of Fusion code.
Paste it in /catking_ws/src/.

## Alignment

<img src = "https://user-images.githubusercontent.com/42258047/112604286-4bcea700-8e59-11eb-976a-e8c7d83d2989.png" width="200px"> <img src = "https://user-images.githubusercontent.com/42258047/112604280-4a9d7a00-8e59-11eb-9646-d51eba01009e.png" width="200px"> <img src = "https://user-images.githubusercontent.com/42258047/112604283-4b361080-8e59-11eb-8ba0-ac3882bee252.png" width="200px">

You can change the hres and vres in launch file. 

## Run 
in catking_ws

```
catkin_make -DCMAKE_BUILD_TYPE=Release
source devel/setup.bash
rosluanch fusion_car_tracking fusion.launch
```

Before run the fusion code, please check the yolov3 and lidar tracking code.
