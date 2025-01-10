---
title: "Drowsiness Detector"
excerpt: "Detecting drowsiness based on EAR values via OpenCV.<br/>"
collection: portfolio
---

[https://github.com/wesleymeredith/Drowsiness-Detection](https://github.com/wesleymeredith/Drowsiness-Detection)

This project was inspired by personal experiences during the gap year between my undergraduate and graduate studies. While attending night classes in computer science after my full-time research job at a laboratory in Raleigh, NC, I sometimes struggled to stay awake during Zoom lectures. This led me to design a drowsiness detector that monitors eye activity using a webcam and alerts users with an audio cue when signs of drowsiness are detected.  

The system relies on the **Eye Aspect Ratio (EAR)**, a metric detailed in [this paper](https://www.sciencedirect.com/science/article/pii/S2667241322000039#fig0001), to measure eye closure.

<img src='/images/eyes.jpg'>


### Setup & Installation  
This project is implemented in Python and leverages the following libraries:  
- **OpenCV**: For video processing and visualization.  
- **dlib**: To detect facial landmarks.  
- **pyttsx3**: To generate audio alerts.  
- **scipy**: For EAR/Euclidean distance calculations and .  

For detailed instructions regarding installation, see the [README](https://github.com/wesleymeredith/Drowsiness-Detection).  

### Methods  
The program uses dlib to detect facial landmarks, focusing on the regions around the eyes. The Eye Aspect Ratio (EAR) is a scalar value that is calculated by determining ratio of Euclidean distances between specific eye landmarks. If the EAR drops below a predefined threshold for more than one second, the system detects drowsiness and issues an alert.  

When drowsiness is detected, the system:  
- Displays a warning on the video feed.  
- Plays an audio alert using pyttsx3.  

### Code Overview  
The main components of the implementation include:  
- **Camera Setup**: Captures live video feed from the webcam.  
- **Facial Detection**: Detects facial landmarks using dlib.  
- **Eye Tracking**: Continuously calculates the EAR for both eyes.  
- **Drowsiness Detection**: Triggers alerts if the EAR remains below 0.3 for over one second.  

Here’s a simplified code snippet:  
```python  
# Detect EAR for left and right eyes  
left_EAR = Detect_Eye(leftEye)  
right_EAR = Detect_Eye(rightEye)  
avg_EAR = (left_EAR + right_EAR) / 2  

# Check for drowsiness  
if avg_EAR < EAR_THRESHOLD:  
    if time.time() - closed_eyes_start_time > DROWSINESS_THRESHOLD:  
        # Trigger alert  
        engine.say("Wake up!")  
        engine.runAndWait()  
```
And it looks something like this:
<img src='/images/eye_open.png'>
<img src='/images/eye_close.png'>