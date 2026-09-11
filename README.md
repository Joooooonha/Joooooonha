# 박준하

### Backend Developer

주변에서 발견한 문제를 직접 작동하는 서비스로 만들고 검증합니다.

Java와 Spring Boot를 중심으로 API, 데이터 흐름과 운영 구조를 설계하며, **제가 없어도 안정적으로 돌아가는 백엔드**를 만드는 데 성취감을 느낍니다. 문제를 해결하는 데 필요하다면 SwiftUI, React, 컴퓨터 비전처럼 낯선 분야도 직접 다룹니다. 결과만 정리하기보다 판단의 근거, 실패한 조건과 적용 범위를 기록하며 다음 결정을 개선합니다.

## 기술

| 영역 | 기술 | 활용 경험 |
|---|---|---|
| **Backend** | Java, Spring Boot, JPA, REST API | 인증·소유권, 외부 API 결합, 캐시 갱신, 비동기 작업과 실패 상태 설계 |
| **Client** | Swift, SwiftUI, MapKit, React, Vite | 러닝 코스 iOS 앱과 지도 기반 응급실 웹 서비스 구현 |
| **Data · AI** | Python, OpenCV, YOLO Pose, MediaPipe Pose, DTW, XGBoost | 춤 영상 정렬·피드백과 정면 웹캠 자세 감지 실험 |
| **Data · Infra** | PostgreSQL, MySQL, AWS EC2, Cloudflare R2 · Tunnel, GitHub Actions | 데이터 저장, 객체 스토리지, 홈서버·클라우드 연결과 배포 자동화 |

## 대표 프로젝트

### [CoCo](https://github.com/Joooooonha/CoCo) — 러닝 코스 선택 iOS 앱

`2026.07–현재` · Apple Developer Academy AI Playground 4일 팀 활동 이후 개인 개발

- **해결하고자 한 문제**: 낯선 러닝 코스를 선택할 때 글 후기만으로는 실제 경로와 경관·주의·편의 정보를 판단하기 어려운 문제
- **참여 범위**: CBL 질문·인터뷰를 통한 문제 정의에 참여하고, 교육 이후 SwiftUI·MapKit 앱과 Spring Boot 서버, 배포 환경을 개인 개발
- **핵심 구현**: 구간별 경로 캐시와 부분 실패 복구, 게스트 계정의 소셜 계정 승계, presigned URL 기반 사진 업로드
- **현재 상태**: MVP 기능 완료, 품질 강화 및 TestFlight 준비

### [ODO — Dance Analyzer](https://github.com/Joooooonha/dance-analyzer-service) — 춤 영상 비교 서비스

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

## 경험과 연구

### [Excel Streaming Parser Study](https://github.com/Joooooonha/excel-streaming-parser-study) — 인턴십 기술 사례

- 제한된 JVM heap에서 가변 크기의 Excel 파일을 처리하기 위한 파싱 구조와 작업 상태, 동시성 제어를 검토했습니다.
- 합성 `.xlsx`를 사용한 로컬 실험에서 Workbook 전체 로딩 방식은 50,000행을 `-Xmx512m`과 `-Xmx768m`에서 완료하지 못했고, SAX 기반 행·출력 스트리밍 방식은 `-Xmx512m`에서 완료됐습니다.
- 회사 코드와 고객 데이터를 제외하고 실험 환경, 원시 측정값, 의사결정 과정과 한계를 공개 문서로 재구성했습니다.

### [TurtleHunter](https://github.com/Joooooonha/turtlehunter) — 정면 웹캠 자세 감지 연구

`2025.12.30–2026.01.12` · 2인 프로젝트

- 정면 카메라에서 목 전진과 상체 전체 숙임을 구분하기 위해 개인 기준 자세 대비 상대 피처를 설계했습니다.
- MediaPipe Pose 랜드마크·XGBoost 기반 추정 파이프라인과 실시간 상태·알림 로직을 구현했습니다.
- 단일 환경의 제한된 연속 관측 결과이며, 의료 진단이나 다양한 사용자에 대한 일반화 성능으로 표현하지 않습니다.

## 활동

- **Apple Developer Academy AI Playground** — 4일간 CBL로 문제를 정의하고 CoCo의 Solution Concept과 프로토타입을 설계했습니다.
- **대학교 스트릿댄스 동아리 팀장** — 후배들과 공연을 준비하며 발견한 연습 문제에서 ODO를 시작했습니다.
