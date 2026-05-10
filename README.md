<div align="center">

# 🦯 White Cane at Fire Evacuation
### 시각장애인을 위한 화재 대피 안내 시스템
*Evacuation Guidance System for the Visually Impaired*

<p>
  <img src="https://img.shields.io/badge/Status-Research_Prototype-success?style=flat-square" />
  <img src="https://img.shields.io/badge/Year-2022-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Award-한국정보처리학회_ACK_2022-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/First_Author-Hyerin_Choi-red?style=flat-square" />
</p>

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/Raspberry_Pi-A22846?style=for-the-badge&logo=raspberry-pi&logoColor=white" />
  <img src="https://img.shields.io/badge/Naver_Cloud-03C75A?style=for-the-badge&logo=naver&logoColor=white" />
</p>

</div>

---

## 🔥 Why this project

화재가 발생했을 때 시각장애인은 비상구 표시등이나 유도선을 인지하기 어렵습니다. 본 시스템은 흰 지팡이(white cane) 사용자를 위해 **건물 내 실시간 위치 추적 + 음성 안내 기반 대피 경로 제공**을 목표로 설계됐습니다.

> 일반인을 기준으로 만들어진 대피 인프라가 시각장애인에게는 작동하지 않는다는 문제의식에서 출발한 프로토타입입니다.

---

## 🧠 System Overview

```
┌─────────────────────┐    ┌──────────────────┐    ┌──────────────────────┐
│  Raspberry Pi  +    │    │  Django Backend  │    │  Naver Cloud TTS /   │
│  Sensors (smoke /   │ -> │  REST API        │ -> │  Map / Geofencing    │
│  IR / IMU / mic)    │    │  Real-time event │    │  음성 대피 안내       │
└─────────────────────┘    └──────────────────┘    └──────────────────────┘
        ▲                                                    │
        │                Voice guidance                      ▼
        └─────────────  to white-cane handle  ◀──────────────┘
```

- 라즈베리파이 + 센서 어레이가 흰 지팡이에 부착
- 화재 감지 시 백엔드로 이벤트 송출
- Naver Cloud API가 사용자 위치/상황에 맞는 음성 안내 생성
- 사용자에게 실시간으로 대피 방향을 음성으로 전달

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Hardware | Raspberry Pi / 화재 감지 센서 / IMU / 마이크 / 스피커 |
| Backend | Django (Python) |
| Cloud | Naver Cloud Platform — TTS / Maps |
| Communication | REST API (real-time event) |

---

## 🏆 Awards & Publication

본 프로젝트는 학술대회에 정식 발표된 연구 프로토타입입니다.

> **시각 장애인을 위한 화재 대피 시스템**
> *A development of Evacuation Guidance System for Blind Person*
>
> **최혜린(1저자)**, 고정주, 박예찬, 전상철
> 한국정보처리학회 학술대회논문집 **Vol.29 No.2, pp.1000–1002 (3 pages)**, 2022.11
> UCI: I410-ECN-0102-2023-500-000819813

---

## 👥 Authors

| Role | Name |
|---|---|
| **First Author / System Design** | **최혜린 (Hye-rin Choi)** |
| Co-author | 고정주 (Jeong-ju Go) |
| Co-author | 박예찬 (Ye-chan Bak) |
| Co-author | 전상철 (Sang-cheol Jeon) |

---

<div align="center">

*Built with the belief that emergency infrastructure should work for everyone.*

</div>
