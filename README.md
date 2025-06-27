# Control-LED-s-with-Hand-Gestures
Control LED’s With Waves : No Buttons, Just Magical Hand Gestures
# Hand Gesture Controlled LED Display

This project uses **computer vision** to detect hand gestures and control an **Arduino-connected LED strip** to visually represent the number of fingers shown in front of a webcam.

## 🔧 Components Used

- Python 3.x
- OpenCV
- MediaPipe
- pyfirmata2
- Arduino (with Firmata firmware)
- 5 LEDs
- Resistors & jumper wires
- Webcam

## 📁 Project Structure

```
code_execution/
│
├── Controller.py        # Controls the LEDs via Arduino using pyfirmata2
├── openCV.py            # Uses webcam & MediaPipe to detect hand gestures
├── [Reeteka][1].odt     # Project report or documentation
└── __pycache__/         # Python bytecode cache (can be ignored)
```

## 🚀 How It Works

1. **openCV.py** uses OpenCV and MediaPipe to track a user's hand.
2. It identifies the number of fingers held up.
3. The number of raised fingers is passed to the `led()` function in `Controller.py`.
4. LEDs connected to the Arduino board light up accordingly (e.g., 3 fingers → 3 LEDs).

## 📌 Setup Instructions

1. **Install Required Libraries:**

```bash
pip install opencv-python mediapipe pyfirmata2
```

2. **Connect Arduino:**
   - Upload the Standard Firmata firmware to your Arduino using the Arduino IDE.
   - Connect 5 LEDs to digital pins 2, 4, 6, 8, and 10.

3. **Update COM Port:**
   - In `Controller.py`, update the line:
     ```python
     comport='COM7'  # Change this to match your system's port
     ```

4. **Run the Project:**

```bash
python openCV.py
```

5. Show your hand in front of the webcam. The number of LEDs will light up based on how many fingers you're holding up.

## 📷 Demo

*Add a GIF or link to a demo video here if available.*

## 🧠 Author

Reeteka – AIML Major Project

## ⚠️ Notes

- Ensure your environment has camera access.
- Run the script in a well-lit environment for better hand detection.
- Works best with a single hand visible.

---

Enjoy your gesture-controlled LED magic! ✋✨💡
