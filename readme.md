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

```bash
# 1️⃣ Clone the Repository
git clone https://github.com/SaranshGupta02/Automated-Parking-System.git
cd Automated-Parking-System

# 2️⃣ Install Dependencies
pip install flask ultralytics opencv-python pytesseract requests

# 3️⃣ Set Up Tesseract
# Download and install Tesseract OCR from https://github.com/UB-Mannheim/tesseract/wiki
# Then update the path in `app.py`
# Example: 
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'

# 4️⃣ Run the Application
python app.py
API Endpoints
Endpoint	Method	Description
/	GET	Renders the homepage
/process_images	GET	Detects vehicles, extracts license plates, and retrieves parking slot info
How It Works
The system loads and processes images using YOLO.
If a vehicle is detected, the license plate is extracted via OCR.
The detection data is sent to ThingSpeak.
The system retrieves the available parking slot from ThingSpeak.
The result is displayed in the Flask web interface.
Workflow
Load 5 images (in .jpg, .jpeg, or .png format).
YOLO model detects vehicles (Car, Van, Truck, Bus, Motorcycle, Bicycle).
If a vehicle is detected:
YOLO model detects the license plate.
OpenCV extracts the bounding box.
Tesseract OCR reads the plate number.
Send vehicle detection data to ThingSpeak.
Wait 10 seconds for parking slot data update.
Retrieve slot information from ThingSpeak.
Display detected vehicle, license plate, and slot information in the web interface.
Project Structure
bash
Copy
Edit
📂 Automated-Parking-System
 ┣ 📂 templates
 ┃ ┗ 📜 index.html
 ┣ 📜 app.py
 ┣ 📜 best_5.pt  # YOLO model for vehicle detection
 ┣ 📜 License.pt # YOLO model for license plate detection
 ┣ 📜 requirements.txt  # Dependency list
 ┗ 📜 README.md
Future Improvements
✅ Integrate real-time video processing for live camera feeds.
✅ Implement a database for vehicle entry logs.
✅ Add user authentication for managing parking slots.
