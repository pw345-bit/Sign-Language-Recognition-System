**Sign-Language-Recognition-System**

1. About the Project
The Sign Language Recognition System is a Python-based application that recognizes hand gestures using a webcam and converts them into text and voice.
For example, if you record a gesture and name it “Hello,” the system can recognize that gesture later and speak the word “Hello” aloud.
The project uses MediaPipe to detect hand movements and Dynamic Time Warping (DTW) to compare gestures.
2. Main Features
- Real-Time Recognition: Recognizes recorded gestures using a webcam.
- Voice Output: Speaks the recognized word aloud.
- Record Custom Signs: Allows users to record and save their own gestures.
- Two Modes: Switch between recording new signs and recognizing existing signs.
- Accuracy Control: Uses a DTW threshold to decide whether a gesture matches a saved sign.
- CPU-Based: Runs on a normal laptop without requiring a GPU.
3. Technologies Used
Technology	Simple Explanation
Python	Main programming language
OpenCV	Opens the webcam and displays video
MediaPipe	Detects hand and body landmarks
DTW	Compares a new gesture with saved gestures
NumPy	Performs mathematical calculations
pyttsx3	Converts recognized text into speech
4. How Does It Work?
Step 1: Capture Video
The webcam captures the user's hand movements.
Step 2: Detect Hand Landmarks
MediaPipe identifies important points on the hand, such as fingertips and join
Step 3: Compare Gestures
DTW compares the captured gesture with the gestures saved earlier
Step 4: Display and Speak
The application displays the recognized word and speaks it aloud.
5. How to Run the Project
First, install Python and the required libraries.
Open the terminal in your project folder and run:
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements_updated.txt
python main.py


These commands create a virtual environment, install the required libraries, and start the application on Windows.
6. Keyboard Controls
Key	Function
m	Switch between recording and recognition modes
n	Enter the name of a new sign
r	Start or stop recording/recognition
q	Close the application
7. How to Record and Recognize a Sign
To record a new sign:
1. Press m to enter recording mode.
2. Press n and enter a name, such as Hello.
3. Press r and perform the hand gesture for around two seconds.
4. Press r again to save the gesture.
To recognize a sign:
1. Switch to recognition mode using m.
2. Press r to start recognition.
3. Perform the gesture you previously recorded.
4. Press r again to stop.
5. The system displays the matching word and speaks it aloud.
8. Project Folder Structure
sign_language/
├── main.py
├── sign_recorder.py
├── webcam_manager.py
├── utils/
│   ├── voice_output.py
│   ├── sign_storage.py
│   ├── landmark_utils.py
│   └── dtw.py
├── models/
│   ├── hand_model.py
│   ├── pose_model.py
│   └── sign_model.py
└── data/
    └── signs/


- main.py — Starts the application.
- sign_recorder.py — Handles recording and recognition.
- webcam_manager.py — Manages webcam video and the display.
- voice_output.py — Speaks the recognized word.
- sign_storage.py — Saves and loads recorded gestures.
- landmark_utils.py — Processes hand landmarks.
- dtw.py — Compares gesture sequences.
- models/ — Contains code for processing hand, pose, and sign data.
- data/signs/ — Stores recorded signs.
9. System Requirements
- Python 3.8 or higher, subject to library compatibility.
- Windows, macOS, or Linux.
- A working webcam.
- At least 4 GB RAM; 8 GB is recommended.
- A standard CPU. No GPU is required.
10. Advantages
- Easy to use.
- Works in real time.
- Supports custom gestures.
- Provides both text and voice output.
- Works offline for speech synthesis.
- Does not require expensive hardware.
11. Limitations
- Users must record gestures before the system can recognize them.
- Recognition can be affected by lighting, camera quality, and how consistently a gesture is performed.
- The DTW threshold may need adjustment.
- It does not automatically recognize every sign in a complete sign language.
- Recognizing individual gestures is not the same as translating full sign-language sentences, which can require facial expressions, grammar, and context.
12. Future Improvements
- Add recognition for alphabet signs from A to Z.
- Include a ready-made library of common signs.
- Improve recognition using machine-learning classifiers.
- Convert spoken words into sign-language animations.
- Support more signs and potentially multiple sign languages.
13. Project Summary
The Sign Language Recognition System uses a webcam to capture hand gestures, MediaPipe to identify hand landmarks, and DTW to compare those movements with previously recorded gestures. When a match is found, the system displays the corresponding word and speaks it using offline text-to-speech.
In simple words: You teach the system a hand gesture once, and it can try to recognize that gesture again whenever you perform it in front of the webcam.
