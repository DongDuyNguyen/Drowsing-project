# Drowsiness Detection using Transfer Learning and OpenCV Haar Cascades

## Overview

This project implements a **drowsiness detection system** by utilizing **Transfer Learning (MobileNet)** and **OpenCV Haar Cascades**. The goal is to monitor and detect signs of drowsiness in a person using their facial landmarks, particularly focusing on their eye state (open or closed). The system can be used in real-time applications like driver monitoring, where detecting drowsiness is crucial to prevent accidents.

### Key Components:
- **Haar Cascades**: Used for face and eye detection.
- **MobileNet**: Pre-trained convolutional neural network used via transfer learning to classify eye states (open or closed).
- **OpenCV**: A popular computer vision library used for real-time video processing.

## Features

- **Face and Eye Detection**: Utilizes Haar Cascades for detecting faces and eyes in video streams or images.
- **Eye State Classification**: Uses a fine-tuned MobileNet model to classify the eyes as "open" or "closed" based on real-time video frames.
- **Real-time Drowsiness Detection**: Continuously monitors the eye state to determine if the person is drowsy based on prolonged periods of closed eyes.
- **Alert System**: When drowsiness is detected, the system can trigger an alert (such as a beep or visual indicator).

## How it Works

1. **Face and Eye Detection**:
   - Haar Cascades are used to detect the region of interest (ROI) where the face and eyes are located.
   - Once the eyes are detected, the ROI is passed to the MobileNet model for classification.

2. **Eye State Classification with Transfer Learning (MobileNet)**:
   - A pre-trained MobileNet model is fine-tuned on a dataset of eye images (open and closed).
   - The MobileNet model predicts whether the eyes in the detected region are open or closed.
   
3. **Drowsiness Detection Logic**:
   - If the eyes remain closed for a certain period (e.g., 2-3 seconds), the system flags the user as drowsy.
   - An alert is triggered to notify the user.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/drowsiness-detection
   cd drowsiness-detection
