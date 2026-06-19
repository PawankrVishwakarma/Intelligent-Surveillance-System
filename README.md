# Intelligent Surveillance & Alert System

A real-time AI-powered surveillance system built using YOLOv8, OpenCV, and Python for person detection, restricted-area intrusion monitoring, automated alerts, and incident recording.

## Features

- Real-time person detection using YOLOv8
- Restricted Area (ROI) Intrusion Monitoring
- Automated Email Alerts with Image Evidence
- Automatic Screenshot Capture
- Automatic Video Recording of Intrusion Events
- Timestamp Logging (IST)
- FPS Monitoring
- Apple Silicon (MPS) / CUDA Acceleration Support
- Secure Environment Variables using `.env`

---

## Project Structure

```
Intelligent-Surveillance-System/
│
├── alarm_system.py
├── requirements.txt
├── README.md
├── .gitignore
├── .env
│
├── models/
│   └── yolov8n.pt
│
├── captures/
│   └── person_detected_*.jpg
│
├── videos/
│   └── intrusion_*.mp4
│
└── screenshots/
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/Intelligent-Surveillance-System.git

cd Intelligent-Surveillance-System
```

### Create Virtual Environment

```bash
python -m venv cv_env
```

Activate:

**Windows**

```bash
cv_env\Scripts\activate
```

**macOS/Linux**

```bash
source cv_env/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Download YOLO Model

Download YOLOv8n model:

```bash
yolov8n.pt
```

Create:

```text
models/
```

Place model:

```text
models/yolov8n.pt
```

---

## Environment Variables

Create a `.env` file:

```env
FROM_EMAIL=your_email@gmail.com
EMAIL_PASSWORD=your_app_password
TO_EMAIL=receiver_email@gmail.com
```

---

## Run Project

```bash
python alarm_system.py
```

---

## Workflow

1. Camera starts monitoring.
2. YOLOv8 detects persons in real-time.
3. If a person enters the restricted area:
   - Screenshot is captured.
   - Email alert is sent.
   - Image evidence is attached.
   - Video recording starts automatically.
4. Intrusion video is stored locally.
5. Timestamp and detection details are logged.

---

## Technologies Used

- Python
- OpenCV
- YOLOv8 (Ultralytics)
- Supervision
- PyTorch
- SMTP Email Service
- Python Dotenv

---

## Future Improvements

- Multi-camera support
- Telegram/WhatsApp alerts
- Object Tracking (ByteTrack/DeepSORT)
- Cloud Storage Integration
- Web Dashboard
- Heatmap Analytics

---

## Notes

The following files and folders are excluded from version control using `.gitignore`:

- `.env` (email credentials)
- `models/*.pt` (YOLO model weights)
- `captures/` (captured images)
- `videos/` (recorded videos)
- `__pycache__/`
- `*.pyc`

---

## Author

**Pawan Kumar Vishwakarma**

Computer Vision | AI | Deep Learning | YOLOv8 | OpenCV