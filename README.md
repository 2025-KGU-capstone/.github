# 📦 AI 스마트 안심 택배 플랫폼

> "비인가 접근 NO! 안심하고 택배 받자."  
> AI와 IoT 기술을 활용한 실시간 택배 감시·인증 시스템

---

## 🖼️ 발표 포스터

![3팀 심캡 포스터](https://github.com/user-attachments/assets/17f68b4c-31cd-4ccb-a71b-849435f07611)

> 📌 **요약**: 택배 도난과 분실을 방지하기 위한 AI 기반 실시간 감시 시스템.  
> YOLOv5와 얼굴 인식 알고리즘을 이용해 비인가 접근을 감지하고, OLED 디스플레이 및 사이렌을 통해 즉각 대응합니다.

---

## 🎥 시연 영상


### 앱으로 제어
https://github.com/user-attachments/assets/fadac3fc-713f-41e6-bc99-5b3e2fdca6ac

### 본인이 가져갈때
https://github.com/user-attachments/assets/3996eb9e-1f37-41e6-a228-5167e6dc5fd0

### 범인이 가져갈때
https://github.com/user-attachments/assets/3de6e85f-30f1-4c96-9af9-1f7c79849222


---

## 🧠 핵심 기능

| 기능            | 설명 |
|-----------------|------|
| 📦 택배 감지     | YOLOv5로 택배 상자 인식 |
| 👤 얼굴 인증     | 등록된 사용자와의 얼굴 매칭 (face_recognition) |
| 📡 실시간 스트리밍 | Flask + OpenCV 기반 영상 전송 |
| 🔔 경고 및 알림  | 비인가 접근 시 사이렌 작동 + Firebase 알림 발송 |
| 🖥 OLED UI       | 현재 시스템 상태 표시 및 방문자 로그 |

![image](https://github.com/user-attachments/assets/cce646de-29d1-4c9a-9caf-ed19ee32843d)

---

## 🏗 시스템 구성도

안전모드 ON
↓
PIR 센서 감지
↓
📷 Camera 1 (Stream)
📷 Camera 2 (Capture & Detect)
↓
YOLOv5 + FaceRecognition
↓
Flask Backend → AI 판단 → Firebase 알림 + 사이렌 제어
↓
모바일 앱/웹 실시간 확인 + 로그 저장

---

## 📁 프로젝트 구조

```
Server/
├── app/
│ ├── app.py
│ ├── yolo_detector.py
│ ├── face_man.py
│ ├── push_notification.py
├── captured_images/
├── assets/
│ └── poster.png
├── requirements.txt
├── README.md
└── .env
```

## 👥 팀 구성원

| 이름     | 역할                | 담당 내용                                         |
|----------|---------------------|--------------------------------------------------|
| 박준형[팀장]   | 하드웨어 / Server  | Raspberry Pi GPIO 제어, OLED, 사이렌 연동            |
| 홍원택   | AI       | YOLOv5, 얼굴 인식 모델 연동 및 최적화                |
| 김서영     | Client 개발           |   Flutter 앱개발, 디자인       |
| 홍성조    |    Server      |     Flask 서버, API 라우팅, 영상 스트리밍 구현       |
| 추유진     | Client 개발       | Flutter 앱개발       |
| 서태영     | 논문 작성       | 국내 논문 작성       |



