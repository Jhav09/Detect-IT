# Motion Detection and Alert System 📷✉️

A real-time motion detection system using OpenCV that captures an image when movement is detected and sends it via email.

## Features

- Detects motion through webcam using frame differencing.
- Captures and stores the frame with detected motion.
- Sends the captured image as an email alert.
- Automatically cleans up stored images to save space.
## Requirements

- Python 3.6+
- OpenCV
- `smtplib`, `imghdr`, `email`, `glob`, `threading`

Install dependencies:
```bash
pip install opencv-python
