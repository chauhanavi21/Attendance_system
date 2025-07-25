
# 🎯 Face Recognition Attendance System

A smart face-recognition based attendance system using OpenCV, KNN, and React. This system automates the attendance process by detecting and recognizing faces using a webcam and logs entries to daily CSV files.

---

## 📸 Features

- 👤 Register users by capturing facial data through webcam
- 🧠 Real-time face recognition using K-Nearest Neighbors (KNN)
- 🗣️ Text-to-speech audio feedback when attendance is marked
- 🧾 Automatically creates daily CSV attendance logs
- 🖥️ Beautiful React-based UI: Registration, Attendance, and Dashboard
- 🔐 Data stored locally in `pkl` and `csv` formats (no cloud needed)

---

## 🏗️ Tech Stack

| Layer     | Technology          |
|-----------|---------------------|
| Frontend  | React + Tailwind CSS |
| Backend   | Flask + OpenCV + scikit-learn |
| Language  | Python & JavaScript |
| Storage   | CSV, Pickle (`.pkl`) |
| Camera    | Live Webcam via OpenCV |

---

## 📁 Folder Structure

```
attendance-system/
├── backend/
│   ├── app.py                # Flask backend server
│   ├── register.py           # Capture face and save to database
│   ├── recognize.py          # Face recognition and attendance logging
│   ├── haarcascade_frontalface_default.xml
│   ├── data/                 # Stores .pkl and .csv files
│   └── venv/                 # Python virtual environment
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   │   ├── Register.jsx
│   │   │   ├── Attendance.jsx
│   │   │   ├── Dashboard.jsx
│   └── index.html, App.jsx, etc.
```

---

## 🧪 Setup Instructions (for Windows Users)

### ✅ Backend Setup (Python + PowerShell)

```powershell
cd attendance-system\backend
python -m venv venv
.\venv\Scripts\activate
pip install flask flask-cors opencv-python numpy scikit-learn pywin32
```

#### 🔽 Download this file
Place the following file inside the `backend/` directory:
- [haarcascade_frontalface_default.xml](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml)

### ▶️ Run Backend Server

```powershell
python app.py
# Runs on http://localhost:5000
```

---

### ✅ Frontend Setup (React + PowerShell)

```powershell
cd attendance-system\frontend
npm install
npm run dev
# Runs on http://localhost:5173
```

---

## 🚦 Pages

| Route               | Purpose                       |
|---------------------|-------------------------------|
| `/`                 | Main menu (portal)            |
| `/register`         | Register a new face           |
| `/attendance`       | Mark attendance (10 sec cam)  |
| `/dashboard`        | View list + download CSV      |

---

## 🧾 Attendance Storage

Each day creates a CSV like:

```
data/Attendance_YYYY-MM-DD.csv

Columns: NAME, TIME

Example:
Avi, 10:42:15
John, 10:44:02
```

---

## ✅ How Recognition Works

- KNN classifier trained on `faces_data.pkl` (flattened face images)
- Face detection via Haar Cascade
- If your face is detected, system:
  - ✅ Shows name on screen
  - 🔊 Speaks "Your attendance is marked"
  - 📝 Appends to that day's CSV (once per session)

---

## 🧠 Future Suggestions

- 🔐 Add login for admin dashboard
- ☁️ Migrate storage to database (MongoDB / SQLite)
- 🤖 Switch to face embeddings (DeepFace / FaceNet) for better accuracy
- 🧾 Export to Excel / Google Sheets
- 📱 Convert to mobile web view or app

---

## 🙌 Acknowledgements

- [OpenCV](https://opencv.org/)
- [Flask](https://flask.palletsprojects.com/)
- [React](https://reactjs.org/)
- [scikit-learn](https://scikit-learn.org/)
