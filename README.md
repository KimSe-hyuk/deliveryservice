[README.md](https://github.com/user-attachments/files/21572637/README.md)
# 🥪 실시간 샌드위치 배달 플랫폼 (Team Project)

### 📌 프로젝트 개요
사용자가 맞춤형 샌드위치를 주문하고, 실시간으로 배달 상태를 확인할 수 있는 웹 플랫폼입니다.  
카카오 지도, Toss 결제, Redis 기반 실시간 채팅 등 실제 배달 서비스에 가까운 기능을 구현했습니다.

---

### 🧱 전체 서비스 구성

| 서비스 | 기능 | 개발자 | 코드 |
|--------|------|--------|------|
| auth-service | 로그인, 회원가입, 이메일 인증, JWT, OAuth2 | **김세혁(본인)** | ✅ [내 GitHub](https://github.com/KimSe-hyuk/auth-service) |
| ride-service | 배달 위치, 채팅 처리 (Redis + SQS) | **김세혁(본인)** | ✅ [내 GitHub](https://github.com/KimSe-hyuk/ride-service) |
| select-service | 재료 선택, 완성품 생성 | 팀원 A | 🔗 [링크](https://github.com/ChoDaeKyung/select-service) |
| payment-service | Toss 결제 + Redis Lock | 팀원 B | 🔗 [링크](https://github.com/ChoDaeKyung/payment-service) |
| file-service | Base64 이미지 처리 + S3 업로드 | 팀원 A | 🔗 [링크](https://github.com/ChoDaeKyung/file-service) |
| edge-service | Gateway 라우팅 관리 | 공동 | ✅ [내 GitHub](https://github.com/KimSe-hyuk/edge-service) |

---

### 💻 내가 맡은 기능

- `auth-service`:  
  - JWT 기반 로그인 및 토큰 재발급  
  - OAuth2 로그인 (카카오, 네이버, 구글)  
  - 이메일 인증 → Redis TTL 적용  

- `ride-service`:  
  - 배달원 실시간 위치 저장 (Redis)  
  - 카카오 길찾기 API 활용  
  - 채팅 메시지 처리 (SQS + Redis)  
  - 제품 상태 처리 (SQS + Redis) 
---

### 🔗 시연 영상  
📺 [https://youtu.be/boVifRHbhaQ](https://youtu.be/boVifRHbhaQ)

---

### 🚀 실행 방법
```bash
# Docker로 Redis + MySQL 띄우기
docker-compose up

# 서비스 실행
cd backend/auth-service
./gradlew bootRun
```

---

### 🧠 개발 환경

- Spring Boot 3.x / MyBatis / Redis / JWT / OAuth2
- AWS S3, SQS, Toss Payments
- Spring Cloud Gateway
- CI/CD: GitHub Actions + EKS 배포

---
