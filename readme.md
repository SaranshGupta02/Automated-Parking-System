# **Automated Parking System**

## **Overview**
The **Automated Parking System** is a Flask-based application that utilizes **YOLO** for vehicle and license plate detection, **Tesseract OCR** for license plate recognition, and **ThingSpeak API** for real-time parking slot management.

## **Features**
- 🚗 **Vehicle Detection**: Detects cars, bikes, and other vehicles using a trained YOLO model.
- 🏷️ **License Plate Recognition**: Extracts license plate numbers using OCR.
- 📡 **Real-time Data Communication**: Sends vehicle detection data to **ThingSpeak API**.
- 🚦 **Parking Slot Monitoring**: Retrieves available slots from **ThingSpeak**.
- 🌐 **Web Interface**: Displays processed data using a Flask web app.

## **Tech Stack**
- **Backend**: Flask
- **Computer Vision**: YOLO (Ultralytics), OpenCV
- **OCR**: Tesseract
- **Cloud Integration**: ThingSpeak API
- **Frontend**: HTML, JavaScript (via Flask templates)

## **Installation**

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/SaranshGupta02/Automated-Parking-System.git
cd Automated-Parking-System
