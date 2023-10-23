# 타요타요

<p align="center">
    <img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/81402944/d2883a35-12a9-4c99-a52b-563aa3009b9e" width="40%"/>
</p>

## 1. 프로젝트 소개

본 과제에서는 스마트 시티에서 시민들 간에 개인 모빌리티를 공유할 수 있는 P2P
방식의 공유 모빌리티 서비스를 개발하고자 한다. DID 를 통한 차량 검증으로 개인이
차량의 정보를 관리하는 주체가 되도록 하고, 허가형 블록체인으로 검증된 차량만 거래에
참여할 수 있으며 내부에서만 모든 거래 정보가 투명하게 공개되는 안전한 거래
시스템을 설계한다.
<br>

---

## 2. 팀소개

<div align="center">

2023 전기 부산대학교 정보컴퓨터공학부 졸업과제 팀 **타요타요**
|  **팀원**  | **역할 소개**  |
| :------: |  ------ |
| [<img src="https://github.com/kimdonwoo.png" height=150 width=150>](https://github.com/kimdonwoo) <br> **[김돈우](https://github.com/kimdonwoo)** | - 블록체인 네트워크 구축 및 기능 개발 (Hyperledger Indy)   <br> - Backend 서버 개발 (Spring Boot)|
| [<img src="https://github.com/xet-a.png" height=150 width=150> ](https://github.com/xet-a) <br> **[최세희](https://github.com/xet-a)** | - UI 디자인 및 서비스 기획 <br> - 블록체인 네트워크 구축(Hyperledger Fabric) <br> - 블록체인 체인코드 개발|
| [<img src="https://github.com/Ji-Hyeon212.png" height=150 width=150>](https://github.com/Ji-Hyeon212) <br> **[이지현](https://github.com/Ji-Hyeon212)** |  - UI 디자인 및 서비스 기획 <br> - 클라이언트 UI 설계 및 기능 개발(React.js) |

</div>



<br>

---

## 3. 시스템 구성도

![전체 시스템 구성도](https://github.com/pnucse-capstone/capstone-2023-1-42/assets/81402944/45a47b53-ccb9-4764-a193-90e3e6550774)

<br>

---

## 4. 소개 및 시연 영상

[![부산대학교 정보컴퓨터공학부 소개](http://img.youtube.com/vi/zh_gQ_lmLqE/0.jpg)](https://youtu.be/zh_gQ_lmLqE)

<br>

---

## 5. 설치 및 사용법

본 프로젝트는 다음과 같은 단계에 따라 관련 패키지들의 설치와 빌드를 수행할 수 있습니다.

1. 먼저 타요타요 프로젝트를 클론합니다.
```
- git clone https://github.com/pnucse-capstone/capstone-2023-1-42.git
```

2. Indy Pool 먼저 docker에 build하고 실행합니다.
```
- Windows : docker build -f indy-pool.dockerfile -t indy_pool ../ci
- Mac OS : docker build --platform linux/amd64 -f indy-pool.dockerfile -t indy_pool ../ci
- docker run -itd -p 9701-9708:9701-9708 indy_pool
```

3. tayonetwork.sh 스크립트 파일로 Fabric 네트워크 실행시키기
```
- cd network
- ./tayonetwork.sh
```

4. 환경 변수 추가해주기
```
- Path에 capstone-2023-1-42\libindy\lib 절대 경로 추가하기
- ex) - D:\capstone-2023-1-42\libindy\lib
```

5. 프로젝트 내에 Tayo-Backend 서버랑 VC_Service 서버 빌드 후 실행 시키기
```
- cd Tayo-Backend
- ./gradlew build
- java -jar ./build/libs/Tayo-BE-0.0.1-SNAPSHOT.jar

- cd VC_Service
- ./gradlew build
- java -jar ./build/libs/VC_Service-0.0.1-SNAPSHOT.jar
```

6. React 서버 실행시키기