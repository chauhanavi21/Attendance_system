# Attendance System

A versatile attendance management system for recording and tracking attendance via facial recognition or manual entry. Built with Python, OpenCV, and Tkinter.

---

## 🔧 Features

- **Face-Based Attendance**: Automatically captures attendance using webcam and face recognition.
- **Manual Entry**: Option to input attendance manually.
- **Training Module**: Train your dataset by adding new student faces.
- **Subject-Based Logging**: Create separate attendance logs (CSV) for each subject.
- **Interactive GUI**: Simple and intuitive Tkinter-based interface.
- **Attendance Viewer**: Easily view recorded entries in a tabular format.

---

## 🛠️ Installation

1. Clone the repo:
git clone https://github.com/chauhanavi21/Attendance_system.git
cd Attendance_system

2. Install dependencies:
pip install -r requirements.txt
3. (Optional) Ensure `project_requirement.txt` is synchronized with `requirements.txt`.
4. Create a directory named `TrainingImage/` in the project root to store captured face images.

---

## 🚀 Usage

1. **Capture Images**  
- Run `takeImage.py`
- Enter Student ID & Name, then click **“Take Image”**
- Webcam will capture ~50 face samples into `TrainingImage/NAME.ID`

2. **Train Model**  
- Run `trainImage.py`  
- Converts face data into a trained recognizer model file.

3. **Record Attendance Automatically**  
- Run `automaticAttendance.py`
- Enter subject name, click **“Start Attendance”**
- System detects faces and logs attendance in `Attendance_<SUBJECT>.csv`

4. **Manual Attendance**  
- Run `takemanually.py`  
- Input student details manually, log attendance accordingly.

5. **View Records**  
- Run `show_attendance.py`
- Displays attendance entries for all subjects.

---

## 📁 File Overview

| File / Folder             | Description                                              |
|--------------------------|----------------------------------------------------------|
| `takeImage.py`           | Captures student face images via webcam                 |
| `trainImage.py`          | Processes images and builds a face recognition model    |
| `automaticAttendance.py` | Logs attendance automatically using real-time detection  |
| `takemanually.py`        | Manual attendance entry utility                         |
| `show_attendance.py`     | GUI to view existing attendance logs                    |
| `haar…xml` files         | Pre-trained Haar cascades for face detection            |
| `TrainingImage/`         | Stores captured face images                             |
| `Attendance_*.csv` files | Attendance logs for each subject                       |
| `requirements.txt`       | Python dependencies                                     |

---

## 🚦 Notes & Tips

- Use a consistent naming format: `Name.ID` for image folders.
- Ensure good lighting & clear face position while capturing images.
- Retrain the model whenever you add new students.
- CSV logs include: ID, Name, Date, Time, Subject.
- Customize # of captured images and CSV columns in code if needed.

---

## 🙌 Contributions

Feel free to fork, improve, and submit pull-requests! ⭐ If you find bugs or have ideas, open an issue.

---

## 📝 License

Distributed under MIT License. See `LICENSE` for details.

