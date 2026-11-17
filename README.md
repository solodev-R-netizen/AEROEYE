# AEROEYE
This project presents AeroEye, a sophisticated autonomous aerial tracking system that integrates high-level artificial intelligence with low-level embedded hardware control. Unlike traditional manual drone operation, this system utilizes a closed-loop feedback mechanism driven by the YOLOv8 (You Only Look Once) object detection architecture to achieve precise, real-time pursuit of dynamic targets. The project’s technical core is a dual-environment software ecosystem consisting of a Python-based Ground Control Station (GCS) and an ESP32-powered Flight Controller (FC), communicating over a low-latency wireless network.

• Operating System:
The GCS runs on Windows 10/11 or Ubuntu Linux 20.04+. Linux is preferred for lower
network overhead, though Windows is supported via the CustomTkinter GUI.

• Primary Programming Environment:
Python 3.10 or 3.11 is the core language for the GCS. It handles the AI logic, PID math,
and UDP socket management. The ESP32 utilizes the Arduino IDE with the C++
framework for high-speed hardware execution.

• Artificial Intelligence Framework:
The Ultralytics YOLOv8 library is used for real-time object detection. The model is loaded
in .pt (PyTorch) or .engine (TensorRT) format to maximize speed.

• Computer Vision Libraries:
OpenCV (Open Source Computer Vision Library) is used for image pre-processing,
MJPEG stream decoding, and drawing the real-time tracking overlays (bounding boxes and
coordinate markers).

• Networking & Protocols:
The system requires the Socket library for UDP communication. The IP Webcam
application (Android/iOS) is used as the bridge to convert smartphone hardware data into
a network-accessible JSON/MJPEG format.

• Graphical User Interface (GUI):
CustomTkinter is used to build the control dashboard. This modern Python library allows
for a responsive, multi-threaded interface that displays live telemetry without slowing
down the AI detection loop.
