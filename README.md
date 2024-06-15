![image](https://github.com/Ankitpatil9901/Hand-Gesture-Recognition-and-Analysis/assets/96898434/9516a41a-2f1c-40bd-95c9-affb02386a4b)# Hand Gesture Recognition with MediaPipe

**Abstract**  
In the realm of computer vision, hand gesture recognition plays a vital role in tasks such as sign language interpretation and enhancing human-computer interaction. This project explores hand gesture analysis, focusing on estimating hand positions and recognizing motions using Python's MediaPipe. Current methods are promising but lack the ability to store learned data points. This project aims to address this limitation by introducing a feature that enables the saving of the training dataset. By enhancing the adaptability and flexibility of hand gesture recognition systems, this approach seeks to advance the field with improved performance and versatility.

**Keywords**  
`MediaPipe`, `Hand Recognition`, `Finger Tracking`, `Deep Learning`, `TensorFlow`, `Computer Vision`

## Table of Contents

- [Introduction](#introduction)
- [Methodology](#methodology)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Hand gesture recognition is a critical component of the rapidly evolving field of computer vision. It has real-world applications ranging from enhancing human-computer interaction to supporting sign language interpretation. This project leverages Python's MediaPipe to advance gesture recognition by developing robust models for finger gesture identification and key point categorization. In addition to providing real-time inference, ease of integration, and versatility, our approach addresses previous methods' drawbacks by introducing an optimized model capable of storing the training dataset, essential for future iterations and improved model management.

## Methodology

### Overall Strategy

Our methodology for hand gesture identification using MediaPipe and OpenCV involves several key steps:

1. **Command-Line Argument Parsing**: Utilizes the `argparse` package for flexible specification of device settings, camera size, confidence criteria for hand detection and tracking, and the ability to toggle static picture mode.
   
2. **Camera Initialization**: Initiates camera capture using OpenCV (`cv.VideoCapture`) and sets width and height parameters according to user-defined settings.

3. **Model Initialization**: Initializes the hand detection model obtained from the MediaPipe package for precise hand recognition.

4. **Label Retrieval**: Uses CSV files as the basis for point history and key point classification, enabling accurate gesture analysis.

5. **Frame Rate Measurement**: Sets up a frame rate calculator (`CvFpsCalc`) to precisely measure frames per second for real-time performance evaluation.

6. **Historical Landmark Tracking**: Maintains a deque (`point_history`) with historical hand landmarks for motion tracking and contextual analysis.

7. **Finger Gesture History Logging**: Utilizes another deque (`finger_gesture_history`) to capture past finger gesture classifications, providing insights into gesture evolution.

8. **Main Loop Execution**: Retrieves camera frames and applies hand gesture recognition to each one in a continuous loop.

9. **Key Press Detection**: Detects key presses to enable mode switching or program termination, enhancing user control and engagement.

10. **Hand Landmark Detection**: Uses MediaPipe to detect hand landmarks and compute bounding box coordinates, forming the basis for gesture analysis.

11. **Data Pre-processing**: Pre-processes landmark coordinates into relative and normalized coordinates for uniform analysis.

12. **Data Logging**: Logs important point and landmark historical data into CSV files, based on the chosen mode.

13. **Visualization**: Draws bounding boxes, explanatory text, and detected hand landmarks onto the screen for improved interpretability and visual clarity.

14. **Display**: Shows the processed frame in a "Hand Gesture Recognition" window, offering an intuitive interface for gesture analysis.

15. **Cleanup Operations**: Releases the camera and closes all OpenCV windows upon pressing the ESC key, ensuring proper resource management and application termination.

## Results

The project establishes a foundation for hand gesture recognition by integrating essential modules for data collection, MediaPipe-based key point extraction, and basic gesture classification using scikit-learn's Support Vector Machine. While this provides a solid starting point, further development is required to build more sophisticated models and conduct thorough feature engineering. Future iterations may explore the incorporation of deep learning methodologies to enhance precision, real-time inference, smooth user interface integration, and resilient error management protocols.




## Installation

To set up the project, follow these steps:

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/hand-gesture-recognition.git
   cd hand-gesture-recognition
   ```

2. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

   Ensure you have Python and `pip` installed. Dependencies include:
   - `mediapipe`
   - `opencv-python`
   - `numpy`
   - `pandas`
   - `scikit-learn`

3. **Run the Application**

   ```bash
   python hand_gesture_recognition.py
   ```

## Usage

1. **Command-Line Arguments**: Customize device settings, camera size, and other parameters using command-line arguments.

   ```bash
   python hand_gesture_recognition.py --camera 0 --width 640 --height 480 --confidence 0.5
   ```

2. **Real-Time Gesture Recognition**: Run the script to perform real-time hand gesture recognition through your webcam.

3. **Data Logging**: The system logs landmark data and gesture history into CSV files for further analysis.

## Future Work

This project sets the stage for ongoing development in hand gesture recognition. Future work will focus on:
- Integrating deep learning models for enhanced accuracy.
- Incorporating real-time inference and user interface improvements.
- Developing robust error handling and management protocols.
- Exploring additional hand gestures and motion patterns.

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) for more information on how to get involved in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to customize further based on the specifics of your project and add any additional sections as needed.
