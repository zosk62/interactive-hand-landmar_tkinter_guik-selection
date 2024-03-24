# interactive-hand-landmar_tkinter_guik-selection
**Hand Detector App**

This application uses OpenCV and MediaPipe to detect hands in real-time video and display them on a Tkinter canvas. It also allows you to select a specific landmark on the detected hand and highlight it.

**Features**

* Real-time hand detection using MediaPipe
* Hand landmark detection and visualization
* Ability to select and highlight a specific landmark on the hand

**Getting Started**

1. **Prerequisites**
    * Python 3.x
    * OpenCV (`pip install opencv-python`)
    * MediaPipe (`pip install mediapipe`)
    * Tkinter (included in Python standard library)


**Explanation of the Code**

The code is divided into three main parts:

1. **`HandDetectorApp` class:**
    * This class handles the Tkinter GUI and application loop.
    * It creates a canvas to display the video feed and labels for FPS.
    * It has a button to toggle highlighting a specific landmark and an entry field to enter the landmark ID (replaced with landmark selection functionality).
    * The `update` method continuously reads frames from the video capture, processes them using the `handDetector` class, and updates the canvas with the new frame.

2. **`handDetector` class:**
    * This class handles hand detection and landmark processing using MediaPipe.
    * It takes various parameters for hand detection configuration like mode, maximum number of hands, and detection/tracking confidence.
    * The `findHands` method detects hands in a frame and optionally draws the landmarks on the frame.
    * The `findPosition` method extracts the landmark positions for a specific hand and optionally draws circles around them.
    * The `highlight_landmark` method highlights a specific landmark on the hand with a colored circle.

3. **`main` function:**
    * This function creates a video capture object, a Tkinter root window, and an instance of the `HandDetectorApp` class.
    * It starts the Tkinter event loop, which continuously calls the `update` method of the `HandDetectorApp` class to process video frames.

**Using the GUI App**

1. Run the application using the instructions above.
2. The application window will display the webcam feed with detected hands.
3. Click on a landmark on the hand displayed on the canvas. The selected landmark will be highlighted with a green circle.


