Face Recognition Project with ESP32 Integration


A Python-based face recognition system using deep learning, integrated with an ESP32 camera module.

🚀 Features

✅ Detect faces from images or video streams

✅ Recognize known faces using a pre-trained PyTorch model (weights.pt)

✅ Integrate with ESP32/Arduino camera for real-time streaming

✅ Works on local images, videos, or live ESP32 feed

✅ Easy to extend for custom datasets

🛠 Requirements

Python 3.8+

PyTorch

OpenCV (opencv-python)

Arduino IDE / ESP32 support

ESP32-CAM module (or similar) for live streaming

🖥 Installation (Python)

Clone the repository

git clone https://github.com/Niloy-Sarker-T/Face_Recog.git
cd Face_Recog


Create a virtual environment (optional)

python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows


Install dependencies

pip install -r requirements.txt


Ensure PyTorch is installed correctly, since weights.pt is a PyTorch model.

🔌 ESP32 Integration

Connect ESP32-CAM to your computer via USB or serial programmer.

Open ESP32_Cam.ino in Arduino IDE and set:

Your Wi-Fi SSID and password

The correct COM port and ESP32 board type

Upload the sketch to ESP32.

Open the Serial Monitor to get the IP address of the camera stream.

Update main.py in Python to use the ESP32 IP stream as input:

esp32_stream_url = "http://<ESP32-IP>/stream"

🎬 Usage

Local images/videos: Place your input in the input/ folder.

ESP32 feed: Set the stream URL in main.py.

Run the main script:

python main.py


Outputs will be saved in the output/ folder.

📦 Model Weights

Pre-trained model file weights.pt (~90 MB) is included.

⚠️ Larger than GitHub recommended 50 MB — consider using Git LFS
 for large files.

🤝 Contributing

Add support for multiple ESP32 cameras

Train with custom datasets

Optimize the model for faster inference

Fork the repository

Create a feature branch: git checkout -b feature-name

Commit your changes: git commit -m 'Add feature'

Push: git push origin feature-name

Open a Pull Request

📝 License

MIT License — free to use and modify.