🚗 자율주행 ROKEYBOT (Real)
===
ROKEY B-1조 협동-3 Project (디지털 트윈 기반 서비스 로봇 운영 시스템 구성)
---

### 🔨 개발환경
본 프로젝트는 Ubuntu 22.04 (ROS2 humble) 환경에서 개발되었습니다.   
&nbsp;

### 🦾 작업공간
<img src="https://github.com/user-attachments/assets/49bff4e1-3291-40fc-b944-a49a6a6ce594" width="75%" height="75%" title="px(픽셀) 크기 설정" alt="project workspace"></img>   
&nbsp;

### 💻 코드 실행

#### **Bringup**
```bash
ros2 launch turtlebot_manipulation_bringup hardware.launch.py
```

#### **Moveit**
```bash
ros2 launch turtlebot3_manipulation_moveit_config moveit_core.launch.py
```

#### **Arm Controller**
```bash
ros2 run turtlebot_moveit turtlebot_arm_controller
```

#### **Detect Lane**
code: [turtle_pubimg.py](turtlebot3_autorace/turtlebot3_autorace_detect/turtlebot3_autorace_detect/turtle_pubimg.py)
```bash
ros2 run turtlebot3_autorace_detect turtle_pubimg
```

#### **Control Lane**
code: [control_lane.py](turtlebot3_autorace/turtlebot3_autorace_mission/turtlebot3_autorace_mission/control_lane.py)
```bash
ros2 launch turtlebot3_autorace_mission control_lane.launch.py
```

#### **Aruco Detect**
code: [aruco_detector.py](aruco_yolo/aruco_yolo/aruco_detector.py)
```bash
ros2 run aruco_yolo aruco_detector
```

#### **Task Aruco**
code: [task_aruco.py](aruco_yolo/aruco_yolo/task_aruco.py)
```bash
ros2 run aruco_yolo task_aruco
```

&nbsp;

### 📷 시연 영상
https://youtu.be/cOo7qpPeUjg (00:21 ~ 01:00)

---

&nbsp;

## 목차

#### [1. 📘 프로젝트 개요](#1--프로젝트-개요-1)   
#### [2. 👥 프로젝트 팀 구성 및 역할분담](#2--프로젝트-팀-구성-및-역할분담-1)   
#### [3. 🗓 프로젝트 구현 일정](#3--프로젝트-구현-일정-1)   
#### [4. 📌 SKILLS](#4--skills-1)   
#### [5. 🤖 Hardware](#5--hardware-1)   
#### [6. 🛠️ Node Architecture](#6-%EF%B8%8F-node-architecture-1)   

---

&nbsp;

## 1. 📘 프로젝트 개요
자율주행 기술의 핵심은 도로의 구조와 교통 상황을 정확히 인식하고, 이를 바탕으로 차량을 안전하고 안정적으로 제어하는 데 있음   
특히 차선 인식 기술은 차량의 주행 경로를 결정하고 차로 유지, 차로 변경 등과 같은 기본적인 자율주행 기능을 구현하는 데 필수적인 핵심 기술임   
본 프로젝트는 TurtleBot3, ROS2를 활용하여 실제 도로 상황을 시뮬레이션하고, 영상 처리 기반의 차선 인식 알고리즘을 개발함으로써 자율주행의 기초 요소 기술을 구현하는 것을 목표로 함   
기존 맵 정보와 실시간 카메라를 융합하여 더욱 정확하고 안정적인 차선 인식 성능을 구현함. 이를 통해 조명 변화, 장애물 인식 등 외부 환경 변화에 대한 강건성을 향상시킴   

&nbsp;

## 2. 👥 프로젝트 팀 구성 및 역할분담
|이름|담당 업무|
|--|--|
|백홍하(팀장)| ARUCO 인식 및 좌표 계산, Manipulation |
|이하빈| 차선 탐지, 터틀봇 이동 로직 |
|장연호| ARUCO 인식 및 좌표 계산, Manipulation |
|정찬원| 차선 탐지, 터틀봇 이동 로직 |

&nbsp;

## 3. 🗓 프로젝트 구현 일정
**진행 일자: 25.06.16(월) ~ 25.06.20(금) (5일)**
<img src="rokey_project/image/notion/250717_project_management.png" width="100%" height="100%" title="px(픽셀) 크기 설정" alt="project_management"></img>

&nbsp;

## 4. 📌 SKILLS
### **Development Environment**
<div align=left>
  
  ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
  ![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
</div>

[![My Skills](https://skillicons.dev/icons?i=ubuntu,vscode&theme=light)](https://skillicons.dev)

### **Robotics**
![ROS](https://img.shields.io/badge/ros-%230A0FF9.svg?style=for-the-badge&logo=ros&logoColor=white)   
[![My Skills](https://skillicons.dev/icons?i=ros&theme=light)](https://skillicons.dev)

### **Programming Languages**
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)   
[![My Skills](https://skillicons.dev/icons?i=python&theme=light)](https://skillicons.dev)

### **AI & Computer Vision**
<div align=left>
  
  ![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
</div>

[![My Skills](https://skillicons.dev/icons?i=opencv&theme=light)](https://skillicons.dev) 

&nbsp;

## 5. 🤖 Hardware
### **Robot**
- Turtlebot3, OpenManipulator-X
### **Vision Camera**
- Webcam

&nbsp;

## 6. 🛠️ Node Architecture
<img src="https://github.com/user-attachments/assets/f5e56d89-cfc8-4112-b8d1-b437e9dd1226" width="75%" height="75%" title="px(픽셀) 크기 설정" alt="system_flow"></img>

&nbsp;
