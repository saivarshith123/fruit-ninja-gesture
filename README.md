# 🥷🍉 Fruit Ninja - Gesture Control Edition

A fun, interactive **Fruit Ninja-style slicing game** that uses your **hand gestures** to slice falling fruits in real-time, powered by **Python, OpenCV**, and **MediaPipe**!

## 🎮 How It Works

This project uses your webcam to track your hand in real time. When you move your index finger fast enough (a "swipe"), and it intersects with a falling fruit, the fruit gets sliced — just like in the classic Fruit Ninja game!

- 👆 Hand tracking: via [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html)
- 🎥 Webcam input: via `cv2.VideoCapture()`
- 🍎 Falling fruits: created as objects and animated using velocity
- ✂️ Swipe detection: based on distance moved by index fingertip across frames

## 🛠️ Technologies Used

- **Python 3.7+**
- [OpenCV](https://opencv.org/) (`cv2`)
- [MediaPipe](https://mediapipe.dev/)

## 📦 Installation

### 1. Clone this repository

```bash
git clone https://github.com/saivarshith123/fruit-ninja-gesture.git
cd fruit-ninja-gesture
```

### 2. Set up your Python environment

```bash
python -m venv venv
venv\Scripts\activate   # On Windows
# Or use `source venv/bin/activate` on macOS/Linux
```
### 3. Install dependencies

```bash
pip install opencv-python mediapipe
```
## Running the Game

Make sure your webcam is connected and working.

```bash
python one.py
```
Press Q to quit the game window.

## 🎯 Game Controls

- 🖐️ Use your hand in front of your webcam.

- 🟣 Your index fingertip is tracked with a purple dot.

- ✂️ Swipe fast across a fruit to slice it!

- ❌ Missed fruits will fall off the screen and disappear.

## 📁 File Structure

```bash
fruit-ninja-gesture/
│
├── one.py               # Main game script
├── README.md            # Project documentation
```

## 🧠 Key Features Explained

| Feature           | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| Real-time tracking | Uses MediaPipe to track one hand and extract index finger coordinates.      |
| Swipe detection   | Calculates distance moved by finger tip across frames to detect a "swipe". |
| Fruit class       | Custom class to animate falling fruits and handle collision detection.      |
| Slicing effect    | When swiped, fruit disappears and displays "SLICED!" on screen.             |
| Simple UI         | Rendered using OpenCV’s `cv2.circle()` and `cv2.putText()`.                 |

## 📌 Future Improvements

- Add multiple fruits and more complex slicing patterns

- Add sound effects and score tracking

- Add game levels or difficulty modes

## 🤝 Contributing

Pull requests are welcome! If you'd like to improve the game or fix bugs, feel free to fork and submit a PR.

