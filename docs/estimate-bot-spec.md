# 대화형 외주 견적 산출기 기획서 (MVP)

## 1. 서비스 개요
- 목적: 대화형 인터페이스로 의뢰인의 요구사항을 수집하고, 자동으로 견적을 산출하는 웹 서비스
- 타겟: 비개발자 의뢰인, 프리랜서/소규모 개발팀

## 2. 사용자 플로우 요약
1. 의뢰인이 프로젝트 아이디어를 입력
2. 시스템이 보완 질문 진행
3. 요구사항 자동 요약
4. 기능별 포인트 계산
5. 견적 및 기간 산출
6. 결과 요약 제공 (복사/다운로드)

## 3. 챗봇 톤 & 페르소나
- 역할: 전문 PM / 기업 컨설턴트
- 말투: 존댓말, 단정한 문장, 과도한 감탄 배제

## 4. 기능 포인트 테이블 (요약)
```json
{
  "base": {
    "mobile_primary": 40,
    "mobile_additional": 25,
    "web_front": 35,
    "admin_web": 30,
    "backend_api": 40,
    "infra_deploy": 25
  },
  "features": {
    "auth_email": 15,
    "auth_social_primary": 8,
    "auth_social_additional": 5,
    "auth_roles": 15,
    "crud_entity": 12,
    "file_upload": 8
  }
}
```
## 5. 견적 계산 로직
- 총포인트 = 플랫폼 베이스 + 기능 포인트
- 총금액 = 총포인트 × pointPrice × 디자인계수 × 복잡도계수 × 리스크계수

## 6. MVP 범위
- Flutter Web 기반 단일 페이지
- 대화형 UI
- 계산 및 결과 요약
- 결과 텍스트 복사

