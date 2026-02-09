# 🤖 Face Recognition Automatic Attendance System

![Project Banner](./Face-Recognition-Automatic-Attendance-System.png)

## 📝 Overview
The **Face Recognition Automatic Attendance System** is a Python-based application that leverages computer vision to automate the process of recording attendance. By using real-time video feed from a webcam, the system identifies individuals based on pre-registered images and logs their presence along with a timestamp into a CSV file.

This project is ideal for schools, offices, or any organization looking to modernize their attendance tracking with a touchless and efficient solution.

---

## ✨ Features
- **Real-time Recognition**: Instant face detection and recognition from a live webcam feed.
- **Automated Logging**: Automatically records the name and time of arrival in a `attendance.csv` file.
- **Anti-Duplication**: Prevents multiple entries for the same person on the same day (based on current implementation logic).
- **Easy Maintenance**: Simply add or remove images in the `ImagesAttendance` folder to update the recognized personnel.
- **Visual Feedback**: Displays a bounding box and the name of the recognized person on the video stream.

---

## 🛠️ Technologies Used
- **Python**: Core programming language.
- **OpenCV**: For image processing and video capturing.
- **face_recognition**: A high-level library for face detection and encoding (built on dlib).
- **NumPy**: For numerical computations and array manipulations.
- **CSV**: For lightweight data storage.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.7 or higher.
- A functional webcam.
- [CMake](https://cmake.org/download/) installed (required for the `dlib` dependency of `face_recognition`).

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/Face-recognition-attendance-sysytem-main.git
   cd Face-recognition-attendance-sysytem-main
   ```

2. **Create a virtual environment (optional but recommended)**:
   ```bash
   python -m venv venv
   source venv/bin/scripts/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   # Note: You may also need to install face_recognition manually if not in requirements.txt
   pip install face-recognition opencv-python numpy
   ```

---

## 📖 Usage
1. **Register Faces**:
   Place clear images of the persons you want to recognize into the `ImagesAttendance` directory. Ensure the file names are the names of the individuals (e.g., `elon_musk.jpg`).

2. **Run the System**:
   Execute the main script:
   ```bash
   python attendance_system.py
   ```

3. **Check Attendance**:
   Open `attendance.csv` to view the recorded attendance data.

---

## 📂 Project Structure
```text
├── ImagesAttendance/      # Directory for registered face images
├── ImagesTest/            # Directory for testing images
├── attendance_system.py   # Main entry point for the application
├── attendance.csv         # Recorded attendance data
├── requirements.txt       # Project dependencies
├── Dockerfile             # Containerization configuration
└── README.md              # Project documentation
```

---

## 📸 Demo
The system captures the webcam feed, resizes each frame for faster processing, and compares detected faces against the encodings of registered images. Once a match is found, it draws a green rectangle around the face and displays the name.

---

## 🤝 Contributing
Contributions are welcome! If you'd like to improve the system, add features, or fix bugs:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/NewFeature`).
3. Commit your changes (`git commit -m 'Add some NewFeature'`).
4. Push to the branch (`git push origin feature/NewFeature`).
5. Open a Pull Request.

---

## ⚖️ License
This project is open-source and available under the MIT License.

---

## 👨‍💻 Developed By
**Muhammad Danish** 

*Feel free to reach out for questions or collaborations!*
