# pYOLO

A MOOS-IvP app wrapping YOLOv5 for real-time object detection on autonomous surface vehicles. Built in summer 2023 at the West Point Robotics Research Center with [Deja Scott](https://github.com/dejaa1), [Logan Delaar](https://github.com/logandelaar1) and [Luke Baker](https://github.com/luke-baker24) for a maritime man-overboard search-and-rescue project.

- Full project (dataset, homography localization, missions): [dejaa1/SNR-yolo-moos-integration](https://github.com/dejaa1/SNR-yolo-moos-integration)
- Official copy of this app: [westpoint-robotics/pYolo](https://github.com/westpoint-robotics/pYolo)
- This repo is the development history of the wrapper. `pYOLO/yolo/` is a vendored copy of [ultralytics/yolov5](https://github.com/ultralytics/yolov5) (AGPL-3.0).

## Overview
This MOOS-ivp wrapper for YOLOv5 allows you to seamlessly integrate the YOLOv5 object detection capabilities into your MOOS-ivp applications or systems. By using this wrapper, you can leverage the power of YOLOv5 for real-time object detection.

## Usage
1. Place your custom model in: `pYOLO\yolo\custom_models`
2. Modify `input_source`, `weights`, and `python` in `pYOLO\YOLO.cpp` to reflect your web stream input source, your custom model, and the location of your python executable.

### Publishes
- BOX_X
  - The x-coordinate of the bottom middle of the bounding box in the image where an object is detected.
- BOX_Y
  - The y-coordinate of the bottom middle of the bounding box in the image where a object is detected.
- DETECTED 
  - A boolean value indicates whether a object is detected (true) or not (false).
- CONF:
  - The confidence level of the object detection
- CLASS_LABEL
  - The label of the detected class in the image
