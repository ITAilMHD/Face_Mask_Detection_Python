
# **Face Mask Detection with Python** 😷

🔍 **Face_Mask_Detection_Python** is a real-time face mask detection system using **OpenCV** and **TensorFlow/Keras**. It detects faces from a webcam or IP camera and predicts whether a person is wearing a mask or not using a pre-trained deep learning model.

---

## **✨ Features**

* 🎥 Supports both **webcam** and **IP camera** streams.
* 🤖 Face detection with **OpenCV DNN Face Detector**.
* 🧠 Mask prediction using a pre-trained **Keras CNN model**.
* 🟢 Green box for **Mask detected**.
* 🔴 Red box for **No Mask detected**.

---

## **📂 Project Structure**

```
Face_Mask_Detection_Python/
│── face_detector/  
│   ├── deploy.prototxt  
│   ├── res10_300x300_ssd_iter_140000.caffemodel  
│── mask_detector.model  
│── face_mask_detection.py  
│── README.md  
```

---

## **⚙️ Requirements**

Install the required Python libraries before running:

```bash
pip install opencv-python
pip install tensorflow
pip install keras
pip install numpy
```

---

## **🚀 How to Run**

1. Make sure the following model files are available:

   * `face_detector/deploy.prototxt`
   * `face_detector/res10_300x300_ssd_iter_140000.caffemodel`
   * `mask_detector.model`

2. Run the script:

   ```bash
   python face_mask_detection.py
   ```

3. A video window will appear showing detection results:

   * ✅ **Mask** → Green box
   * ❌ **No Mask** → Red box

4. Press **Q** to exit.

---

## **📷 Camera Settings**

* The script is currently configured for an **IP camera**:

  ```python
  url = "http://192.168.34.176/cam-lo.jpg"
  ```
* To use the **laptop webcam** instead, replace it with:

  ```python
  vid = cv2.VideoCapture(0)
  ```

---

## **📝 Notes**

* `mask_detector.model` must be pre-trained for mask classification.
* Performance can be improved with **GPU acceleration**.
* Tested on **Python 3.7+**.

