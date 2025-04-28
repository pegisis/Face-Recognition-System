

# Face Recognition Attendance System

A simple Python-based face recognition system that captures face data, trains a KNN model, and records attendance automatically using a webcam.

---

## Features

- Real-time face detection using OpenCV.
- Face data collection and training using K-Nearest Neighbors (KNN).
- Automatic attendance marking in a CSV file.
- Supports adding multiple users.
- Saves all data locally for privacy.

---

## Requirements

- Python 3.x
- OpenCV (`cv2`)
- scikit-learn (`sklearn`)
- numpy
- pickle

You can install the required packages using:

```bash
pip install opencv-python scikit-learn numpy
```

---

## Project Structure

```
├── data/
│   ├── haarcascade_frontalface_default.xml
│   ├── names.pkl
│   └── faces_data.pkl
├── Attendance/
│   └── (generated attendance CSVs)
├── faces.py       # For capturing face data
├── test.py        # For real-time face recognition and attendance
├── .gitignore     # (optional, not necessary for basic runs)
└── README.md
```

---

## How to Use

### 1. Capture Face Data

Run the following command:

```bash
python faces.py
```

- Enter your name when prompted.
- The webcam will open. Look into it.
- It will collect 100 images of your face (one every few frames).
- Press `q` anytime to quit early.

> All face data and names are saved in the `data/` folder.

---

### 2. Start Attendance System

Run the following command:

```bash
python test.py
```

- The webcam will open and start recognizing faces.
- If recognized, it displays the name in **green**; otherwise, shows **Unknown** in **red**.
- Press `m` to **mark your attendance** manually.
- Press `q` to **quit** the session.

> Attendance is saved in the `Attendance/` folder as a CSV file named `Attendance_dd-mm-yy.csv`.

---

## Important Notes

- Ensure the `data/haarcascade_frontalface_default.xml` file is present. If not, download it from the [OpenCV GitHub repository](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml).
- Face recognition is basic and uses simple distance thresholds. You can improve accuracy by adjusting the `distance` threshold (`5300`) or upgrading the model.
- Data is cumulative — new users are added to the existing dataset.

---

## Controls

| Key | Action                    |
|:---:|:---------------------------|
| `q` | Quit video feed             |
| `m` | Mark attendance (during test.py run) |

---

## License

This project is for **educational purposes**. Feel free to modify and extend it.

---

Would you also like me to create a **requirements.txt** file for you? 🚀  
It would make installing dependencies even easier.
