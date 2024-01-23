# YOLO app
This MOOS-ivp wrapper for YOLOv5 allows you to seamlessly integrate the YOLOv5 object detection capabilities into your MOOS-ivp applications or systems. By using this wrapper, you can leverage the power of YOLOv5 for real-time object detection.

### Publishes:
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
