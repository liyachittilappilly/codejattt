

# CODE JATT Tiger Vision Hub 🐯

![Flying Jatt Logo](https://www.pngitem.com/pimgs/m/297-2978829_a-flying-jatt-netflix-flying-jatt-logo-png.png)

A powerful computer vision web application that brings the action-packed energy of Tiger to image and video analysis. This hub features multiple AI-powered detection tools with a sleek, dark-themed interface inspired by the Flying Jatt.

## Features

### 🏋️ Abs Blaster
Advanced AI-powered system that detects and analyzes abdominal muscles in images.

![Abs Detector](https://i.pinimg.com/1200x/b2/4b/d3/b24bd3f2b0c3817ed95fe8035b05d906.jpg)

### 📊 Barcode Breaker
Precisely counts and analyzes barcode lines in images with sniper-like accuracy.

![Barcode Counter](https://barcode-test.com/wp-content/uploads/2015/05/Flexo-with-Fat-Bars.jpg)

### 👁️ Eye Spy
Detects and counts eyes in both uploaded images and real-time camera feeds.

![Eye Counter](https://i.pinimg.com/736x/ac/66/26/ac66261160b201e5406686c358c48f86.jpg)

### 🐱 Cat Boss Counter
Uses YOLOv8 to detect and count cat heads with deadly accuracy.

![Cat Head Counter](https://i.pinimg.com/736x/f0/ca/6b/f0ca6b24c54cfcb7a6e160239895ed0a.jpg)

### 🫧 Bubble Smash
Counts and analyzes bubbles in images with advanced circularity detection.

![Bubble Counter](https://i.pinimg.com/1200x/65/15/96/651596694df46ca0ec89e39415ed6299.jpg)

### 🖌️ Bristle Buster
Detects and counts bristles in images using edge detection and line analysis.

![Bristle Counter](https://i.pinimg.com/736x/3d/b5/24/3db5241121df55878dd802ef840958f0.jpg)

### 🌧️ BAAGHI Movie Rain Counter
Detects and counts rain events in videos with advanced temporal analysis.

![Rain Detector](https://i.pinimg.com/736x/86/8b/52/868b52614c4d50b0d0c3d73602d3d396.jpg)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/tiger-vision-hub.git
cd tiger-vision-hub
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install the required dependencies:
```bash
pip install -r requirements.txt
```

4. Run the application:
```bash
python app.py
```

5. Open your browser and navigate to `http://localhost:5000`

## Usage

### Using the Detectors

1. Select a detector from the homepage
2. Upload an image or video (depending on the detector)
3. Click the analyze button to process the media
4. View the results and visualization

### Training the Abs Model

The Abs Blaster requires training before first use:

1. Click the "Train Model" button on the Abs Blaster card
2. Upload images of abs and non-abs in the respective sections
3. Click "Upload Data" then "Train Model"
4. Wait for training to complete (this may take several minutes)
5. The detector will be ready to use after training

### Real-time Eye Detection

The Eye Spy feature supports real-time camera detection:

1. Click on the "Camera" tab
2. Click "Start" to activate your camera
3. The system will detect and count eyes in real-time
4. Click "Stop" to end the camera session

## Technologies Used

- **Backend**: Flask, Python
- **Computer Vision**: OpenCV, MediaPipe, Ultralytics (YOLOv8)
- **Machine Learning**: TensorFlow, Scikit-learn
- **Frontend**: HTML5, CSS3, JavaScript, Bootstrap
- **Image Processing**: NumPy, Matplotlib

## Project Structure

```
tiger-vision-hub/
├── app.py                 # Main Flask application
├── train_abs.py           # Script for training the abs detector
├── requirements.txt       # Python dependencies
├── static/
│   └── css/
│       └── style.css      # Custom CSS styles
├── templates/
│   └── index.html         # Main HTML template
├── uploads/               # Temporary storage for uploaded files
├── results/               # Storage for processed results
├── models/                # Trained models
└── data/                  # Training data
    ├── 0/                 # Non-abs images
    └── 3/                 # Abs images
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the energy and style of Tiger Shroff's characters
- Powered by state-of-the-art computer vision libraries
- Designed with the action-packed aesthetic of the Flying Jatt

---

<div align="center">
  <p style="color: #1a5276; font-size: 1.2em; font-weight: bold;">Tiger Vision Hub © 2025 - Bringing Action to Computer Vision</p>
  <img src="https://www.pngitem.com/pimgs/m/297-2978829_a-flying-jatt-netflix-flying-jatt-logo-png.png" alt="Flying Jatt" width="100">
</div>
