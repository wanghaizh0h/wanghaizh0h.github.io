# 👨‍💻 Projects
## 1. Vision System for Unmanned Aerial Vehicle Swarms

`Mar.2021 ~ Mar. 2023`

**Brief Description:** This project builds a neural network (NN)-based vision system that integrates advanced vision techniques, including target detection, action recognition, distance measurement, etc. This system can efficiently extract real-time flight vision information to provide essential data for downstream formation control tasks and perform environmental perception and dynamic decision-making. Particularly, to achieve fast and robust responses on the resource-constrained system on chip (SoC), a pipeline framework is integrated to parallelize all workflows and utilize the NN speedup technique to accelerate model inference.

**My Contributions:**

- **Modular System Framework Design and Implementation:** I use a modular framework to construct our vision system with four core modules, each responsible for a specific function—data acquisition, algorithm execution, data packaging and transmission, and log recording. This modular design effectively streamlines data flow, enhancing system adaptability and scalability.
- **System Workflow Optimization:** A pipelined parallel architecture is designed to reconstruct the traditional sequential workflow, leveraging shared memory and locking mechanisms to enable efficient inter-process data synchronization. This design achieves a significant reduction in end-to-end processing latency, making a shift from second-level to millisecond-level performance (1.04s $\rightarrow$ 55ms).
- **Algorithm Performance Optimization:** TensorRT and FP16 quantization techniques are first introduced to shorten the response latency of all NN models  (2.8x $\sim$ 5.8x speedup), and then a linear interpolation approach is proposed to increase the response frequency of the distance measurement algorithm (18 FPS $\rightarrow$ 30 FPS).


## 2. Intelligent Traffic Monitoring System

`Sep. 2022 - Dec. 2022`

**Brief Description:** This project develops efficient visual models to realize real-time traffic violations monitoring. In particular, limited by resource-constrained terminal devices, TensorRT and quantization techniques are applied to accelerate the response speed of vision NN models. This enables instant analysis on video streams from multiple high-definition cameras with low-cost SoC, providing an economical and energy-efficient digital solution for urban traffic management.

**My Contributions:**

- **Dataset Creation:** I first make up a comprehensive dataset annotation specification document, and then train and organize students to use DarkLabel Tool to complete precise and detailed annotation work for high-definition video streams, generating high-quality datasets to train accurate YoloV5 models.
- **Technological Route Design:** I specify a well-decoupled multi-thread procedure architecture as the basic framework of this project, which can parallelize multi-source video stream parsing, visual algorithm execution, and cloud data synchronization in an efficient manner, reducing system latency and development cost.


## 3. Posture Identification- and Adaptive Lifting-based Smart Desk

`May. 2019 - Jul. 2019`

**Brief Description:** This project aims to help users develop good posture and protect their eyesight. We implement an integrated design that combines software, hardware, and algorithms. The posture identification algorithm detects poor sitting habits and provides instant reminders, while the adaptive lifting algorithm drives the smart desk to automatically adjust to a comfortable height. To further promote healthy habits, an Android app allows users to visualize their data in detail, enabling them to track their progress and make scientific adjustments.

**My Contributions:**

- **Hardware and Software Co-Development:** I integrate a Raspberry Pi as the core controller of the smart desk, enabling compact and seamless coordination between hardware and software. The Raspberry Pi communicates with a cloud server for health data synchronization and links with local hardware components such as LED lights, motors, cameras, and buzzers for real-time identification and precise control.
- **Real-Time Data Visualization:** I develop a parent app that automatically generates professional visual reports. With a variety of charts (line, bar, pie), it provides an intuitive way for parents to track their children's health habits, including posture, eye usage, viewing distance, and other relevant health trends.
- **Posture Identification Algorithm:** I first utilize facial keypoint detection and human skeletal joint localization algorithms to extract critical feature points data. Then, I analyze the spatial relationships of these data and classify them to a specific posture to swiftly complete identification.
- **Adaptive Lifting Algorithm:** This system leverages trigonometric functions and human body keypoint detection algorithms to calculate the optimal height range, and then controls the motor-driven mechanical linkage for automatic height adjustment of the smart desk. Note that a steady feedback regulation mechanism is introduced for smoother and safer lifting.


