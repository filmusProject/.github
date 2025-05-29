# 🎬 Filmus

AI 기반 영화 검색 및 추천 플랫폼 **Filmus**는 사용자의 취향과 줄거리 키워드를 분석해  
[영화 검색](https://filmus.o-r.kr/search) 및 [줄거리 기반 추천](https://filmus.o-r.kr/plot-search)을 제공하는 웹 서비스입니다.  
검색 기능, 줄거리 기반 추천, 찜/리뷰 작성까지 통합된 사용자 경험을 제공합니다.

> **백엔드**: Spring Boot · MySQL · JWT 인증  
> **프론트엔드**: React · TypeScript · Tailwind CSS  
> **NLP 서버**: Python · SBERT · Flask API  
> **배포**: AWS EC2, RDS, S3, CloudFront · GitHub Actions CI/CD

👉 [Filmus 서비스 바로가기](https://filmus.o-r.kr)
---

## 📌 주요 기능

| 기능 | 설명 |
|------|------|
| 🔍 **기본 검색** | 제목, 감독, 배우 기반 영화 검색 (KMDb Open API 연동) |
| ✨ **줄거리 기반 추천** | 사용자가 입력한 줄거리에서 키워드를 추출하고 유사 영화 추천 |
| 🎞️ **영화 상세 페이지** | 줄거리, 포스터, 관련 정보 + 유사 영화 추천 제공 |
| ⭐ **찜하기 & 리뷰 작성** | 유저가 영화에 리뷰 및 별점 작성, 찜 기능 제공 |
| 📈 **트렌딩 & 추천** | 최근 인기작/추천작을 카드 형태로 홈에서 표시 |
| 👤 **회원가입 / 로그인** | JWT 기반 인증 · 마이페이지에서 찜/리뷰 관리 가능 |
| 🔐 **관리자 기능 (예정)** | DB 등록 / 리뷰 관리 등 (권한 기반 접근 제어)

---

## ⚙️ 기술 스택

### 🖥 Backend
- Java 21, Spring Boot 3
- Spring Security + JWT 인증
- MySQL 8 + MyBatis
- RESTful API 설계
- Swagger API 문서화
- Batch 키워드 동기화 로직

### 💻 Frontend
- React + TypeScript
- Tailwind CSS + ECharts
- React Router / Context API
- Axios Interceptor로 토큰 인증 처리

### 🧠 NLP Server
- Python + Flask
- SBERT (KLUE-NLI), KRWordRank
- 줄거리 텍스트 → 키워드 추출 → 유사도 기반 추천

### ☁ DevOps
- AWS EC2 (Spring, Flask 각각 분리)
- RDS(MySQL), S3 + CloudFront (정적 호스팅)
- Nginx + SSL (Certbot)
- GitHub Actions CI/CD

---

## 🗂️ 프로젝트 구조

```bash
filmus/
├── filmus-backend/         # Spring Boot 백엔드
├── filmus-frontend/        # React 프론트엔드
├── filmus-nlp/             # Python 기반 Flask 키워드 서버
└── README.md
