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

```
trash-detection/
├── app.py              # Main application (Streamlit or Flask)
├── helper.py           # Detection logic and utility functions
├── model/
│   └── best.pt         # YOLO-trained weights
├── static/             # (Optional) CSS/JS if using Flask
├── requirements.txt    # Dependencies list
├── Dockerfile          # Docker build configuration
├── README.md           # Project documentation
└── LICENSE             # License file
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Felix-ryn/trash-detection.git
cd trash-detection
```

### 2. Setup Environment

```bash
python3 -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Add YOLO Model Weights

Place your YOLO `.pt` model file inside the `model/` directory (e.g., `model/best.pt`).

---

### ▶️ Running the Application

#### Option A: Using Streamlit

```bash
streamlit run app.py
```

Access the app at: [http://localhost:8501](http://localhost:8501)

#### Option B: Using Flask (if implemented)

```bash
python app.py
```

Access via: [http://localhost:5000](http://localhost:5000)

---

## 💡 How It Works

1. User uploads an image.  
2. `helper.py` loads the YOLO model and runs inference.  
3. Detections (labels and bounding boxes) are applied to the image.  
4. Annotated image is returned and displayed in the browser.

---

## ⚙️ Configuration

- **Model**: Update `model/best.pt` with your custom-trained weights.  
- **Confidence Threshold**: Change it in `helper.py` (e.g., `CONFIDENCE_THRESHOLD = 0.4`)  
- **Class Mapping**: Modify label map inside helper file if your classes differ.  
- **UI**: Customize using Streamlit config or Flask templates.

---

## 🐳 Docker Deployment (Optional)

```bash
docker build -t trash-detector .
docker run -p 8501:8501 trash-detector
```

---

## 🧪 Testing

Run tests using:

```bash
pytest
```

---

## 🔭 Future Enhancements

- 🎥 Live webcam or video stream support  
- 🌐 REST API for mobile or remote submission  
- 📊 Detection logs and dashboard analytics  
- 📁 Batch processing for multiple images  
- 💡 Integration with alert or scheduling systems  

---

## 🤝 Contribution Guide

We welcome contributions!

1. Fork the repository  
2. Create a new branch (e.g., `feat/your-feature`)  
3. Commit your changes with clear messages  
4. Submit a pull request  
5. Wait for review and merge

Please open an issue first for major proposals.

---

## 📜 License

MIT License  
Copyright (c) 2025 Felix Ryan

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is  
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in  
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER  
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,  
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN  
THE SOFTWARE.

---

## 👨‍💻 Author

**Felix Ryan Agusta**  
GitHub: [@Felix-ryn](https://github.com/Felix-ryn)

> “Transforming waste into insight — one image at a time.” 🌿
