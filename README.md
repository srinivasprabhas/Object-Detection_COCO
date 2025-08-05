"""
# 🔍 Object Detection using OpenCV and SSD MobileNet

This project demonstrates real-time object detection using the **SSD MobileNet V3** model with OpenCV's `dnn` module. It processes both **static images** and **live webcam/video feed** to detect objects based on the **COCO dataset**.

---


## ⚙️ Functionalities

- Load and configure pre-trained **SSD MobileNet V3** model
- Read class labels from the COCO dataset
- Run detection on:
  - Static images
  - Webcam stream
  - Video input (code scaffolded for all three)
- Display object bounding boxes and labels on images
- Filter detections based on confidence threshold

---

## 🧠 Model and Classifier

- **Model**: `ssd_mobilenet_v3_large_coco_2020_01_14`
- **Framework**: OpenCV DNN module
- **Classifier**: Deep neural network detecting 80+ object categories from the **COCO dataset**

---

## 🏷️ Classes Detected

Objects include but are not limited to:
person, bicycle, car, motorcycle, airplane, bus, train, truck,
boat, traffic light, fire hydrant, stop sign, parking meter, ...

markdown
Always show details

Copy

> Full list is available in `Labels.txt`.

---

## 🖼️ Types of Inputs Supported

- Static image (e.g., `s1.jpg`)
- Webcam feed (via `cv2.VideoCapture(0)`)
- Video files (code placeholder present, easily extendable)

---

## 📈 Steps Followed in Code

1. **Import libraries** (`cv2`, `matplotlib`)
2. **Load Model & Config Files**
   - `.pb` → frozen graph
   - `.pbtxt` → model config
3. **Read COCO labels** from `Labels.txt`
4. **Model Setup**:
   - Input size: 320x320
   - Input scaling & normalization
   - RGB channel swap
5. **Detection**:
   - Read image/video
   - Use `model.detect()` with confidence threshold
   - Draw bounding boxes & label names on image
6. **Display Result**:
   - Use `matplotlib` for images
   - `cv2.imshow` for webcam/video stream

---
