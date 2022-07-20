# Autoware-results-fusion

This code change the output of the range_vision_fusion, original code outputs the detected results of the LIDAR or YOLO, depending on which one is empty. The original code returns the non-empty results.

This code, howwever, output the results if both LIDAR and YOLO results are non-empty.

In the second terminal, 
```
cd Autoware/src/autoware/core_perception/range_vision_fusion/src/
```
Replace this code with existing ```range_vision_fusion.cpp```


Go to Autoware
```
cd ~/Autoware
```
Rebuild the package by running 
```
colcon build --packages-select range_vision_fusion
```
Run regular carla-autoware.
