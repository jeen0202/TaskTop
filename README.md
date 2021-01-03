# Project TaskTop(2020/10/30~2020/11/07)
스마트그리드 기반 IoT융합 SW전문가 과정 핵심융합프로젝트
## 1.**프로젝트 배경 및 주제**

**1) 프로젝트 배경**

COVID-19의 영향으로 원격, 재택근무가 증가함에 따라 사무 업무시 공동 휴게공간을 이용하기 어려운 사용자를 타겟으로 웹 서비스에 IoT기술을 융합하여 업무환경을 개선시키기 위한 제품

**2) 목표 서비스 및 기능**

1. 사용자의 얼굴을 인식하여 자동으로 부재유무를 서버에 갱신 (아두이노 + 웹서비스)
2. 관리자 및 사원의 사원 정보 및 부재유무 파악 (웹 서비스)
3. 사용자가 자리에서 커피머신, 컴퓨터 전원제어 기능(웹 + 아두이노)
4. 사용자의 동작을 인식하여 자동으로 안마기 작동( 아두이노)
5. 사용자의 근무시간을 체크하여 매시간마다 스트레칭 제안
6. 사용자의 복지기능 사용 빈도를 count, 분석하여 최적의 근무환경 제공(미완성)

## 2. **시스템 구성**

![TaskTop_시스템](https://user-images.githubusercontent.com/71309053/103478308-1b064500-4e09-11eb-964d-a7356f53c0e0.PNG)

## 3. **프로젝트 개요**

### 1. **도식도**

![TaskTop_도식도](https://user-images.githubusercontent.com/71309053/103478310-1c377200-4e09-11eb-9a46-5b1862501b13.PNG)

### 2. **동작 개요**

- **Arduino** : 3개의 디바이스로 나뉘어 각각 커피머신제어, 안마기제어, 객체인식 기능을 수행한다.

    1) 객체 인식 : 카메라모듈(Huskylens)를 통해 등록된 사원의 안면인식을 통한 부재유무 업데이트

    2) 커피 머신 제어 : server와의 통신을 통해 사용자의 요청이 있을경우 서보모터를통해 커미머신 작동

    3) 안마기 제어 : 사용자의 좌석에 부착된 자이로 센서를 통해 동작을 감지하여 서보모터에 연결되어있는 안마기 작동, server에 데이터 반영(미완성)

- **Web Service** : Login을 통해 관리자와 사원의 기능으로 구분된다.
 1. 관리자  
  
          1. 사원에 대한 CRUD 기능
          2. 사원목록 조회 기능
          3. 메시지 전송 기능
      
 2. 사원  
 
          1. 동일부서 조회 기능
          2. 메시지 확인 기능
      
 3. 공통기능  
 
          1. 사원부재유무 확인 기능
          2. 연동되어있는 디바이스를 통한 자동제어 및 통계 제공기능
          3. 시간을 기반으로한 스트레칭 제안 기능
          4. 웹을통한 컴퓨터의 전원 제어 기능

## 4. 웹 **화면구성**

 주요기능에 따라 관리자, 사원으로 나뉘어집니다.

1. **관리자 페이지**
    1. 사원 CRUD 페이지
    2. 메시지 전송을 위한 페이지
2. **사용자 페이지**
    1. 동일 부서 사원 조회 페이지
3. **공용 페이지**
    1. 로그인 페이지
    2. 메인 페이지
    3. 스트레칭 페이지

## 5. **디바이스 구성(추후 업데이트)**

## 6. DB 구성

### E-R Diagram

![TaskTop_ER](https://user-images.githubusercontent.com/71309053/103477942-c366da00-4e06-11eb-99e4-472a930ad05e.png)

## 7. **프로젝트 결과**

1. **시연 영상**

<a href="https://youtu.be/RBZsV7t_b1s" height="5" width="10" target="_blank">
    <img width="600" src="http://i.ytimg.com/vi/RBZsV7t_b1s/0.jpg">
<a>

2. **프로젝트 사진** 
    - 공통
    
  ![TaskTop_main](https://user-images.githubusercontent.com/71309053/103477962-ef825b00-4e06-11eb-96ad-3ff013953a8c.PNG)
  ![TaskTop_Login](https://user-images.githubusercontent.com/71309053/103477964-f27d4b80-4e06-11eb-8a9b-7f77dd71b5aa.PNG)

    - 관리자
    
  ![TaskTop_adminMenu](https://user-images.githubusercontent.com/71309053/103478145-f198e980-4e07-11eb-8a9c-f8a2ddb4c78c.PNG)
  ![TaskTop_AdminMes](https://user-images.githubusercontent.com/71309053/103478018-5f90e100-4e07-11eb-8764-1534f0246f7f.PNG)
    
    - 사원
  ![TaskTop_MemberMain2](https://user-images.githubusercontent.com/71309053/103477992-2c4e5200-4e07-11eb-8347-60a7b5baeab7.PNG)
  ![TaskTop_MemberMain3](https://user-images.githubusercontent.com/71309053/103478030-69b2df80-4e07-11eb-9854-a17b03e63b63.PNG)
  
3. **팀 구성** 

  ![TaskTop_팀 소개](https://user-images.githubusercontent.com/71309053/103478582-07f47480-4e0b-11eb-959f-6a43f9e102da.PNG)
