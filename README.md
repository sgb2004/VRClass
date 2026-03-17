# 🎓 VRClass: Immersive 3D Virtual Classroom

![Unity](https://img.shields.io/badge/Unity-100000?style=for-the-badge&logo=unity&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)


> **Say goodbye to "Zoom fatigue."** VRClass is a cross-platform desktop application that transforms remote education into an interactive, synchronized 3D experience using AI-generated avatars and webcam-based motion capture—no VR headsets required.

---

## ✨ Key Features

* **🤖 AI-Driven Personalization:** Generates highly realistic, custom 3D avatars using mathematical parameter injection onto high-fidelity meshes (**PSHuman** & **SMPL-X**).
* **🎥 Hardware-Free Motion Capture:** Animates your avatar in real-time using only a standard webcam. Powered by **MediaPipe** pose extraction and custom Python kinematics.
* **🌐 Scalable Multiplayer:** Low-latency transform and state synchronization across all connected clients via **Unity NetCode**.
* **🎙️ Classroom Audio:** Integrated **Vivox** common-channel audio ensures clear, non-positional voice communication between teachers and students.
* **🌉 Bidirectional Web Bridge:** Seamlessly connects the Unity 3D engine with a dynamic React/Vue web frontend via a custom JS Bridge.
* **💻 Cross-Platform:** Native standalone builds optimized for Windows, Linux, and macOS.

---

## 🏗️ System Architecture

*(Optional: Replace the link below with the actual path to your architecture diagram)*
![VRClass Architecture](Assets/Architecture_VRClass.png)

VRClass operates on a modular client-server architecture:
1.  **Avatar Engine (Server):** Handles the initialization of PSHuman prefabs, SMPL-X parameter computation, and VRM conversion.
2.  **Animation Engine (Client):** Captures video, extracts 3D pose coordinates via MediaPipe, and transmits bone rotations to the rendering engine via a local socket server.
3.  **Multiplayer Sync (Server/Client):** A centralized Load Balancer and Class Instance Manager syncs character states, audio channels, and shared educational resources.

---

## 🛠️ Technology Stack

| Category | Technologies |
| :--- | :--- |
| **Core Engine** | Unity (Standalone Desktop), Blender (`.glb` assets) |
| **AI & MoCap** | Python, MediaPipe, PSHuman, SMPL-X |
| **Networking** | Unity NetCode, Unity Socket Server, Task Scheduler |
| **Audio/Comms** | Unity Gaming Services (Vivox) |
| **Frontend UI** | React / Vue, JavaScript Bridge |

---

## 🚀 Getting Started

### Prerequisites
* [Unity Hub](https://unity.com/download) (Version 2022.3 LTS or higher recommended)
* [Python 3.8+](https://www.python.org/downloads/)
* Webcam (for motion capture)

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/VRClass.git](https://github.com/yourusername/VRClass.git)
    cd VRClass
    ```

2.  **Run the Unity Client:**
    * Open the `UnityProject` folder in Unity Hub.
    * Open the `MainClassroom` scene.
    * Hit **Play**!

*(Note: Downloadable pre-compiled builds for Windows, Mac, and Linux are available on our landing page.)*

---
