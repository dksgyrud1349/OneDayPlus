# 🎨 원데이플러스 (OneDayPlus)
> **사용자 취향 분석 기반 원데이 클래스 큐레이션 및 통합 관리 플랫폼**

**원데이플러스**는 질문지를 통해 사용자의 성향을 분석하고 최적의 클래스를 추천하며, 예약부터 결제, 사후 관리까지 한 번에 해결할 수 있는 **Spring 기반의 웹 서비스**입니다.

---

## 🛠 Tech Stack

### **Development Environment**
![Spring Tool Suite](https://img.shields.io/badge/Spring_Tool_Suite-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Oracle 18c](https://img.shields.io/badge/Oracle_18c-F80000?style=for-the-badge&logo=oracle&logoColor=white)
![Apache Tomcat](https://img.shields.io/badge/Apache_Tomcat-F8DC75?style=for-the-badge&logo=apache-tomcat&logoColor=black)
![Maven](https://img.shields.io/badge/Apache_Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

### **Backend**
![Java](https://img.shields.io/badge/Java_8-007396?style=for-the-badge&logo=java&logoColor=white)
![Spring Framework](https://img.shields.io/badge/Spring_Framework-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=spring-security&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=for-the-badge&logo=mybatis&logoColor=white)
![JSP/Servlet](https://img.shields.io/badge/JSP%20%2F%20Servlet-007396?style=for-the-badge&logo=java&logoColor=white)

### **Frontend**
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![JSON](https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white)

### **Libraries & Tools**
![FullCalendar](https://img.shields.io/badge/FullCalendar-2C3E50?style=for-the-badge&logo=calendar&logoColor=white)
![Apache ECharts](https://img.shields.io/badge/Apache_ECharts-AA0000?style=for-the-badge&logo=apache-echarts&logoColor=white)
![Highcharts](https://img.shields.io/badge/Highcharts-8085E9?style=for-the-badge&logo=chart&logoColor=white)
![ERDCloud](https://img.shields.io/badge/ERDCloud-FF6B6B?style=for-the-badge)

---

## 🚀 담당 주요 기능 (My Role)

### 1. **사용자 (User) & 마이페이지**
* **클래스 탐색 및 예약**:
    * 원데이 클래스 목록 조회 및 **등록일/높은가격/낮은가격순 정렬** 기능 구현.
    * 관심 있는 클래스 **위시리스트** 등록 및 관리 기능 구현.
    * 예약 시 **최대 인원수 검증** 및 **소유 적립금** 한도 체크 로직 적용.
* **결제 및 환불**:
    * 사용자가 입력한 정보를 바탕으로 최종 가격 산정 후 **결제 API** 연동.
    * '대기' 상태 예약건에 대한 **은행/계좌 정보 입력 기반 환불 신청** 시스템 구축.
* **커뮤니케이션 및 혜택**:
    * 클래스별 **공지사항 확인** 및 개설 사업자 대상 **1:1 문의글 작성**.
    * 마이페이지 내 **적립금 내역(적립/사용/환불)** 조회 기능 구현.

### 2. **플러스 (Business Owner: 사업자)**
* **클래스 및 예약 운영**:
    * 원데이 클래스 **등록, 수정, 삭제** 및 개설 클래스 목록 확인 기능.
    * 클래스별 **누적 신고 건수** 실시간 모니터링 기능.
    * 예약 현황 확인 및 사용자 예약 상태를 **'대기'/'확정'**으로 변경 관리.
* **고객 응대**:
    * 사용자 문의글에 대한 **답변 작성/수정/삭제** 및 부적절한 게시글 삭제 기능.

### 3. **관리자 (Admin)**
* **클래스 거버넌스**:
    * 플랫폼 내 개설된 모든 원데이 클래스의 **승인 권한 관리**.
    * 클래스 상태를 **'대기', '승인', '보류', '취소'**로 동적 수정하여 노출 제어.

---

## 💡 핵심 구현 포인트
* **데이터 정교화**: **MyBatis 동적 쿼리**를 활용하여 승인 상태 및 정렬 조건에 따른 유연한 데이터 필터링 구현.
* **보안 및 권한**: **Spring Security**를 적용하여 사용자, 플러스, 관리자 간의 접근 권한을 엄격히 분리.
* **UX 최적화**: **Tiles 3**를 이용한 레이아웃 공통화 및 **Ajax/JSON** 통신을 통한 비동기 데이터 처리.

---

## 🏗 Database Architecture
* **Oracle 18c**를 기반으로 설계되었으며, **ERDCloud**를 통해 `사용자`, `클래스`, `예약`, `적립금`, `문의`, `환불` 테이블 간의 유기적 관계를 정의했습니다.
