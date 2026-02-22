# AI-Based Laboratory Safety Compliance Inspector 🦺🔬

An automated computer vision system designed to monitor and enforce Personal Protective Equipment (PPE) compliance in laboratory environments. 

## Overview
This project uses a custom-trained YOLOv8 object detection model to monitor a live camera feed. It detects whether individuals entering a lab are wearing the required safety gear (helmets, masks, and gloves). It features automated audio warnings, email alerts to administrators for repeated violations, and a web-based dashboard for access management.

## Features
* **Real-Time Detection:** Utilizes YOLOv8 for high-speed, accurate PPE detection via webcam.
* **Automated Alerts:** Text-to-speech warnings and buzzer sounds for missing equipment.
* **Email Notifications:** Automatically emails administrators if a student exceeds the maximum number of warnings.
* **Admin Dashboard:** A Streamlit-based web application to view logs, grant/deny access, and generate PDF reports.
* **Access Logging:** Records all entry attempts, timestamps, and PPE status into a CSV database.

## Technologies Used
* **Python** * **Computer Vision:** OpenCV, Ultralytics (YOLOv8)
* **Web Dashboard:** Streamlit, Pandas, Matplotlib
* **Utilities:** pyttsx3 (Audio), smtplib (Email), FPDF (Report Generation)

## How to Run Locally
The project requires two scripts to be running simultaneously.

1. **Start the AI Camera Feed:**
   ```bash
   python lab_ppe_ai.py

2. Start the Admin Dashboard:
  python -m streamlit run admin_dashboard.py


  Model Weights
This repository includes a custom PyTorch model (yolov8s_custom.pt) trained specifically to detect laboratory helmets, safety masks, and gloves.


### Step 3: Check Your Folder
Your `C:\Projects\AI-Laboratory-Inspector` folder should now contain exactly 5 files:
1. `admin_dashboard.py`
2. `lab_ppe_ai.py`
3. `lab_ppe_log.csv`
4. `yolov8s_custom.pt`
5. `README.md`