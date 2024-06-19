# 박준우 프로젝트

- - -

## 목차

### 1차 프로젝트

- [쇼핑몰 & 관리자 모드 기반 Chatbot 구현](#쇼핑몰--관리자-모드-기반-Chatbot-구현)

### 2차 프로젝트

- [그룹웨어 기본 연동 기능 및 메시지 봇 구현](#그룹웨어-기본-연동-기능-및-메시지-봇-구현)

### 3차 프로젝트

- [시나리오형 챗봇 웹 개발](#시나리오형-챗봇-웹-개발)

- - -

### 쇼핑몰 & 관리자 모드 기반 Chatbot 구현

#### **● 프로젝트 명** : E 1 I 4

#### **● 프로젝트 설명** : One Day Class 강의 쇼핑몰 사이트

#### **● 프로젝트 파일명** : Project1TeamE1I4, ProjectCICD

#### **● 역할** : 팀장

- **Preview**<br>
    - 회원가입
      <br>
      <img src="https://github.com/qkrwnsdn981204/ParkJunwooProjects/assets/154858222/ec914912-02ef-46b5-a95a-34717fda28c0" width="100%" height="auto"/>
      <br>
      <br>
    - 일반 회원 로그인
      <br>
      <img src="https://github.com/qkrwnsdn981204/ParkJunwooProjects/assets/154858222/ede553f8-313a-436a-91f3-0a7092aaa178" width="100%" height="auto"/>
      <br>
      <br>
    - Oauth2 로그인
      <br>
      <img src="https://github.com/qkrwnsdn981204/ParkJunwooProjects/assets/154858222/9775dc1f-affa-4a8e-9e86-fb94ac071a78" width="100%" height="auto"/>
      <br>
      <br>
    - 수정, 삭제
      <br>
      <img src="https://github.com/qkrwnsdn981204/ParkJunwooProjects/assets/154858222/12eb2306-88d7-4a64-9136-d9ee0420a78f" width="100%" height="auto"/>

<details>

<summary> 기술 스택 </summary>

| 카테고리     | 요소                                                                                                                  |
|----------|---------------------------------------------------------------------------------------------------------------------|
| 프로그래밍 언어 | JAVA                                                                                                                |
| 개발 툴     | IntelliJ                                                                                                            |
| 프레임워크    | Spring Boot 2.7.11                                                                                                  |
| 라이브러리 DI | Spring WEB(MVC), Thymeleaf, Spring Data JPA, Lombok, SpringSecurity5 <br/>, websocket, validation, OAuth2, security |
| 데이터베이스   | MySql8                                                                                                              |
| ORM      | Spring Data JPA (JAVA(SQL))                                                                                         |
| 템플릿 엔진   | Thymeleaf (HTML + Data)                                                                                             |
| FRONT    | css, javaScript, html, ajax                                                                                         |
| 설정       | application.yml, application-oauth2.yml                                                                             |

</details>

<details>

<summary> 프로젝트 일정 </summary>

![img.png](images/Project1/project1plan.png)

</details>

<details>

<summary> ER 다이어그램 </summary>

![img.png](images/Project1/project1ERD.png)

</details>

<details>

<summary> 기능 구현 </summary>

- DB 설계

  | **No** | **주요 Entity** | **상세 Entity**                                           |
      |--------|---------------|---------------------------------------------------------|
  | 1      | member        | member, memberFile                                      |
  | 2      | shop          | shop, cart, cartShopList, shopFile, shopReply, shopLike |
  | 3      | board         | board, boardReply, boardFile                            |


- 회원 CRUD

  | **No** | **기능**  | **설명**                                                                     |
     |--------|---------|----------------------------------------------------------------------------|
  | 1      | 회원가입    | 강사와 수강생으로 나누어 회원가입 <br> 비밀번호 확인 기능 <br> 전화번호 자동 하이픈(-) <br> 프로필 사진 추가 <br> |
  | 2      | 회원정보 조회 | 회원 개인 정보 조회 <br/> 간이 장바구니 기능                                               |
  | 3      | 회원수정    | 프로필사진, 개인정보, 비밀번호 수정                                                       |
  | 4      | 회원삭제    | 회원 탈퇴 기능                                                                   |


- 로그인

  | **No** | **기능**     | **설명**                                                                |
         |--------|------------|-----------------------------------------------------------------------|
  | 1      | 일반 회원 로그인  | Security를 통해 회원가입한 아이디로  로그인                                          |
  | 2      | Oauth2 로그인 | Oauth2를 이용하여 google, kakao, naver 아이디로 로그인<br/> 로그인시 아이디가 없으면 자동 회원가입 |

- CI/CD

  | **No** | **설명**                            |
         |--------|-----------------------------------|
  | 1      | 배포할 파일 github push                |
  | 2      | git actions 실행                    |
  | 3      | 빌드한 프로젝트 압축                       |
  | 4      | 압축된 파일 S3 복사                      |
  | 5      | S3에 있는 파일을 CodeDeploy 를 통해 EC2 배포 |
  | 6      | EC2에서 jar 파일 실행                   |

</details>

<details>

<summary>팀원 역할</summary>

   > 박준우 (팀장) : DB설계, 회원 CRUD, Oauth2, Security, CI/CD

   > 손** (팀원) : 관리자페이지, Chatbot, 강사소개 페이지, 메뉴바, INDEX 애니메이션 기능

   > 심** (팀원) : 게시판 CRUD, Naver API

   > 이** (팀원) : 상품 CRUD, Cart 담당

   > 조** (팀원) : INDEX 페이지, 1:1 문의내역, Naver API

</details>


**[⬆ 위로 가기](#목차)**

### 그룹웨어 기본 연동 기능 및 메시지 봇 구현

**[⬆ 위로 가기](#목차)**

### 시나리오형 챗봇 웹 개발

**[⬆ 위로 가기](#목차)**

