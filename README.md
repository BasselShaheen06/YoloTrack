# Football Player Detection and Tracking using YOLO and OpenCV

This Python script utilizes OpenCV and YOLO (You Only Look Once) for detecting and tracking football players in match videos. It processes video frames, aligns them with a 2D football pitch, and visualizes player movements and heatmaps.

## Features

- **Player Detection and Tracking**:
  - Detects players in video frames using YOLO.
  - Assigns unique IDs to players based on proximity in consecutive frames.

- **Football Pitch Alignment**:
  - Allows manual selection of reference points on the pitch for coordinate alignment.
  - Computes a transformation matrix to map video coordinates to a standard 2D football pitch.

- **Data Visualization**:
  - Generates movement trails on a 2D football pitch for individual players.
  - Creates heatmaps to highlight high-activity zones for each player.

- **Video Processing**:
  - Processes video frame-by-frame with Non-Maximum Suppression (NMS) for optimized detections.
  - Displays video with overlays showing detected players and their IDs.

- **Exportable Data**:
  - Formats player tracking data for export or further analysis.

## Requirements

1. **YOLO Model Files**:
   - `yolov4.weights`
   - `yolov4.cfg`

2. **A Video File**:
   - A football match video to analyze.

3. **Python Dependencies**:
   - OpenCV
   - NumPy
   - Matplotlib
   - SciPy

Install dependencies using:
```bash
pip install opencv-python-headless numpy matplotlib scipy
Usage
Clone the repository and ensure all required files are in place.

python yolo.py
Manually select four reference points on the pitch:
Top-left corner of the visible pitch area.
Top-right corner of the visible pitch area.
Bottom-left corner of the visible pitch area.
Bottom-right corner of the visible pitch area.
Watch the processed video with player tracking displayed in real-time.
After video processing, visualize player data:
Movement trails on a 2D pitch.
Heatmaps of activity zones.
Suggested Improvements
Enhance player ID assignment to handle occlusions and abrupt stops.
Add detection for other objects, like the football.
Automate data saving in formats like JSON or CSV.
