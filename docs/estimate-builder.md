# 프로젝트명
대화형 외주 견적 산출 웹 애플리케이션 (Chat-based Estimate Builder)

## 목적
비전문가 의뢰인도 대화형 인터뷰 방식으로 서비스 요구사항을 설명하면,
시스템이 필요한 추가 질문을 하고 기능을 정리해주며,
최종적으로 개발 견적과 예상 기간을 자동 산출하는 웹 기반 도구.

결과물은 PDF 또는 텍스트로 제공.

---

# 📌 전체 화면 구조
1. **메인 시작 페이지**
2. **대화형 상담 화면 (Chat UI)**
3. **요구사항 자동 요약 화면**
4. **견적 산출 결과 화면**
5. **PDF/텍스트 다운로드 영역**

---

# 📌 페이지별 요구사항 상세

## 1. 메인 시작 페이지
### 목적
사용자가 상담을 시작하도록 안내.

### 구성 요소
- 상단 타이틀: “대화형 견적 상담 시작”
- 간단 설명 문구
- 입력창(텍스트 한 줄)
- 버튼: “상담 시작하기”
- Material Design 3 기반 깔끔한 레이아웃

---

## 2. 대화형 상담 화면
### 목적
의뢰인의 설명을 기반으로 추가 질문을 진행해 정보 수집.

### UI 구성
- 좌측: 채팅 버블 UI (사용자/시스템)
- 입력창 + 전송 버튼
- 자동 스크롤 영역
- 메시지 구분: 사용자(우측), 시스템(좌측)
- 색상 톤: 기업형(화이트/네이비/블루)

### 대화 흐름(요약)
1) “어떤 서비스를 만들고 싶으신가요?”  
2) “누가 사용하는 서비스인가요?”  
3) “앱/웹/관리자 페이지 중 어떤 플랫폼이 필요할까요?”  
4) “로그인/권한 기능이 필요할까요?”  
5) “알림 기능이 필요하신가요?”  
6) “지도/위치 관련 기능이 필요할까요?”  
7) “결제/구독 기능이 계획되어 있나요?”  
8) “관리자가 데이터를 관리해야 하나요?”  
9) “디자인은 템플릿 기준인가요? 완전 커스텀인가요?”

모든 질문은 전문 PM/컨설턴트 톤으로.

---

## 3. 요구사항 자동 요약 화면
### UI 구조
- 카드 형태로 주요 요구사항 정리:
  - 플랫폼(앱/웹/관리자)
  - 핵심 기능
  - 알림/결제/위치 여부
  - 관리자 기능
  - 디자인 난이도
- “수정하기” 버튼
- 미니멀한 카드 UI

---

## 4. 견적 산출 결과 화면
### UI 구성
- 큰 금액 텍스트: “예상 견적 ○○만원”
- 작은 텍스트: “예상 개발 기간 ○~○주”
- 기능별 포인트 리스트
- 옵션: “유지보수 비용 안내”
- 버튼: “PDF 다운로드”, “텍스트 복사”
- 기업형 비주얼

---

# 📌 기능 포인트 구조 (Stitch가 구조 이해하도록 요약)
- base.mobile_primary: 40
- base.mobile_additional: 25
- base.web_front: 35
- base.admin_web: 30
- base.backend_api: 40
- base.infra_deploy: 25

- features.auth_email: 15
- features.auth_social_primary: 8
- features.auth_roles: 15
- features.crud_entity: 12
- features.file_upload: 8
- features.push_notification: 15
- features.map_basic: 20
- features.realtime_location: 35
- features.payment_basic: 35
- features.subscription: 25
- features.external_api: 18

계수:
- design.template: 0.9
- design.custom: 1.0
- design.full_branding: 1.2
- complexity.simple: 1.0
- complexity.logic: 1.1
- complexity.realtime: 1.2
- risk.default: 1.05

---

# 📌 견적 계산 로직(요약)

---

# 📌 스타일 가이드
- Material Design 3 기반
- 기업형 미니멀 스타일
- 컬러 팔레트: 블루/네이비/그레이
- 폰트: 기본 Material Typography
- 여백/간격은 8px 단위 그리드

---

# 📌 결과물
- SPA 형태 Flutter Web UI
- 시각적으로 안정적이고 읽기 쉬운 레이아웃
- 대화 중심 구조
