Project Title: Driver Drowsiness Detection System

Description:

The Drowsiness Detection System is a Python-based application that uses computer vision and deep learning techniques to monitor a person's eyes and detect signs of drowsiness in real-time. The system captures video from a webcam, analyzes the individual's facial features (particularly the eyes), and triggers an alarm if drowsiness is detected. The application incorporates pre-trained models for face and eye detection, along with a Convolutional Neural Network (CNN) model to classify eye states as open or closed.

Key Features:

Real-Time Video Processing:

Captures video frames from the webcam in real-time, allowing continuous monitoring of the user's face and eyes.
Haar Cascade Classifiers:

Utilizes pre-trained Haar Cascade classifiers for face, left eye, and right eye detection, providing a foundation for subsequent analysis.
Convolutional Neural Network (CNN) Model:

Loads a pre-trained CNN model (cnncat2.h5) for eye state classification (open or closed).
Processes individual eye regions to determine their state based on the CNN predictions.
Scoring System:

Implements a scoring mechanism to track the user's eye state over time.
Increments the score when both eyes are detected as closed and decrements it when at least one eye is open.
Visual Feedback:

Displays real-time feedback on the video frame, indicating whether the eyes are open or closed.
Dynamically adjusts the displayed score based on the user's eye state.
Alarm Trigger:

Triggers an alarm (audio beep) and increases the thickness of a red border around the video frame when the accumulated score surpasses a predefined threshold.
Provides a visual and audible alert to notify the user of potential drowsiness.
Image Capture on Alarm:

Captures a still image (image.jpg) of the user's face when the alarm is triggered, allowing for further analysis and documentation.
Pygame Audio Library Integration:

Utilizes the Pygame library (mixer) to play an audio alarm ('alarm.wav') when drowsiness is detected.
Ensures compatibility with audio playback on various platforms.
Dynamic Alarm Adjustment:

Dynamically adjusts the thickness of the red border around the video frame to emphasize the alarm state without obstructing the view excessively.
User Interaction:

Displays information, such as the user's score and eye state, on the video frame.
Prompts the user to press 'q' to exit the application.
Modularity and Reusability:

Organizes functionalities into functions and loops, promoting code modularity and reusability.
Adopts an object-oriented approach for cleaner code organization.
Error Handling:

Implements error handling to gracefully handle potential exceptions during audio playback, ensuring a more robust application.
