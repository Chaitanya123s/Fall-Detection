# Fall Detection Using Human Pose Estimation

## Objective
Detect fall events from a video using human pose estimation.

## Technology Used
- Python 3.10
- MediaPipe Pose
- OpenCV
- NumPy

## Project Files
- input_video.mp4
- pose_detection.py
- annotated_video.mp4
- fall_detection_log.txt
- detection_report.txt
- README.md

## Setup
1. Create environment
conda create -n mediapipe_env python=3.10 -y  
conda activate mediapipe_env  

2. Install libraries
pip install mediapipe==0.10.9 opencv-python numpy  

## How to Run
1. Place the video as `input_video.mp4`
2. Run the script
python pose_detection.py  

## Working
- Video processed frame by frame
- MediaPipe Pose extracts skeleton keypoints
- Head, shoulders, hips, and ankles are used
- Vertical body height and torso angle are calculated
- Falls detected when the person stays near the ground
- Multi-frame validation avoids false detection

## Output
- annotated_video.mp4 → skeleton overlay with posture label
- fall_detection_log.txt → fall timestamps
- detection_report.txt → total falls and confidence

## Detection Logic
- Reduced body height
- Horizontal torso orientation
- Confirmed over multiple frames

## Result
- Standing, Bent, and Lying (Fall) postures classified
- Falls logged with timestamps

## Author
Chaitanya T. Suryawanshi
