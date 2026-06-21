![BioSignal-Interface](<asset/ChatGPT Image Jun 20, 2026, 09_43_27 PM.png>)

![Status](https://img.shields.io/badge/status-experimental-red)
![ESP32](https://img.shields.io/badge/platform-ESP32-blue)


<p align="center">
  <a href="https://awakenfury.github.io/BioSignal-Interface/">
    🌐 Live Demo
  </a>
</p>

# BioWearable-Neural-Core
BioWearable Neural Core is an experimental six-channel electromyography (EMG) platform designed to capture, visualize, classify, and replay muscle activation patterns in real time using an ESP32.


# 🧠 BioWearable Neural Core

### Real-Time Multi-Channel EMG Interface for Human Motion Analysis and Experimental Control Systems

![ESP32](https://img.shields.io/badge/ESP32-Async%20WebServer-red)
![EMG](https://img.shields.io/badge/EMG-6%20Channels-blue)
![WebSocket](https://img.shields.io/badge/WebSocket-Real--Time-green)
![Status](https://img.shields.io/badge/Status-Experimental-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## Overview

BioWearable Neural Core is an experimental six-channel electromyography (EMG) platform designed to capture, visualize, classify, and replay muscle activation patterns in real time using an ESP32.

The system combines embedded signal processing, browser-based telemetry, lightweight pose classification, and future-ready data infrastructure into a single wearable neural interface architecture.

At its current stage, the project focuses on rapid EMG acquisition and local inference. Future iterations are intended to expand into long-term storage, machine learning workflows, robotics integration, and private cloud synchronization through Network Attached Storage (NAS) systems.

This project is intended for experimentation, education, prototyping, and research exploration.

---

## Core Objectives

* Capture six independent EMG channels simultaneously.
* Perform low-latency signal filtering directly on the ESP32.
* Extract signal features using rolling RMS windows.
* Classify predefined muscle activation patterns locally.
* Stream telemetry to a browser dashboard using WebSockets.
* Record sessions for offline analysis and replay.
* Provide fine-tuning controls for calibration.
* Build a scalable architecture capable of evolving into larger neural interaction systems.

---

## Current Features

### Embedded Neural Processing

The ESP32 performs signal processing without requiring an external computer.

Current processing pipeline:

1. Multi-channel analog acquisition
2. Exponential moving average filtering
3. Rolling RMS feature extraction
4. Threshold gating
5. Lightweight rule-based pose classification
6. Immediate action dispatch

---

### Six-Channel EMG Architecture

Current muscle layout:

| Channel | Example Placement       | Functional Purpose     |
| ------- | ----------------------- | ---------------------- |
| CH1     | Wrist Flexor / Extensor | Fine wrist activity    |
| CH2     | Forearm Supinator       | Grip contribution      |
| CH3     | Bicep Pull Vector       | Extension detection    |
| CH4     | Tricep Extension        | Counter-force analysis |
| CH5     | Anterior Deltoid        | Rotational movement    |
| CH6     | Trapezius Anchor        | Stability and support  |

The placement strategy can be modified depending on the application.

---

### Real-Time Browser Dashboard

The ESP32 hosts its own web interface through Wi-Fi Access Point mode.

Dashboard capabilities include:

* Live six-channel oscilloscope visualization
* Independent channel displays
* RMS calculations
* Adjustable filter alpha values
* Threshold tuning sliders
* Session recording
* Replay mode
* CSV export
* Pose activity visualization
* Connection monitoring

No external software installation is required.

Users simply connect to the ESP32 access point and open the hosted dashboard.

---

### On-Chip Pose Classification

The current classifier uses rule-based inference derived from EMG activation relationships.

Implemented states include:

* REST / IDLE
* POWER GRIP
* ARM EXTENSION
* ROTATIONAL TWIST

The classification engine is intentionally lightweight to minimize latency.

Future versions may support:

* Adaptive thresholds
* User-specific calibration profiles
* TinyML inference
* Neural network models
* Sequence-based classification

---

## Data Recording and Replay

The dashboard includes a built-in session capture system.

Captured sessions allow users to:

* Record muscle activation sequences.
* Export datasets to CSV.
* Replay captured movements.
* Analyze activation timing.
* Build training datasets.

This functionality is intended to support future machine learning development.

---

## Future NAS Cloud Infrastructure

One of the long-term goals of BioWearable Neural Core is the integration of private cloud storage through NAS systems.

Rather than relying exclusively on third-party cloud providers, the project aims to support self-hosted storage solutions.

Potential capabilities include:

### Dataset Archiving

Store long-term EMG recordings.

* CSV datasets
* Calibration sessions
* Subject profiles
* Experimental logs

---

### Multi-Device Synchronization

Synchronize recordings across devices.

Examples:

* Desktop analysis workstations
* Research laptops
* Secondary dashboards
* Companion wearable nodes

---

### Machine Learning Repository

Maintain centralized datasets for training future models.

Possible workflows:

ESP32 → Dashboard → NAS → Model Training → Model Deployment

---

### Private Research Infrastructure

NAS integration enables:

* Local ownership of experimental data
* Controlled access permissions
* Reduced dependence on external services
* Expandable storage capacity

---

## Potential Future Directions

The architecture has been intentionally designed to remain modular.

Possible expansions include:

### TinyML Integration

Deploy lightweight models directly onto embedded hardware.

Examples:

* Gesture recognition
* Adaptive calibration
* Fatigue detection
* Personalized classifiers

---

### Robotics Control

Use EMG patterns to drive:

* Prosthetic hand simulators
* Servo-actuated systems
* Robotic manipulators
* Exoskeleton prototypes

---

### Multi-Sensor Fusion

Combine EMG with additional sensors such as:

* IMUs
* Environmental sensors
* Force sensors
* Pressure arrays
* Biofeedback systems

---

### Private Neural Data Pipeline

Future architecture concept:

```
EMG Sensors
     ↓
ESP32 Neural Core
     ↓
Web Dashboard
     ↓
NAS Storage
     ↓
Analytics / Machine Learning
     ↓
Updated Embedded Models
```

---

## Experimental Status

BioWearable Neural Core is an evolving experimental project.

It should not be considered a medical device and is not intended for diagnosis, treatment, or clinical decision-making.

The project exists to explore human-machine interaction, embedded signal processing, wearable computing, and future neural interface concepts.

---

## Hardware Requirements

Current implementation:

* ESP32 Development Board
* 6× EMG channels (MyoWare or equivalent analog sources)
* Wi-Fi capable device for dashboard access
* Power source appropriate for wearable experimentation

Future optional additions:

* NAS server
* IMU modules
* Robotic actuators
* Additional sensor arrays
* TinyML accelerators

---

## License

This project is released under the MIT License.

Contributions, experimentation, and educational adaptation are encouraged.

---

## Vision

BioWearable Neural Core represents an exploration into accessible neural interfaces built from commodity hardware.

The immediate objective is real-time understanding of muscle activity.

The longer-term vision is a modular ecosystem where wearable sensing, embedded intelligence, private data ownership, and adaptive control systems converge into a continuously evolving experimental platform.
