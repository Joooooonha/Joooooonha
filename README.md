# 박준하

### Backend Developer

Java와 Spring Boot를 중심으로 서비스 API와 데이터 흐름을 개발하는 백엔드 개발자 박준하입니다.

사내 대시보드의 Spring 전환과 DB 쿼리 최적화를 담당했습니다. 개인 프로젝트로는 공공데이터 기반 응급실 지도 서비스, 춤 영상 분석 서비스와 러닝 코스 iOS 앱을 개발했습니다. API와 DB를 중심에 두고 운영 제약, 데이터 신뢰성과 실패 조건을 코드와 문서로 확인합니다.

[![Email](https://img.shields.io/badge/Email-wnsgk5175497%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:wnsgk5175497@gmail.com)

## 기술

**Backend**

![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white)
![REST API](https://img.shields.io/badge/REST%20API-005571?style=flat-square)

**Vision · AI**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![YOLO Pose](https://img.shields.io/badge/YOLO%20Pose-111F68?style=flat-square&logo=ultralytics&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square)
![DTW](https://img.shields.io/badge/DTW-5B5B5B?style=flat-square)
![XGBoost](https://img.shields.io/badge/XGBoost-EB5B28?style=flat-square)

**Data · Infra**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**Collaboration**

![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=flat-square&logo=slack&logoColor=white)

## 경력

### 에픽카 — Backend Developer Intern

`2026.03–2026.06`

- FastAPI 기반 사내 매출 현황 대시보드를 Spring Boot로 마이그레이션하며 구조 개선, 쿼리 오류 수정과 DB 성능 최적화를 담당했습니다.
- 쿼리 단위 Repository와 Facade로 Service 의존성을 정리하고, 접근 경로에 따라 Repository를 선택하는 Strategy·Provider 구조를 구현했습니다.
- 누락 필터와 잘못된 집계 로직을 수정해 과소 집계되던 총매출의 13% 오차를 바로잡았습니다.
- p6spy와 `EXPLAIN ANALYZE`로 병목을 선별하고 복합 인덱스를 재설계해, 해당 대시보드 측정에서 API 평균 응답시간을 522ms에서 226ms로 줄였습니다.
- S3 업로드와 Excel 파싱 구조를 검토한 과정은 회사 코드와 데이터를 제외한 [공개 기술 사례](https://github.com/Joooooonha/excel-streaming-parser-study)로 재구성했습니다.

## 대표 프로젝트

### [CoCo](https://github.com/Joooooonha/CoCo) — 러닝 코스 선택 iOS 앱

`2026.07–현재` · Apple Developer Academy AI Playground 4일 팀 활동 이후 개인 개발

- **해결하고자 한 문제**: 낯선 러닝 코스를 선택할 때 글 후기만으로는 실제 경로와 경관·주의·편의 정보를 판단하기 어려운 문제
- **참여 범위**: CBL 질문·인터뷰를 통한 문제 정의에 참여하고, 교육 이후 SwiftUI·MapKit 앱과 Spring Boot 서버, 배포 환경을 개인 개발
- **핵심 구현**: 구간별 경로 캐시와 부분 실패 복구, 게스트 계정의 소셜 계정 승계, presigned URL 기반 사진 업로드
- **현재 상태**: MVP 기능 완료, 품질 강화 및 TestFlight 준비

### [ODO — Dance Analyzer](https://github.com/Joooooonha/ODO) — 춤 영상 비교 서비스

`2025.03–현재` · 개인 프로젝트 · [서비스](https://odostudio.site)

- **해결하고자 한 문제**: 정기 연습 밖에서도 후배가 기준 영상과 자신의 춤을 비교하며 동작을 점검할 수 있는 방법
- **참여 범위**: 포즈 분석 엔진 설계·검증, Spring Boot·React 웹 서비스 구현과 배포
- **핵심 구현**: 포즈에서 관절 각도를 추출하고 DTW로 서로 다른 시작 시점과 속도를 정렬해 구간별 피드백으로 변환
- **확인한 범위**: 기본기 동작에서 가능성을 확인했으며, 관절 겹침과 2D 영상의 모호성은 현재 분석의 한계로 유지

### [FindEr](https://github.com/Joooooonha/FindEr) — 주변 응급실 정보 탐색 서비스

개인 프로젝트 · 기획, 프론트엔드, 백엔드, 배포 · [서비스](https://find-er.info)

- **해결하고자 한 문제**: 응급실 진료가 필요한 상황에서 주변 기관의 위치와 공개된 진료·병상 정보를 한 화면에서 비교하기 어려운 문제
- **핵심 구현**: 여러 공공데이터를 병원 식별자 `hpid`로 결합하고, 사용자 요청과 외부 API 갱신을 캐시·스케줄러로 분리
- **데이터 처리**: 오래됐거나 비정상인 병상 수를 `UNKNOWN`으로 처리하고, 외부 API 실패 시 정상 캐시를 유지
- **확인한 한계**: 정보 접근성을 개선할 수는 있지만 실제 병원 수용을 보장하거나 응급의료 체계의 구조적 문제를 해결할 수는 없음

## 연구

### [TurtleHunter](https://github.com/Joooooonha/turtlehunter) — 정면 웹캠 자세 감지

`2025.12.30–2026.01.12` · 2인 프로젝트

- 정면 카메라에서 목 전진과 상체 전체 숙임을 구분하기 위해 개인 기준 자세 대비 상대 피처를 설계했습니다.
- MediaPipe Pose 랜드마크·XGBoost 기반 추정 파이프라인과 실시간 상태·알림 로직을 구현했습니다.
- 단일 환경의 제한된 연속 관측 결과이며, 의료 진단이나 다양한 사용자에 대한 일반화 성능으로 표현하지 않습니다.

## 학력

- **동국대학교 컴퓨터공학전공** · `2021.03–2026.08`

## 수상 · 자격

- **IoT Coss 아이디어톤 우수상** · `2026` — 감귤박 자원 재순환
- **TOPCIT Lv3** · `2025` — 과학기술정보통신부
- **교내 아두이노 어드벤처디자인 장려상** · `2023` — 주차장 자동 배정 시스템
- **동국대학교 학기 우등생** · `2021`, `2023`

## 교육 · 활동

- **Apple Developer Academy AI Playground** · `2026.07` — 4일간 CBL로 문제를 정의하고 CoCo의 Solution Concept과 프로토타입 설계
- **새싹(SeSAC) 자바 백엔드 과정 수료** · `2025.09–2026.03`
- **컴퓨터 학술 중앙동아리 CAPS 학술부 팀장** · `2023.09–2025.12` — 스터디 개편과 알고리즘 대회 출제 TF 참여
- **동국대학교 스트릿댄스 동아리 ODC 브레이킹 팀장** · `2024.11–2025.11` — 공연 준비 및 댄스 분석 서비스 ODO 개발
- **동국대학교 한글 봉사 동아리 하람 교육국** · `2024.09–2025.09` — 외국인 학생 대상 한국 문화 수업 진행
