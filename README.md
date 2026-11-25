# cha-a-ni

**로봇 관제와 지도 기반 경로 탐색 프로젝트를 개발합니다.**  
센서 값에서 관제 화면에 표시할 이벤트를 골라내고, 시설물 데이터를 경로 탐색에 쓸 수 있는 가중치로 바꾸는 작업을 해왔습니다.

## 프로젝트

### Scout2Map · 실시간 로봇 관제

**센서가 감지한 이상을 로봇의 위치와 함께 볼 수 있을까?**

ROS 2 이벤트 엔진에서 센서 값과 주행 상태를 받아 임계값·지속 시간·심각도를 판정합니다. React 관제 화면에서는 WebSocket으로 받은 지도와 로봇 위치 위에 이벤트를 표시해, 운용자가 어떤 일이 어디서 일어났는지 확인할 수 있습니다.

[웹 관제 화면](https://github.com/cha-a-ni/S2M-Web-Monitoring) · [ROS 2 이벤트 엔진](https://github.com/cha-a-ni/S2M-Event-Engine)

### Safe Root Finder · 보행 경로 탐색

**도로 길이에 가로등과 CCTV 위치를 더하면 경로 선택이 어떻게 바뀔까?**

교차로와 도로 구간을 NetworkX 그래프로 만들고, 가로등·CCTV 데이터를 도로 구간의 가중치에 반영해 경로를 계산합니다. Kakao Local API는 주소를 좌표로 바꾸는 데 사용합니다.

[경로 탐색 코드](https://github.com/cha-a-ni/safe-root-finder)
