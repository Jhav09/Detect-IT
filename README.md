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
```

🗂️ Project Structure
bash
Copy
Edit
.
├── main.py               # Main program: captures video and detects motion
├── emailing.py           # Emailing module to send images with motion
├── tempCodeRunnerFile.py # Temporary scratch file
├── thumb.jpeg            # Sample motion detection image
└── images/               # Runtime folder for storing captured frames

⚙️ How It Works
Captures video from the webcam.

Compares current frame with the initial frame to detect differences.

If motion is found:

Draws a rectangle around the object.

Saves the frame in the images/ folder.

When motion ends (no movement for a moment), it:

Selects the best image.

Sends an email with the image as an attachment.

Cleans up old images using a background thread.

🚀 Getting Started
Run the script with:

bash
Copy
Edit
```
python main.py
Press q to exit the program gracefully.
```

✉️ Email Configuration
Open emailing.py and set your email credentials:

python
Copy
Edit
```
SENDER = "your_email@gmail.com"
RECEIVER = "receiver_email@gmail.com"
PASSWORD = "your_gmail_app_password"
```

🤝 Contribution
Feel free to fork this repo and add your improvements. Pull requests are welcome!
