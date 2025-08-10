# Touch-Free-Laptop-Brightness-Adjustment-using-OpenCV-and-MediaPipe
Developed an OpenCV &amp; MediaPipe-based system to control laptop brightness via thumb–index finger gestures. Used math.hypot() to calculate finger distance and mapped it to brightness levels, enabling real-time, touch-free screen adjustment.

This project uses OpenCV and MediaPipe to control your laptop's brightness in real time by detecting
the distance between your thumb and index finger. The finger distance is calculated using Python's
math.hypot() function and mapped to brightness levels using NumPy interpolation.


Features:
- Real-time hand tracking using MediaPipe
- Detects thumb and index finger tips
- Calculates distance between fingers using hypot
- Maps finger distance to screen brightness (0–100%)
- Hands-free, intuitive brightness control


How It Works:
1. MediaPipe Hands detects the hand landmarks from webcam input.
2. The positions of the thumb tip (ID 4) and index finger tip (ID 8) are extracted.
3. math.hypot() calculates the Euclidean distance between them.
4. NumPy maps the distance range (15–220 pixels) to brightness levels (0–100).
5. screen_brightness_control adjusts the laptop’s brightness instantly.


Requirements:
pip install opencv-python mediapipe screen-brightness-control numpy

Usage:
1. Clone this repository:
git clone https://github.com/yourusername/gesture-brightness-control.git
cd gesture-brightness-control


2. Run the script:
python brightness_control.py
Controls:
- Bring thumb and index finger closer → brightness decreases
- Move them apart → brightness increases

Notes:
- Works best in good lighting conditions
- Adjust the interpolation range if your camera resolution changes
- Only tested on laptops supporting screen_brightness_control
