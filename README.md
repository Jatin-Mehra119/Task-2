# Task-2

- Environment set up
    - Install necessary dependencies for model inference and video preprocessing. See `requirements.txt` for details. Main libraries: PyTorch, OpenCV, matplotlib.

- Load the video using OpenCV
    - Used OpenCV to read and process the input video file (`sample_video.mp4`).

- People Detection using YOLOv5s
    - Loaded the YOLOv5s model using PyTorch Hub. Detected people in each frame using the model's inference.

- Crowd Alert System
    - Tracked the number of people detected in recent frames. Triggered an alert if 3 or more people were detected in 5 consecutive frames.
    - Alerts are logged with frame number, timestamp, and count in `alerts_log.json`.
    - Alert messages are overlaid on the video frames.

- Output Video
    - The processed video with detection boxes and alert overlays is saved as `output_with_alerts.avi`.

- Alert Timeline Visualization
    - Plotted a timeline of alert occurrences using matplotlib. Saved as `alerts_timeline.png`.

## How to Run

1. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
2. Place your input video as `sample_video.mp4` in the project directory. (video file in Google Drive)
3. Run the notebook `task_2.ipynb` or execute the code in a Python environment.
4. Output files (`output_with_alerts.avi`, `alerts_log.json`, `alerts_timeline.png`) will be generated in the project directory.

## Files
- `task_2.ipynb`: Main notebook with code for detection and alert system.
- `output_with_alerts.avi`: Output video with detection and alerts. (Saved in Google Drive)
- `alerts_log.json`: Log of alert events.
- `alerts_timeline.png`: Visualization of alert timeline.
- `requirements.txt`: List of required Python packages.
- Video:https://drive.google.com/drive/folders/1owdeqkyFKDBJag7jL_6yaZZH_vP9_B-z?usp=sharing

## Notes
- Press 'q' during video playback to exit early.
- The alert system is tuned for crowd detection (3+ people in 5 consecutive frames).