# Gesture Recognition & Desktop Control

This repository contains a complete pipeline for collecting hand gesture data, training a neural network model (using an MLP) to recognize gestures, and using the trained model for real-time desktop control. The code is implemented in Python with Jupyter Notebook and leverages libraries such as OpenCV, MediaPipe, TensorFlow, and more. It is designed to be easy to understand and modify.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Customization](#customization)
- [Contributing](#contributing)


## Features

- **Data Collection:**  
  Captures hand gesture data (landmark coordinates) using MediaPipe and saves it as text files.

- **Model Training:**  
  Trains an MLP (Multi-Layer Perceptron) using TensorFlow/Keras to classify gestures such as open hand, fist, thumb up, thumb down, peace, and OK.

- **Real-Time Gesture Recognition:**  
  Uses the webcam feed to detect gestures in real time and performs corresponding desktop control actions:
  - **Mouse Control:** Move the cursor using an open hand.
  - **Clicking:** Perform left-click with a fist.
  - **Volume Control:** Increase or decrease system volume using thumb up and thumb down gestures.
  - **Application Switching:** Use the peace gesture to switch between open applications.
  - **Desktop View:** Use the OK gesture to minimize all windows and show the desktop.

- **Evaluation:**  
  Provides a section to evaluate the model’s accuracy on test data and measures the processing latency of a single frame.

## Installation

Before running the code, ensure you have Python 3.x installed. You can install the required libraries using pip. Open your terminal and run:

```bash
pip install opencv-python mediapipe tensorflow numpy matplotlib scikit-learn pyautogui pycaw comtypes
pip install msvc-runtime
```
# Usage
## Data Collection:

-Run the data collection cells in the notebook.
-For each gesture, the webcam will display the feed.
-Press s to start capturing data and q to quit.
-100 samples per gesture are automatically captured and stored.

## Model Training:

-After collecting data, the notebook loads and preprocesses the data.
-The MLP model is built and trained using the collected gesture data.
-Training and validation accuracy are plotted for quick feedback.
-The trained model is saved as gesture_model.keras.

## Real-Time Gesture Recognition & Desktop Control:

-The Code loads the trained model and uses it to predict gestures in real time.
-Depending on the detected gesture, corresponding desktop actions (mouse movement, clicking, volume control, etc.) are performed.

## Evaluation:

-The notebook includes a section that evaluates the model on a test set and prints the test accuracy.
-It also measures and displays the processing latency for a single frame.

## Code Structure
-Data Collection:
Captures hand landmarks from the webcam and saves them for each gesture.

-Model Training:
Loads and preprocesses data, splits it into training and test sets, builds the MLP, trains the model, and saves the trained model.

-Real-Time Gesture Recognition:
Uses MediaPipe and the trained model to recognize gestures from a live webcam feed and triggers desktop control actions accordingly.

-Evaluation:
Evaluates the trained model's performance and measures frame processing latency.

## Customization
This project is designed for easy modification:

->Add New Gestures:
Update the gestures list and add corresponding actions in the real-time control loop.

->Model Architecture:
Adjust the MLP layers, number of epochs, or batch size to experiment with model performance.

->Desktop Actions:
Customize or extend the desktop control actions (e.g., mouse movements, volume adjustments) as needed.

->Data Collection:
Change the number of samples or modify the user interface prompts for collecting gesture data.
Feel free to fork the repository and adapt the code to suit your requirements.

# Contributing
Contributions are welcome! If you find bugs, have suggestions, or want to add new features, please open an issue or submit a pull request.
