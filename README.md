# Emotion-Detection-with-Face# Facial Emotion Analysis using Deep Learning

This code performs facial emotion analysis using deep learning techniques to detect emotions from live video feed. The model used for emotion detection is loaded from a pre-trained Keras model (`best_model.h5`).

## Prerequisites

Make sure you have the following libraries installed:

- `numpy`
- `cv2` (OpenCV)
- `keras`
- `matplotlib`

You can install them using `pip`:

```
pip install numpy opencv-python keras matplotlib
```

## How to Use

1. Clone or download the repository containing the pre-trained model (`best_model.h5`) and this Python script (`emotion_detection.py`).

2. Load the pre-trained model:

```python
model = load_model("LOAD YOUR H5 FILE")
```

3. Run the script. It will open your webcam and start analyzing facial emotions in real-time.

4. Press the 'q' key to stop the live video feed and close the application.

## Description

The code uses the OpenCV library to capture video from the webcam and detect faces in each frame using the Haar Cascade Classifier (`haarcascade_frontalface_default.xml`). Once a face is detected, the region of interest (ROI) containing the face is cropped, resized, and passed through the pre-trained Keras model for emotion prediction.

The emotions recognized by the model are:
- Angry
- Disgust
- Fear
- Happy
- Sad
- Surprise
- Neutral

The predicted emotion is then displayed as text on top of the live video feed.

Note: It is recommended to run this code on a machine with a webcam connected.

## Troubleshooting

If you encounter any issues with the code, make sure you have installed all the required libraries and have the model file (`best_model.h5`) available in the specified location. If the model file is missing or the path is incorrect, the code will raise an error.

Also, make sure that your webcam is properly connected and accessible by the code.

Enjoy analyzing facial emotions in real-time using this Python script! Feel free to modify and extend the code as per your requirements. Happy coding!
