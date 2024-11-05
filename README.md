# My Select Shop

## 과제 목표

> Spring MVC와 네이버 Open API를 통해 My Select Shop을 제작한다.
과제를 통해 Spring MVC를 이해하고, API를 구현할 수 있다.
>

## About My Select Shop

- 네이버 쇼핑 API를 통한 상품 검색
- 관심 상품 등록
- 관심 상품 폴더 별 분류
- 관심 상품 희망 최저가 업데이트

## My Selct Shop API

| 기능 | Method | URL |
| --- | --- | --- |
| 관심 상품 등록하기 | POST | /api/products |
| 관심 상품의 희망 최저가 업데이트 | PUT | /api/products/{id} |
| 관심 상품 조회하기 | GET | /api/products |
| 로그인 페이지 호출 | GET | /api/user/login-page |
| 회원가입 페이지 호출 | GET | /api/user/signup |
| 회원가입 | POST | /api/user/signup |
| 회원 정보 요청 | GET | /api/user-info |
| 회원의 폴더 생성 | POST | /api/folders |
| 회원의 폴더 조회 | GET | /api/user-folder |
| 폴더 전체 조회 | GET | /api/folders |
| 폴더 추가 | POST | /api/products/{productId}/folder |
| 폴더별 상품 조회 | GET | /api/folders/{folderId}/products |

## 실행방법

```
spring.datasource.url=${DB_URL}
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update

spring.jpa.properties.hibernate.show_sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.properties.hibernate.use_sql_comments=true

jwt.secret.key=${JWT_KEY}

naver.id=${NAVER_ID}
naver.key=${NAVER_KEY}
```

- MySQL의 url, username, password를 각 환경변수에 기입
- JWT KEY 값 설정
- NAVER 개발자 Open API에 웹 애플리케이션 등록 후 발급받은 ID와 KEY값 기입
- 실행

## 개발 환경

- JAVA 17
- Spring Boot 3.1.0
- gradle build

## 기술 스택

- Front
    - thymeleaf
- Back
    - Spring Boot
    - JPA
- Deploy
    - AWS EC2
    - AWS RDS