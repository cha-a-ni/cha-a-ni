# 안녕하세요, cha-a-ni입니다 👋

로봇의 센서 데이터를 지도 위에 표시하고, 지도 위의 시설물 데이터를 경로 탐색에 활용하는 프로젝트를 만들고 있습니다.

## 주요 프로젝트

### Scout2Map · 로봇 관제

로봇이 수집한 지도, 위치, 센서 상태를 웹에서 실시간으로 확인하고 위험 이벤트를 지도 위에서 파악할 수 있는 시스템입니다.

| 저장소 | 기능 | 기술 |
| --- | --- | --- |
| [S2M-Web-Monitoring](https://github.com/cha-a-ni/S2M-Web-Monitoring) | 지도·로봇 위치·주행 상태를 실시간으로 표시하는 관제 화면 | React · WebSocket |
| [S2M-Event-Engine](https://github.com/cha-a-ni/S2M-Event-Engine) | 센서와 주행 상태를 받아 임계값과 심각도를 판정하고 이벤트를 발행 | ROS 2 |

### [Safe Root Finder](https://github.com/cha-a-ni/safe-root-finder) · 보행 경로 탐색

가로등과 CCTV 위치를 도로 그래프의 가중치에 반영해 보행 경로를 계산하는 프로젝트입니다. Python과 NetworkX로 그래프를 구성하고, Kakao Local API로 주소를 좌표로 변환합니다.
