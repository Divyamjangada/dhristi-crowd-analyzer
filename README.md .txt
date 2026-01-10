# 🚨 Dhristi - AI Crowd Management System

AI-powered crowd safety monitoring system designed to prevent stampedes at large gatherings like Mahakumbh, concerts, and rallies.

## 🎯 Overview

Dhristi uses computer vision and AI to monitor crowd density in real-time, detect dangerous situations, and alert security personnel before incidents occur.

## ✨ Features

- 📊 **Real-time Crowd Counting**: Accurate people detection using OpenCV
- 🔥 **Density Heatmaps**: Visual representation of crowd distribution
- ⚠️ **Anomaly Detection**: Identifies panic movements and potential stampedes
- 🚨 **Smart Alert System**: Multi-level warnings (Safe/Moderate/High/Critical)
- 📹 **Video Analysis**: Process entire event recordings
- 📈 **Analytics Dashboard**: Interactive charts and comprehensive reports
- 🗺️ **Safety Zones**: Area-wise crowd monitoring

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| Python 3.8+ | Core programming language |
| OpenCV | Computer vision and image processing |
| Gradio | Web interface and dashboard |
| Plotly | Interactive visualizations |
| NumPy | Numerical computations |
| Pandas | Data handling and analysis |

## 🚀 Quick Start

### Installation
```bash
# Install required packages
pip install gradio opencv-python-headless numpy pandas plotly pillow

# Run the application
python dhristi_app.py
```

### Access Dashboard

Open browser and go to: `http://localhost:7860`

## 📖 How to Use

### Image Analysis
1. Click **"Image Analysis"** tab
2. Upload a crowd image
3. Enter location name (e.g., "Main Gate - Mahakumbh")
4. Click **"Analyze"**
5. View annotated image, heatmap, safety zones, and recommendations

### Video Analysis
1. Click **"Video Analysis"** tab
2. Upload crowd video (MP4/AVI/MOV)
3. Enter location name
4. Click **"Analyze Video"**
5. Wait for processing (progress bar shown)
6. View processed video, timeline charts, and comprehensive report

## 🎯 Crowd Safety Thresholds

| Alert Level | People Count | Action Required |
|-------------|--------------|-----------------|
| 🟢 **SAFE** | < 150 people | Normal operations, routine monitoring |
| 🟡 **MODERATE** | 150-250 people | Enhanced monitoring, track trends |
| 🟠 **HIGH** | 250-350 people | Deploy additional security, slow entry |
| 🔴 **CRITICAL** | > 350 people | **EMERGENCY**: Stop entry, open exits |

*Note: Thresholds can be customized based on venue capacity*

## 📊 Key Features Explained

### 1. Crowd Counting
Uses contour detection to identify and count people in the frame. Applies calibration factor for accuracy.

### 2. Anomaly Detection
Monitors motion patterns across frames. Sudden increases in movement intensity indicate panic or stampede situations.

### 3. Heatmap Visualization
Color-coded density map:
- **Red** = High density (danger)
- **Yellow/Orange** = Moderate density
- **Green/Blue** = Low density (safe)

### 4. Smart Alerts
- Automatic alert generation when thresholds exceeded
- Cooldown period prevents alert spam
- Comprehensive incident logging
- Actionable recommendations provided

### 5. Video Timeline Analysis
- Frame-by-frame processing
- Peak crowd identification
- Danger level distribution charts
- Historical trend analysis

## 🏗️ System Architecture
```
Input (Camera/Video)
        ↓
Preprocessing (Grayscale, Blur)
        ↓
People Detection (Contours)
        ↓
Crowd Analysis & Classification
        ↓
Alert Generation & Visualization
        ↓
Dashboard Display
```

## 🌐 Real-World Deployment

### For Production Use:

**1. Connect to CCTV Cameras**
```python
camera_url = "rtsp://username:password@camera_ip:554/stream"
cap = cv2.VideoCapture(camera_url)
```

**2. Setup Alert Notifications**
- SMS alerts via Twilio
- Email notifications via SMTP
- WhatsApp Business API integration

**3. Deploy on Server**
- Use dedicated server or cloud instance
- Configure 24/7 monitoring
- Setup backup systems

## 📁 Project Structure
```
Dhristi/
├── README.md              # Project documentation
├── requirements.txt       # Python dependencies
├── dhristi_app.py        # Main application code
└── screenshots/           # Dashboard screenshots
    ├── dashboard.png
    ├── heatmap.png
    └── analysis.png
```

## 💡 Use Cases

- 🕉️ **Religious Gatherings**: Mahakumbh, Hajj, temple festivals
- 🎪 **Concerts & Events**: Music festivals, cultural programs
- ⚽ **Sports Events**: Stadiums, marathons
- 🏛️ **Political Rallies**: Public meetings, protests
- 🏬 **Shopping Centers**: Malls during sales, holiday rush
- 🚉 **Transportation Hubs**: Railway stations, airports, bus terminals
- 🎓 **Educational Institutions**: Campus events, examinations
- 🏥 **Healthcare Facilities**: Hospital crowds, vaccination drives

## 🔧 Configuration

Customize thresholds in `dhristi_app.py`:
```python
self.safe_threshold = 150        # Adjust for your venue
self.moderate_threshold = 250
self.critical_threshold = 350
```

## 🚀 Future Enhancements

- [ ] Deep Learning integration (YOLO v8 for better accuracy)
- [ ] Multi-camera synchronization
- [ ] Mobile app for field officers
- [ ] Predictive analytics using ML
- [ ] Weather integration for risk assessment
- [ ] SMS/Email alert system
- [ ] Database for historical analysis
- [ ] Cloud deployment
- [ ] Facial recognition (optional, for security)
- [ ] Drone integration for aerial views

## 🎓 Academic Details

**Project Type**: Mini Project  
**Domain**: Computer Vision, AI for Social Good  
**Applications**: Public Safety, Crowd Management  
**Technologies**: Python, OpenCV, Machine Learning, Web Development  

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Divyam Jangada**
**Yashraj Nikam**
**Aditya lagad**
**Palak Chawarkar**

- GitHub: [@Divyamjangada](https://github.com/Divyamjangada)
- Project Link: [Dhristi Crowd Analyzer](https://github.com/Divyamjangada/dhristi-crowd-analyzer)

## 🙏 Acknowledgments

- OpenCV community for computer vision tools
- Gradio team for the web interface framework
- All contributors and testers
- Inspired by the need for better crowd safety at public gatherings

## 📞 Support

For questions, issues, or deployment assistance:
- Open an issue on GitHub
- Contact via GitHub profile

## ⭐ Show Your Support

Give a ⭐️ if this project helped you or could save lives!

---

<div align="center">

**Dhristi - Protecting Lives Through Technology** 💙

*Built with passion for public safety*

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.8+-green.svg)](https://opencv.org)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>
