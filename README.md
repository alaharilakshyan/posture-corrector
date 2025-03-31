# AI Posture Corrector

## Overview
This application uses computer vision and AI to monitor and improve your sitting posture in real-time. Using your webcam and MediaPipe's pose estimation, the system detects poor posture and provides immediate audio and visual feedback to help you maintain proper ergonomic positioning.

## Features
- Real-time posture monitoring
- Personalized calibration to your natural sitting position
- Visual skeleton tracking with angle measurements
- Audio alerts when poor posture is detected
- Simple, intuitive interface with posture status and metrics

## Requirements
- Python 3.6+
- OpenCV
- MediaPipe
- NumPy
- playsound

## Installation
1. Clone this repository
2. Install required packages:
   ```
   pip install opencv-python mediapipe numpy playsound
   ```
3. Ensure you have a working webcam

## Usage
1. Run the application:
   ```
   python main.py
   ```
2. Sit in your ideal ergonomic position for the calibration phase (first 30 frames)
3. The system will then monitor your posture and alert you when it detects poor positioning
4. Press 'q' to quit

## How It Works
The application uses MediaPipe's pose estimation to track key body landmarks, particularly focusing on shoulder and neck angles. After calibration, it establishes threshold values for good posture and provides feedback when your posture falls below these thresholds.

## Customization
You can modify the following parameters in the code:
- `alert_cooldown`: Time between alerts (default: 5 seconds)
- Calibration frames (default: 30)
- Angle thresholds offset (default: 10 degrees below calibration average)

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
[MIT License](LICENSE)
