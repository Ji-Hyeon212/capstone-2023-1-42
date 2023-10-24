# TayoTayo (타요타요)

<p align="center">
    <img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/81402944/d2883a35-12a9-4c99-a52b-563aa3009b9e" width="40%"/>
</p>

## 1. 프로젝트 소개

본 과제에서는 스마트 시티에서 시민들 간에 개인 모빌리티를 공유할 수 있는 **P2P 방식의 공유 모빌리티 서비스**를 개발하고자 한다.
<br>**DID를 통한 차량 검증**으로 개인이 차량의 정보를 관리하는 주체가 되도록 하고, **허가형 블록체인**으로 검증된 차량만 거래에 참여할 수 있으며
<br>내부에서만 모든 거래 정보가 투명하게 공개되는 안전한 거래 시스템을 설계한다.
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

### FrontEnd(React)

#### Dependency

| Dependency       | Version   |
|------------------|-----------|
| Next.js          | 13.4.7    |
| TypeScript       | 5.1.5     |
| Recoil           | 0.7.7     |
| axios            | 1.4.0     |
| tailwindCSS      | 3.3.2     |
| react-hook-form  | 7.45.2    |


## 4. 소개 및 시연 영상

#### 페이지 소개

|로그인|회원 가입|대시보드|차량 검색|
|---|---|---|---|
|<img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78369633/65022c49-2e49-4478-a1b2-3025fa641eb5" width=300>|<img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78369633/4a24043e-dfae-4d7c-b47d-3c03f72eb100" width=300>|<img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78369633/f8c60808-1206-441d-b004-9772580cbd73" width=300>|<img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78369633/73e4e30b-152e-4a15-bc34-503a1663cd9f" width=300>|
|차량 관리|차량 등록|채팅|마이페이지|
|<img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78369633/af6dea04-f012-4c24-aac6-d7d68a1b06c6" width=300>|<img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78369633/ef4fb659-17fd-499e-8657-f3c666fe127d" width=300>|<img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78369633/8f6dfd65-a8d6-4a2b-905d-d4474a9fe1ab" width=300>|<img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78369633/9d7332ee-38f8-44d1-9987-d555d5069712" width=300>|
---

[![부산대학교 정보컴퓨터공학부 소개](http://img.youtube.com/vi/zh_gQ_lmLqE/0.jpg)](https://youtu.be/zh_gQ_lmLqE)

<br>

---

## 5. 📌 디렉토리 구조 소개
```javascript
📦capstone-2023-1-42
 ┣ 📂Tayo-Backend               // 타요타요(차량 공유) 서비스 Server
 ┣ 📂VC_Service                 // 차량 VC 발급 서비스 Server
 ┣ 📂bin                        // Hyperledger Fabric's binaries
 ┣ 📂chaincode                  // Hyperledger Fabric's chaincode
 ┃ ┣ 📂tayocar                  // 차량 관리 체인코드
 ┃ ┣ 📂tayosharing              // 차량 공유 및 지갑 체인코드
 ┣ 📂config                     // Hyperledger Fabric's config
 ┣ 📂libindy                    // Hyperledger Indy's library
 ┗ 📂network                    // Hyperledger Fabric's network
```

## 6. 설치 및 사용법

본 프로젝트는 다음과 같은 단계에 따라 관련 패키지들의 설치와 빌드를 수행할 수 있습니다.

**1. 타요타요 프로젝트를 클론합니다.**
```
- git clone https://github.com/pnucse-capstone/capstone-2023-1-42.git
```

**2. 먼저 Indy Pool을 docker에 build하고 실행합니다.**
```
- Windows : docker build -f indy-pool.dockerfile -t indy_pool ../ci
- Mac OS : docker build --platform linux/amd64 -f indy-pool.dockerfile -t indy_pool ../ci
- docker run -itd -p 9701-9708:9701-9708 indy_pool
```

**3. 다음으로 tayonetwork.sh script 파일로 Fabric network를 실행합니다.**
```
- cd network
- ./tayonetwork.sh
```
<p align="center"><img src="https://github.com/pnucse-capstone/capstone-2023-1-42/assets/78337522/cdc14fe9-1326-4c06-8eb2-7115336aca66" width="500" height="300"/></p>
<p align="center"><sub>여기까지 완료되면 위 사진과 같이 docker desktop에서 container들을 확인할 수 있습니다.</sub></p>

**4. 환경 변수를 설정합니다.**
### Windows
```
- Path에 capstone-2023-1-42\libindy\lib 절대 경로 추가하기
- ex) - D:\capstone-2023-1-42\libindy\lib
```
### Mac OS
```
- 프로젝트 실행 전 dylb 환경변수를 설정합니다. (필수)
- LD_LIBRARY_PATH = D:\capstone-2023-1-42\libindy\lib
- DYLD_LIBRARY_PATH = D:\capstone-2023-1-42\libindy\lib
```
<p><sub>Mac OS(M1 chip)에서 libindy 라이브러리 인식이 되지 않아 서버 실행 시 `NullPointerException`이 발생하는 경우가 있습니다.<br>
라이브러리가 제대로 출력되는지 확인해보시고, 제대로 출력된다면 설치한 JDK를 확인해보세요. ARM 프로세서 기반인 M1 chip에서 JAVA가 Intel chip 프로세서로 동작하고 있을 수 있습니다.</sub></p>
<br>

**5. 프로젝트 내 Tayo-Backend 서버와 VC_Service 서버를 빌드 후 실행합니다.**
```
- cd Tayo-Backend
- ./gradlew build
- java -jar ./build/libs/Tayo-BE-0.0.1-SNAPSHOT.jar

- cd VC_Service
- ./gradlew build
- java -jar ./build/libs/VC_Service-0.0.1-SNAPSHOT.jar
```

**6. React로 웹 클라이언트를 실행합니다.**
```
- cd Tayo-FE
- npm install
- npm run dev
```
<p><sub>프로젝트 실행 후 http://localhost:3000 으로 접속합니다.</sub></p>
