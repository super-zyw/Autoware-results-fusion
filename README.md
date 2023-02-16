# Autoware-results-fusion

This code change the output of the range_vision_fusion, original code outputs the detected results of the LIDAR or YOLO, depending on which one is empty. The original code returns the non-empty results.

This code, however, output the results if YOLO result is non-empty. The code checks if YOLO detection is empty by adding the condition ```in_vision_detections->objects.empty()```, and publish the empty fusion_objects to force an empty costmap  

In the second terminal, 
```
cd Autoware/src/autoware/core_perception/range_vision_fusion/src/
```
There is a ``` range_vision_fusion.cpp```. Replace it with the code in this repository.



Go to Autoware
```
cd ~/Autoware
```
Rebuild the package by running 
```
colcon build --packages-select range_vision_fusion
```
Run regular carla-autoware.
