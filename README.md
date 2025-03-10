# Gesture Recognition & Desktop Control

This repository contains a complete pipeline for collecting hand gesture data, training a neural network model (using an MLP) to recognize gestures, and using the trained model for real-time desktop control. The code is implemented in Python with Jupyter Notebook and leverages libraries such as OpenCV, MediaPipe, TensorFlow, and more. It is designed to be easy to understand and modify.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

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
