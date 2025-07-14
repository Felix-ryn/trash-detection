# 🚮 Trash Detection

A high-performance computer vision web application built in Python to detect and classify trash in images using YOLO. This project is designed for environmental monitoring, smart clean-up systems, and educational purposes.

---

## 🔍 Project Overview

This application leverages a YOLO-based object detection model to identify different types of waste—plastic, metal, paper, cans, etc.—in images uploaded by users. The detection results are rendered as annotated bounding boxes and category labels through a clean and interactive web interface.

---

## 🛠️ Features

- 🔍 Trash detection using YOLOv10 or YOLOv8  
- 🖼️ Upload images directly through web UI  
- 📦 Output includes bounding boxes, labels, and confidence scores  
- ⚙️ Modular logic for easy customization and extension  
- 🌐 Ready for local or Docker-based deployment  

---

## 🧰 Tech Stack

| Component      | Technology            |
|----------------|------------------------|
| Language       | Python 3              |
| Web Framework  | Streamlit / Flask     |
| Model          | YOLOv10 (Ultralytics) |
| Libraries      | OpenCV, Torch, Pillow |
| Deployment     | Docker (optional)     |
| Testing        | Pytest                |

---

## 📂 Project Structure
trash-detection/
├── app.py # Main application (Streamlit or Flask)
├── helper.py # Detection logic and utility functions
├── model/
│ └── best.pt # YOLO-trained weights
├── static/ # (Optional) CSS/JS if using Flask
├── requirements.txt # Dependencies list
├── Dockerfile # Docker build configuration
├── README.md # Project documentation
└── LICENSE # License file


---

## 🚀 Getting Started

### 1. Clone the Repository
git clone https://github.com/Felix-ryn/trash-detection.git
cd trash-detection```

### 2. Setup Environment
python3 -m venv venv
source venv/bin/activate   
pip install -r requirements.txt

### 3. Add YOLO Model Weights
Place your YOLO .pt model file inside the model/ directory (e.g., model/best.pt).

▶️ Running the Application
Option A: Using Streamlit
streamlit run app.py
Access at: http://localhost:8501

Option B: Using Flask (if implemented)
python app.py
Access at: http://localhost:5000


💡 How It Works
User uploads an image.

helper.py loads the YOLO model and runs inference.

Detections (labels and bounding boxes) are applied to the image.

Annotated image is returned and displayed in the browser.

⚙️ Configuration
Model: Change or update model/best.pt with your custom-trained weights.

Confidence Threshold: Adjust in helper.py (e.g., CONFIDENCE_THRESHOLD = 0.4)

Class Mapping: Modify label map inside helper file if your classes differ.

UI Themes: Use Streamlit configuration or Flask templating for design customization.

🐳 Docker Deployment (Optional)
docker build -t trash-detector .
docker run -p 8501:8501 trash-detector

🧪 Testing
pytest

🔭 Future Enhancements
🎥 Live webcam or video stream support

🌐 REST API for mobile or remote submission

📊 Detection logs and dashboard analytics

📁 Batch processing for multiple images

💡 Integration with alert or scheduling systems

🤝 Contribution Guide
We welcome contributions!
Fork the repository
Create a new branch (feat/your-feature)
Commit your changes with clear messages
Submit a pull request
Wait for review and merge
