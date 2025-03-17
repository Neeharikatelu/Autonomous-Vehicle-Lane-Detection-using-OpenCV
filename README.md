# Road Lane Detection  

## Aim  
Develop a road lane detection system using Python and computer vision.  

## Objective  
Accurately identify lane markings under various conditions (night, curves, fog, rain, zebra crossings, sandy roads) for real-time lane detection in autonomous driving.  

## Methodology  
1. Video Processing: Capture and decode frames.  
2. Preprocessing: Convert to grayscale, apply Gaussian blur, and detect edges using Canny.  
3. ROI Selection: Focus on lane areas.  
4. Lane Detection: Use Hough Transform to identify lane lines.  
5. Visualization: Overlay detected lanes on frames.  
6. Real-time Processing & Evaluation: Assess accuracy for autonomous applications.  

## Motivation  
- Autonomous Driving: Enhances vehicle navigation.  
- ADAS Integration: Provides lane departure warnings.  
- Safety Improvement: Reduces lane departure risks.  
- R&D: Advances computer vision for self-driving tech.  

## Expected Results
The goal is to develop a lane detection system capable of processing both static images and dynamic video streams. The initial focus is on refining image-processing algorithms before advancing to video analysis.

## Processing Steps  
1. Grayscale Conversion: Simplifies the image to a single channel for better edge detection.  
2. Gaussian Blur: Reduces noise and smooths intensity variations.  
3. Canny Edge Detection: Identifies significant intensity changes to highlight lane markings.  
4. Zoomed Edge Detection: Provides a closer view of detected edges.  
5. Region Selection Mask: Focuses on the road area where lane markings are typically present.  
6. Final Output: Displays only lane markings within the selected region.

---

## Evaluation and Enhancements  
During testing, detecting lanes on curved roads was challenging due to camera distortion, impacting accuracy. To address this, the system was improved to:  
1. Enhance Curved Road Detection: Optimized algorithms for accurate lane tracking on curved roads.  
2. Implement Directional Guidance: Determines whether the vehicle should turn left or right based on lane curvature, improving navigation accuracy.

---

### Challenges  
1. Curved Road Detection: Existing algorithms struggle with non-linear lane patterns.  
2. Lane Boundary Ambiguity: Difficulties in distinguishing merging or splitting lanes.  
3. Varying Lane Marking Patterns: Differences in road geometry impact detection reliability.  
4. Limited Field of View: Camera constraints affect lane visibility in curves.

---

### Curved Road Detection Algorithm  
1. Calibration & Undistortion: Corrects lens distortion for accurate road representation.  
2. Image Thresholding: Applies Sobel edge detection and HLS color thresholding to isolate lane lines.  
3. Lane Detection Pipeline:  
   - Corrects image distortion.  
   - Combines gradient and color thresholding for lane identification.  
   - Warps perspective for a bird’s-eye view.  
   - Uses a sliding window method to detect lanes.  
   - Draws lane boundaries and visualizes road conditions in real-time.  

---

## Additional Challenges
Despite improvements, our system faces challenges in:

Foggy & Rainy Weather – Reduced lane visibility.
Night Driving – Low lighting conditions.
Improper Camera Angles – Distorted lane perspective.
Sandy Roads – Faint or absent lane markings.
Zebra Crossings & Pedestrians – Interference with lane tracking.
Wide Lane Gaps – Difficulty in continuous lane detection.
Highway & City Roads – Complex traffic and varying lane structures.

## Final Results  
1. Improved Curved Road Detection: Enhanced accuracy in identifying and tracking lane markings, even in distorted perspectives.  
2. Directional Guidance Implementation: Real-time analysis of lane curvature enables accurate left/right navigation assistance.  

## Future Scope
Our system successfully detects lanes on straight and curved roads, integrating directional guidance for improved navigation. 
However, further enhancements are required for challenging real-world conditions like adverse weather, urban environments, and pedestrian considerations. 
These improvements will bring us closer to a more robust and reliable lane detection system for autonomous driving.


## 🛠️ Installation
## 🔧 Requirements
Python 3.x 🐍
OpenCV 🖼️
NumPy 🔢
Matplotlib 📊


