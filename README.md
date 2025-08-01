# 🛴 Smart Scooter Safety System

📄 프로젝트 상세 문서: [https://lopsided-tray-d39.notion.site/20e04872d73a808ea356ea7a39253cc3](https://lopsided-tray-d39.notion.site/20e04872d73a808ea356ea7a39253cc3)

> **“실시간 센서 감지 + 제어 로직으로 공유 킥보드 사고를 줄이는 스마트 안전 시스템”**

---

## 📌 프로젝트 개요

- **헬멧 미착용, 2인 이상 탑승, 후방 차량 접근**을 실시간 감지하여  
  ➤ **속도 제한 / 시동 차단 / 경고 출력**을 수행하는 스마트 안전 시스템  
- **Arduino + Load Cell + TFmini LiDAR + Bluetooth + App Inventor** 기반 통합 구현  
- **PWM 제어 / UART 센싱 / 실시간 앱 시각화 / 부저 경고 시스템** 탑재

---

## ⚙️ 시스템 구성

| 구성 요소       | 설명                                                                 |
|----------------|----------------------------------------------------------------------|
| **MCU**        | Arduino UNO                                                          |
| **센서**       | 압력 센서(RA30P), Load Cell ×4 + HX711 ×2, TFmini LiDAR              |
| **통신**       | HC-05 블루투스 모듈, UART (SoftwareSerial)                          |
| **모터**       | DC 모터 (PWM 제어, 방향 제어)                                        |
| **앱**         | App Inventor 기반 모바일 앱 (실시간 센서 상태 시각화)                |
| **전원**       | 14.8V 리튬 배터리 (10,000mAh) → 고전력 모듈 대응                    |

---

## 💡 주요 기능

- ✅ **헬멧 미착용 시 시동 차단**
- ✅ **2인 이상 탑승 시 속도 25% 제한**
- ✅ **주행 중 헬멧 탈착 시 모터 제어 + 경고음 출력**
- ✅ **후방 차량이 3m 이내 접근 시 경고음 발생**
- ✅ **모바일 앱에서 실시간으로 상태 및 위험 상황 확인 가능**

---

## 🔧 핵심 기술 스택

- **MCU 제어**: C (Arduino IDE)
- **센서 통신**: UART (SoftwareSerial)
- **무게 인식**: HX711 기반 Load Cell 측정 및 보정
- **거리 측정**: TFmini LiDAR 거리센서
- **앱 개발**: App Inventor (Bluetooth 통신 + 실시간 UI 처리)
- **하드웨어 구성**: 아크릴 재단 회로박스 + 모듈 집적 배선 구성

---

## 🧠 문제 해결 및 고찰

- 🔸 **3D 프린터 출력 한계** → 아크릴 직접 재단 방식으로 대체  
- 🔸 **센서값 튐 현상** → 전선 교체 및 정밀 배선으로 안정화  
- 🔸 **모터 동작 불량** → 알카라인 전지 대신 리튬 배터리로 전원 안정성 확보  
- 🔸 **2인 탑승 기준 설정 어려움** → 100kg 기준으로 단순하고 현실적인 구현
