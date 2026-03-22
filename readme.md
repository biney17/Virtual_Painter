# 🎨 Virtual Painter

> Draw in the air using only your hand and a webcam — no mouse, no touch screen needed.

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?style=flat-square&logo=opencv)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Hand_Tracking-orange?style=flat-square)
---


## ✨ Features

- ✋ Real-time hand tracking via webcam
- 🖌️ Draw freely in the air with your index finger
- 🎨 Color selection: Pink, Blue, Green
- 🧹 Eraser mode with black color
- 🖼️ Custom header UI overlay with tool selector
- 📐 Canvas layer blended over live camera feed

---

## 🗂️ Project Structure

```
VirtualPainter/
│
├── VirtualPainter.py       # Main application
├── HandTrackingModule.py   # Hand detection & landmark module
├── Header/                 # UI overlay images (4 headers)
│   ├── 1.png
│   ├── 2.png
│   ├── 3.png
│   └── 4.png
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

**1. Clone the repository**
```bash
git clone https://github.com/biney17/Virtual_Painter.git
cd VirtualPainter
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the app**
```bash
python VirtualPainter.py
```

---

## 📦 Requirements

```
opencv-python
mediapipe
numpy
```

> Generate `requirements.txt` with:
> ```bash
> pip freeze > requirements.txt
> ```

---

## 🖐️ How to Use

| Gesture | Action |
|--------|--------|
| ☝️ Index finger up | **Draw** on the canvas |
| ✌️ Index + Middle finger up | **Selection mode** — choose color from header |
| ✌️ Point to black zone | **Erase** |

### Color Zones (top header bar)
| Zone (x position) | Color |
|-------------------|-------|
| 250 – 450 | 🩷 Pink |
| 550 – 750 | 🔵 Blue |
| 800 – 950 | 🟢 Green |
| 1050 – 1200 | ⚫ Eraser |

---

## 🛠️ Configuration

In `VirtualPainter.py`, you can adjust:

```python
brushthickness = 15    # Brush size
erasethickness = 100   # Eraser size
```

---

## 🧠 How It Works

1. **Webcam capture** — frames are read and flipped horizontally
2. **Hand detection** — `HandTrackingModule` uses MediaPipe to detect 21 hand landmarks
3. **Finger state** — checks which fingers are raised
4. **Draw/Select logic** — index finger draws; two fingers switch to selection mode
5. **Canvas overlay** — drawing layer is blended onto the live camera feed using bitwise operations

---

## 📚 Built With

- [OpenCV](https://opencv.org/) — computer vision & rendering
- [MediaPipe](https://mediapipe.dev/) — hand landmark detection
- [NumPy](https://numpy.org/) — canvas array operations

---

## 👤 Author

** Brahimi Isra Nour El Yakine**
- GitHub: [(https://github.com/biney17)]

---
