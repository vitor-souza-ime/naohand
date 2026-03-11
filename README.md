# 🤖 Gesture-Based Control of the NAO Humanoid Robot Using Computer Vision and MediaPipe

This repository presents an implementation of **real-time hand gesture recognition** to enable **gesture-based interaction with the NAO humanoid robot** using **Computer Vision** and **MediaPipe Hands**.

The system captures images from the **NAO robot camera**, processes them using **MediaPipe**, and identifies basic hand gestures such as **open hand** and **closed hand**. These gestures can be used to control robot behaviors or trigger actions such as **speech feedback**.

This work supports the research presented in the article:

**Gesture-Based Control of the NAO Humanoid Robot Using Computer Vision and MediaPipe: An Approach for Real-Time Human-Robot Interaction**

---

# 📌 Overview

Human–Robot Interaction (HRI) is an important research area in robotics. Vision-based gesture recognition enables **natural and intuitive communication** between humans and robots.

This project implements:

* 📷 Image acquisition from the **NAO camera**
* ✋ **Hand detection and tracking** using MediaPipe
* 🔢 **Finger-based gesture recognition**
* 🗣 Optional **speech feedback using NAO Text-to-Speech**
* ⚡ **Real-time processing**

The system can be extended to control robot behaviors such as:

* Navigation
* Movement commands
* Interaction tasks
* Educational robotics applications

---

# 🧠 Technologies Used

The implementation relies on the following technologies:

* **Python**
* **NAOqi SDK**
* **OpenCV**
* **MediaPipe**
* **NumPy**

---

# ⚙️ System Architecture

The interaction pipeline follows these steps:

```
NAO Camera
     │
     ▼
Image Acquisition (ALVideoDevice)
     │
     ▼
Computer Vision Processing
(OpenCV + MediaPipe)
     │
     ▼
Hand Landmark Detection
     │
     ▼
Gesture Classification
     │
     ▼
Robot Response
(Text-to-Speech / Control Commands)
```

---

# 📂 Project Structure

```
gesture-nao-mediapipe/
│
├── gesture_nao.py        # Main implementation script
├── README.md             # Project documentation
└── requirements.txt      # Python dependencies
```

---

# 🔧 Installation

## 1️⃣ Install Python Dependencies

```bash
pip install opencv-python mediapipe numpy
```

If using NAOqi Python SDK:

```bash
pip install qi
```

Or install it from the official SoftBank Robotics SDK.

---

# 🤖 NAO Robot Configuration

Edit the script and configure the **robot IP address**:

```python
NAO_IP = "172.15.4.178"
NAO_PORT = 9559
```

Make sure:

* Your computer and NAO robot are on the **same network**
* The **NAOqi services** are running

---

# ▶️ Running the System

Execute the script:

```bash
python gesture_nao.py
```

The system will:

1. Connect to the NAO robot
2. Access the robot camera
3. Detect hands using MediaPipe
4. Classify gestures
5. Display results in real time

Press **`q`** to exit.

---

# ✋ Implemented Gestures

| Gesture     | Description                   |
| ----------- | ----------------------------- |
| Open Hand   | Four or more fingers detected |
| Closed Hand | One or zero fingers detected  |
| Unknown     | Any other configuration       |

These gestures can easily be extended to support:

* 👍 Thumbs up
* ✌ Peace sign
* 👆 Pointing
* 🖐 Stop command

---

# 📊 Example Output

```
Open Hand t=0.034s
Closed Hand t=0.029s
Open Hand t=0.031s
```

Where:

* **t** represents the gesture recognition processing time.

---

# 🧪 Research Applications

This project can be used in research areas such as:

* Human-Robot Interaction (HRI)
* Gesture-based robot control
* Educational robotics
* Assistive robotics
* Social robots

---

# 🚀 Possible Extensions

Future improvements may include:

* Integration with **robot motion commands**
* Deep learning gesture classification
* Multimodal interaction (speech + gesture)
* Reinforcement learning for adaptive interaction
* Multi-user gesture detection

---

# 📖 Citation

If you use this work in your research, please cite:

```
Gesture-Based Control of the NAO Humanoid Robot Using Computer Vision 
and MediaPipe: An Approach for Real-Time Human-Robot Interaction.
```

---

# 👨‍🏫 Author

**Prof. Vitor Amadeu**

Research areas:

* Robotics
* Human-Robot Interaction
* Artificial Intelligence
* Computer Vision
* Intelligent Systems

---

# 📜 License

This project is released for **academic and research purposes**.


