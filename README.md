# YOLO-Based PPE Detection System

A real-time **Personal Protective Equipment (PPE) Detection System** powered by the YOLOv8 model. This project is designed to ensure workplace safety by identifying compliance (e.g., hardhat, mask, safety vest) and non-compliance (e.g., missing hardhat, missing mask) in videos or live camera feeds.

---

## 🚀 Features
- Real-time detection of **PPE compliance** (hardhats, masks, safety vests, etc.).
- Identifies **non-compliance** (e.g., missing hardhat, mask, or safety vest).
- Displays bounding boxes and confidence scores for detected objects.
- Supports both **live webcam feeds** and **video files**.

---
## 📂 Project Structure
├── videos/                
│   ├── ppe-1-1.mp4          
├── best.pt               
├── main.py             
└── README.md 
           


---

## 🛠️ Installation

### Prerequisites
1. Python 3.8 or above
2. Required libraries:
   - `ultralytics` (for YOLOv8)
   - `opencv-python`
   - `cvzone`
   - `numpy`
   - `math`

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/mridulchdry17/YOLO-Based-PPE-Detection-System.git
   cd YOLO-Based-PPE-Detection-System
   ```
2 . Install dependencies:
```bash
pip install -r requirements.txt
```
3. Download YOLOv8 model weights:
   * Place the trained YOLOv8 model (best.pt) in the project_3 folder.

4. Run the project:
  * For a video file:
```bash
python main.py
```
  * For webcam detection (uncomment webcam code in main.py):
```bash
python main.py
```
### ⚙️ How It Works
 1. The system uses the YOLOv8 model trained on a dataset of PPE-related images.
 2. Input frames (from webcam or video) are passed through the model.
 3. Objects like hardhats, masks, safety vests, and non-compliant items are identified.
 4. Bounding boxes are drawn with the following color scheme:
* 🟢 Green: Compliant items (e.g., Hardhat, Mask, Safety Vest)
* 🔴 Red: Non-compliant items (e.g., Missing Hardhat, Missing Mask)
* 🔵 Blue: Other detected objects (e.g., vehicles, people)

### 📖 Dataset
The model is trained on a custom PPE dataset, including classes like:

- Hardhat
- Safety Vest
- Mask
- Missing Hardhat
- Missing Mask
- Vehicles (SUV, Truck, etc.)
- Other related objects

### 🎯 Use Cases
- Workplace Safety Monitoring: Ensure employees are using the required PPE.
- Construction Sites: Identify workers missing safety equipment.
- Industrial Zones: Automate compliance checks.
