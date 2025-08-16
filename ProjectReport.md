

# Code Jatt Tiger Vision Hub - Project Report

![Project Logo](https://www.pngitem.com/pimgs/m/297-2978829_a-flying-jatt-netflix-flying-jatt-logo-png.png)

## Project Overview
Code Jatt Tiger Vision Hub is a comprehensive computer vision web application built with Flask that provides multiple image and video analysis features. The application has a dark blue-themed interface with a flying jatt logo, offering various detection and counting capabilities through advanced AI models.

## Features

### 1. Abs Blaster (Abs Detector)
![Abs Detector](https://i.pinimg.com/1200x/b2/4b/d3/b24bd3f2b0c3817ed95fe8035b05d906.jpg)
  <img src="Screenshot 2025-08-09 201414.png" alt="Demo Screenshot" width="500"/>
  
**Description**: Advanced AI system that detects the presence of abdominal muscles in images, classifying them as "Abs" or "No Abs" with confidence scores.

**Technical Implementation**:
- Uses VGG16 as a feature extractor
- Random Forest classifier for prediction
- Custom training capability through web interface
- Image preprocessing and normalization

**Key Features**:
- Real-time classification with confidence scores
- Model training through web interface
- Visual result generation with predictions

### 2. Barcode Breaker (Barcode Counter)
![Barcode Counter](https://barcode-test.com/wp-content/uploads/2015/05/Flexo-with-Fat-Bars.jpg)
  <img src="Screenshot 2025-08-16 150843.png" alt="Demo Screenshot" width="500"/>

  
**Description**: Precisely counts the number of lines in barcode images using advanced image processing techniques.

**Technical Implementation**:
- Grayscale conversion and Gaussian blur
- Adaptive thresholding with binary inversion
- Vertical projection profile analysis
- Peak detection with minimum width constraints

**Key Features**:
- Accurate line counting in barcodes
- Visualization of detected lines
- Robust to different barcode formats

### 3. Eye Spy (Eye Counter)
![Eye Counter](https://i.pinimg.com/736x/ac/66/26/ac66261160b201e5406686c358c48f86.jpg)
  <img src="Screenshot 2025-08-16 144812.png" alt="Demo Screenshot" width="500"/>
  
**Description**: Detects and counts eyes in both uploaded images and real-time camera feeds using MediaPipe Face Mesh.

**Technical Implementation**:
- MediaPipe Face Mesh for facial landmark detection
- Eye landmark identification (left and right eye indices)
- Real-time camera feed processing
- Visibility-based eye counting

**Key Features**:
- Dual mode: image upload and real-time camera
- Accurate eye counting with visualization
- Real-time processing with frame-by-frame analysis

### 4. Cat Boss Counter (Cat Head Counter)
![Cat Head Counter](https://i.pinimg.com/736x/f0/ca/6b/f0ca6b24c54cfcb7a6e160239895ed0a.jpg)
  <img src="Screenshot 2025-08-16 150925.png" alt="Demo Screenshot" width="500"/>
  
**Description**: Detects cats in images and counts the number of heads using YOLOv8 and advanced contour analysis.

**Technical Implementation**:
- YOLOv8 pre-trained on COCO dataset (class 15 for cats)
- Contour analysis and convexity defects detection
- Skin color segmentation for head region identification
- Head point localization

**Key Features**:
- Accurate cat detection using YOLOv8
- Head counting with visual markers
- Centroid and head point visualization

### 5. Bubble Smash (Bubble Counter)
![Bubble Counter](https://i.pinimg.com/1200x/65/15/96/651596694df46ca0ec89e39415ed6299.jpg)
  <img src="Screenshot 2025-08-16 150952.png" alt="Demo Screenshot" width="500"/>
  
**Description**: Counts bubbles in images using multiple thresholding techniques and circularity analysis.

**Technical Implementation**:
- Multiple thresholding methods (Otsu, Adaptive, Inverted)
- Morphological operations for noise removal
- Contour filtering by area and circularity
- Best method selection algorithm

**Key Features**:
- Robust bubble detection with multiple methods
- Circular shape analysis
- Visual result generation with count overlay

### 6. Bristle Buster (Bristle Counter)
![Bristle Counter](https://i.pinimg.com/736x/3d/b5/24/3db5241121df55878dd802ef840958f0.jpg)
  <img src="Screenshot 2025-08-16 151037.png" alt="Demo Screenshot" width="500"/>
  
**Description**: Counts bristles in brush images using edge detection and line analysis.

**Technical Implementation**:
- Contrast enhancement using CLAHE
- Canny edge detection
- Probabilistic Hough Transform for line detection
- Vertical line filtering based on angle

**Key Features**:
- Precise bristle counting
- Visual differentiation of detected bristles
- Angle-based filtering for accuracy

### 7. BAAGHI Movie Rain Counter (Rain Detector)
![Rain Detector](https://i.pinimg.com/736x/86/8b/52/868b52614c4d50b0d0c3d73602d3d396.jpg)
  <img src="Screenshot 2025-08-09 214204.png" alt="Demo Screenshot" width="500"/>
  
**Description**: Detects and counts rain events in videos using background subtraction and temporal analysis.

**Technical Implementation**:
- Background subtraction using MOG2
- Feature extraction (foreground density, edge density, intensity)
- Streak analysis using Hough Line Transform
- Temporal smoothing with deque buffer
- Rule-based classification with probability scoring

**Key Features**:
- Video processing for rain detection
- Multi-feature analysis
- Temporal smoothing for robust detection
- Progress tracking during processing

## Technical Architecture

### Backend
- **Framework**: Flask
- **Computer Vision Libraries**: OpenCV, MediaPipe, Ultralytics (YOLO)
- **Machine Learning**: TensorFlow, Keras, Scikit-learn
- **Data Processing**: NumPy, SciPy

### Frontend
- **UI Framework**: Bootstrap 5
- **Styling**: Custom CSS with dark blue theme
- **Interactivity**: JavaScript for form handling and camera feed
- **Icons**: Font Awesome

### Project Structure
```
project/
├── app.py                 # Main Flask application
├── train_abs.py           # Training script for Abs Detector
├── static/
│   └── css/
│       └── style.css      # Custom styles
├── templates/
│   └── index.html         # Main UI template
├── uploads/               # Uploaded files storage
├── results/               # Result images storage
├── models/                # Trained models storage
└── data/                  # Training data
    ├── 0/                 # Non-abs images
    └── 3/                 # Abs images
```

## Key Technical Highlights

1. **Modular Design**: Each feature is implemented as a separate Flask route with dedicated processing logic.

2. **Real-time Processing**: The eye counter feature supports real-time camera feed processing using MediaPipe.

3. **Model Training**: The Abs Detector includes a complete training pipeline accessible through the web interface.

4. **Multiple Detection Methods**: Many features implement multiple detection algorithms and select the best one automatically.

5. **Visualization**: All features generate visual results with annotations and overlays.

6. **Error Handling**: Comprehensive error handling and user feedback throughout the application.

## Installation and Usage

1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Run the application: `python app.py`
4. Access the web interface at `http://localhost:5000`

## Future Enhancements

1. **Additional Detection Features**: Expand the library with more computer vision capabilities
2. **User Authentication**: Add user accounts to save results and models
3. **Performance Optimization**: Implement caching and parallel processing for faster results
4. **Mobile App**: Develop a companion mobile application
5. **API Integration**: Create RESTful APIs for external integrations

## Conclusion

Code Jatt Tiger Vision Hub is a comprehensive computer vision platform that combines multiple detection and counting capabilities in a user-friendly web interface. With its dark blue theme and flying jatt branding, it offers both powerful functionality and an engaging user experience. The modular architecture allows for easy extension with new features, making it a versatile platform for computer vision applications.
