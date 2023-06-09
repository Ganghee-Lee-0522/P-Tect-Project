# 👮 P-Tect-Project 🚔
편의점 근로자 종합 보안 시스템 서비스

</br></br>

## 🚨 Project Code
|Service|Link|Programmer|
|:--:|:--:|:--:|
|DL-Server|[Link](https://github.com/JYKim1124/P-Tect_DL/tree/main)|[김주연](https://github.com/JYKim1124)|
|Web-Server|[Link](https://github.com/Ganghee-Lee-0522/P-Tect_Backend)|[이강희](https://github.com/Ganghee-Lee-0522)|
|Android|[Link](https://github.com/z00m-1n/ptect_final)|[이주미](https://github.com/z00m-1n)|

</br></br></br></br>

## 🚨 About 편텍트
![image](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/7c205481-f27a-4cb7-8c72-998235486184)
모든 근무자가 안심하고 일할 수 있는 편의점을 만드는 든든한 Co-Worker가 되고자 합니다. 편텍트는 세 가지 서비스로 편의점 안전망을 구축합니다.
</br>
### 1) 무슨 일이 일어나도 당신을 도와줄 편텍트가 있습니다.
![image](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/d8ed646d-8042-4857-bf01-724bea297403)
편의점 CCTV에서 이상 행동이 감지되면, 편텍트는 근무자 대신 112에 문자 신고를 접수합니다. 어노멀리 디텍션 기술로 구현된 이 자동신고 서비스는 위험 상황에서 혼자 신고하기 어려운 근무자 대신 신고 상황을 캐치하고 문자를 구성하여 빠르게 신고합니다.

https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/20b6e3ee-5f4d-4ec7-84e3-5eafeb8ee59b

범죄 상황에 처한 근무자 A씨를 담은 편의점 CCTV 영상입니다. 편텍트는 영상 속에서 일정 임계치를 넘는 비정상 score를 감지합니다. 이 상황을 위험 상황으로 판단한 편텍트가 근무자에게 어플리케이션 push 알람 으로 강력범죄가 발생했음을 알리고 신고의사를 묻습니다.

https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/43cffa00-3c01-4649-8218-42f3602a2b0c

근무자가 알림을 확인하고 신고를 확정하거나, 일정 시간 알림에 대한 응답이 없는 경우, 편텍트는 근무자 A씨가 근무 중인 편의점의 주소와 시각을 담은 신고 문자를 작성하고 112에 신고를 접수합니다.

</br></br>

### 2) 부담스러운 신고 절차를 도와줄 편텍트가 있습니다.
![image](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/f487a2f8-bdad-4ef4-9456-3d19bd4c122e)
편의점 근무 시에는 강력 범죄 상황은 아니지만, 경찰의 도움이 필요한 경우가 발생합니다. 언어 폭력이나 주취자의 난동은 이러한 상황의 예시가 될 수 있습니다. 수동 신고 서비스는 근무자가 신고를 원하는 상황에서 간편하고 빠른 신고를 지원합니다. 편텍트의 버튼을 누르기만하면 발생 시각과 상세 주소가 포함된 신고 문자가 구성되고, 경찰에 신고를 접수합니다. 전화나 문자를 보내는 데 소비되는 시간을 절약하여 빠르게 경찰이 현장에 개입할 수 있게 됩니다.

https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/88addb9b-88d8-435b-92e7-3cae92de1c3e

고객과의 대치 상황에 처한 근무자 A씨가 경찰을 부르고자 합니다. A씨가 편텍트의 버튼을 누르자, A씨가 근무하는 편의점 주소와 현재 시각이 담긴 신고 문자가 구성되어 112에 접수됩니다.

</br></br>

### 3) 든든한 Co-Worker 편텍트가 있습니다.
![image](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/7f408a7b-ce06-44a2-a4a6-6e937af68787)
강력 범죄 발생 시, 편텍트는 편의점 내 스피커와 외부 전광판으로 도움을 요청합니다.편텍트가 편의점 내 스피커를 활용해 범죄가 감지되었고 신고가 접수되었다는 음성 경고 메시지를 내보냄으로써, 범죄 행위자가 행위를 멈추게 할 수 있습니다. 편텍트가 편의점 외부 전광판에 SOS 메시지를 노출함으로써 편의점을 지나는 행인들이 위험 상황을 인지하고 도움을 줄 수 있게 됩니다.

</br></br></br></br>

## 🚨 Project Architecture
![image](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/e85efddc-d928-496f-bc05-cf6aaec15312)

### 자동신고 로직
CCTV 영상에서 anomaly detection으로 딥러닝 서버가 강력범죄를 탐지하게 되면, 스피커를 통한 SOS 음성 메시지가 출력되고 외부 전광판으로 SOS 메시지가 노출됩니다. 이와 동시에, 신고에 대한 정보와 이미지가 웹 서버로 전달이 되어 신고가 접수되고, 사용자는 앱 PUSH 알람으로 강력범죄가 일어났음을 확인하게 됩니다.

### 수동신고 로직
사용자로부터 호출을 받아 웹 서버와 딥러닝 서버에 이를 전달하고, 현장 알림까지 진행됩니다.

</br></br></br></br>

## 🚨 기대효과
![qr포함 사본-002](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/a0ad72cf-1d56-4ed8-9f22-37c80593aecc)

</br></br></br></br>

## 🚨 Team 우리는삼총사
| DL-Server | Web-Server | Android |
|:---:|:---:|:---:|
|![image](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/e04b136c-5887-4fa9-a89c-39f35facd506)|![image](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/cafa86c4-e56a-43bc-8f4d-c1bd9ddb6c20)|![image](https://github.com/Ganghee-Lee-0522/P-Tect-Project/assets/79368467/dda2466a-99e0-4889-866c-70be5b5e1640)|
| [김주연](https://github.com/JYKim1124) | [이강희](https://github.com/Ganghee-Lee-0522) | [이주미](https://github.com/z00m-1n) |
