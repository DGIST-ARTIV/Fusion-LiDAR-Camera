# Fusion
Fusion of LiDAR and Camera 

We used
- VLP 16 LiDAR 
- Logitech stream camera

## Preparation
[LiDAR tracking](https://github.com/DGIST-ARTIV/Fusion-LiDAR-Camera/releases/tag/2.1.12)

[YOLO v3 and tracking](https://github.com/DGIST-ARTIV/VISION/tree/master/%EA%B0%9D%EC%B2%B4)

[Fusion](https://github.com/DGIST-ARTIV/Fusion-LiDAR-Camera/releases/tag/Fusion-V.2.0.9)

## Fusion Result 
![lidar-camera fusion](https://user-images.githubusercontent.com/42258047/112603687-b03d3680-8e58-11eb-8b0b-a8c307c6f01a.gif)

## Download the code
There is release version of Fusion code.
Paste it in /catking_ws/src/.

## Alignment

<img src = "https://user-images.githubusercontent.com/42258047/112604286-4bcea700-8e59-11eb-976a-e8c7d83d2989.png" width="200px"> <img src = "https://user-images.githubusercontent.com/42258047/112604280-4a9d7a00-8e59-11eb-9646-d51eba01009e.png" width="200px"> <img src = "https://user-images.githubusercontent.com/42258047/112604283-4b361080-8e59-11eb-8ba0-ac3882bee252.png" width="200px">

You can change the hres and vres in launch file. 

```
<launch>
    <node name="fusion_car_tracking" pkg="fusion_car_tracking" type="fusion_car_tracking" output="screen" respawn="true">
        <param name="hres" value="0.07480" />
        <param name="vres" value="0.101018" />
        <param name="y_fudge" value="120" />
        <param name="y_fudge2" value="-190" />
	<param name="map" value="0"/>
    </node>
</launch>
```

## Run 
in catking_ws

```
catkin_make -DCMAKE_BUILD_TYPE=Release
source devel/setup.bash
rosluanch fusion_car_tracking fusion.launch
```

Before run the fusion code, please check the yolov3 and lidar tracking code.


## Evaluation

<img src = "https://user-images.githubusercontent.com/25432456/112658768-121c9100-8e97-11eb-9724-2a191fafa971.png" width="500px">
Official Tracking_msg viewer will be provided


## Citation
#### Estimation of Closest In-Path Vehicle (CIPV) by Low-Channel LiDAR and Camera Sensor Fusion for Autonomous Vehicle
[arxiv PDF](https://arxiv.org/pdf/2103.13952.pdf)

[MDPI PDF](https://www.mdpi.com/1424-8220/21/9/3124)

```
@misc{bae2021estimation,
      title={Estimation of Closest In-Path Vehicle (CIPV) by Low-Channel LiDAR and Camera Sensor Fusion for Autonomous Vehicle}, 
      author={Hyunjin Bae and Gu Lee and Jaeseung Yang and Gwanjun Shin and Yongseob Lim and Gyeungho Choi},
      year={2021},
      eprint={2103.13952},
      archivePrefix={arXiv},
      primaryClass={cs.RO}
}
```

```

@Article{s21093124,
AUTHOR = {Bae, Hyunjin and Lee, Gu and Yang, Jaeseung and Shin, Gwanjun and Choi, Gyeungho and Lim, Yongseob},
TITLE = {Estimation of the Closest In-Path Vehicle by Low-Channel LiDAR and Camera Sensor Fusion for Autonomous Vehicles},
JOURNAL = {Sensors},
VOLUME = {21},
YEAR = {2021},
NUMBER = {9},
ARTICLE-NUMBER = {3124},
URL = {https://www.mdpi.com/1424-8220/21/9/3124},
ISSN = {1424-8220},
DOI = {10.3390/s21093124}
}
```

