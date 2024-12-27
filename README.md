# Summary-Note
개인 공부 및 프로젝트 정리

## 🖥️ 프로젝트 소개
기존 솔루션에서는 Front-end와 Back-end가 하나의 프로젝트에 통합되어 있었으나, 솔루션 업그레이드를 통해 구조를 개선하였습니다. 업그레이드 과정에서 Front-end는 Vue.js로, Back-end는 Spring Boot로 분리하여 각각 독립적인 프로젝트로 구성하였으며, 이를 통해 유지보수성과 확장성을 크게 향상시켰습니다.

## 아키텍처

com.andwise.tm7

   ├── massmail 
   
   
   │     ├── control   # API 컨트롤러 (요청을 받고 서비스 계층 호출)
   
   
   │     ├── service   # 비즈니스 로직 및 데이터 처리
   
   
   │   ├── dto       # 데이터 전송 객체 (계층 간 데이터 전달)
   
   
   │   └── mapper    # MyBatis 매퍼 인터페이스
   
   │ 
   
    └── common
    ├── control   # API 컨트롤러 (요청을 받고 서비스 계층 호출)
    
    
    ├── service   # 비즈니스 로직 및 데이터 처리
    
    
    ├── dto       # 데이터 전송 객체 (계층 간 데이터 전달)
    
    
    ├── mapper    # MyBatis 매퍼 인터페이스
    
    
    ├── properties  # 어플리케이션 설정 파일 관련 클래스
    
    
    ├── utils     # 보안 관련 클래스
    
    
    └── security  # 공통 유틸리티 클래스

massmail 같이 다른 패키지들은 공통으로 사용되고 있습니다.

## ⏱️ 개발 시간
2024-11-28 ~ 

## 🧑🏻‍💻 개발 환경
- java 17
- framework 3.3.6
- mybatis 3.0.3
- lombok 1.18.30
- spring security
- DB : MariaDB , Oracle
- Gradle을 이용하여 라이브러리 다운
- Vue.js 2.x
- BootStrap

## 주요 변경
- Back-End
1. Spring Framework 3.2.8 버전을 기반으로 개발되었으나, 최신 기술 도입과 생산성 향상을 위해 Spring Boot 3.3.6으로 업그레이드를 진행하였습니다. 이 과정에서 기존 프로젝트 구조를 Spring Boot에 맞게 재설계하고, 의존성 관리, 설정 파일, 빌드 도구 등을 최신화하여 프로젝트의 효율성과 유지보수성을 크게 개선하였습니다.
2. 기존 프로젝트는 Java 7 기반으로 개발되었으며, 현재 Java 17로 업그레이드되었습니다. 이를 활용해 람다식과 같은 최신 기능을 도입하여 코드를 개선했습니다.

- Front-End
1. jQuery를 활용하여 화면을 설계하였으나, 최신 기술 스택 도입과 효율적인 UI/UX 관리를 위해 Vue.js로 전환하였습니다. 이 과정에서 컴포넌트 기반 설계로 코드 재사용성을 높이고, 데이터 바인딩 및 상태 관리를 통해 개발 생산성과 유지보수성을 향상시켰습니다.


## 담당 부분
- 현재 솔루션에서 사용 중인 Spring Framework 버전이 매우 오래되어 팀 회의를 통해 버전 업그레이드를 제안드렸습니다. 이후 제가 관리자로 선정되어, 프로젝트 구조 설계 및 설정값 등 기초 작업을 직접 진행하였습니다.
- 기존에 jQuery를 활용하여 구현된 CRUD 화면을 Vue.js로 전환하여 컴포넌트 기반 구조로 재구성하였습니다. 또한, Chart.js를 활용해 차트 기능을 개발하였으며, 이를 공통 코드로 모듈화하여 다양한 화면에서 재사용 가능하도록 설계하였습니다. 이러한 개선을 통해 코드의 가독성과 유지보수성을 높이고, 차트 기능의 확장성을 강화하였습니다. 
