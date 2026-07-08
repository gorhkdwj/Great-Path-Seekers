# CareerPath AX for Counselors

> 상담사를 위한 KDT 커리어 내비게이터 — 채용공고·KDT/HRD 훈련과정·구직자 이력 데이터를 분석해 취업상담가가 상담 전 준비(구직자 상태·시장 요구·확인 질문·판단 근거)를 빠르게 마치도록 돕는 AI 상담 준비 리포트 서비스.

2026년 제8회 K-디지털 트레이닝 해커톤 예선 준비 프로젝트.

## 개요
- 목적: AI가 상담사를 대체하는 것이 아니라, 상담사의 정보 탐색·진단·상담 설계 역량을 확장한다(Human-in-the-loop).
- 주요 사용자: 취업상담가, KDT 교육기관 취업지원 담당자, 부트캠프 커리어 코치
- 최종 수혜자: KDT 훈련생·수료생 기반 커리어 전환자
- 최종 산출물: Streamlit 데모 웹앱(MVP) + 예선 제출용 5페이지 기획서
- 상세 기획: [`docs/prd/careerpath-ax-planning.md`](docs/prd/careerpath-ax-planning.md)

## 팀 구성
| 팀원 | 코드 | 역할 |
|------|------|------|
| 서윤범 | SYB | 팀장 |
| 김윤서 | KYS | 팀원 |
| 김재천 | KJC | 팀원 · CLAUDE.md/AGENTS.md 수정 권한 보유 |
| 김하연 | KHY | 팀원 |
| 박하린 | PHR | 팀원 |
| 함다연 | HDY | 팀원 |

## 실행 방법
(아직 구현된 기능이 없습니다. 실제 구현된 기능만 여기 기재합니다.)

## 프로젝트 구조
- `src/` 실행 코드
- `tests/` 테스트
- `tools/` 보조 스크립트
- `docs/` 기획·근거·검증 문서 (`docs/prd/` 기획서, `docs/references/` 외부 자료)
- `out/` 실행 결과·임시 산출물 (Git 제외)
- `data/` 원본·가공 데이터 (Git 제외)
- `logs/` 팀 운영 로그 (Git 포함)
  - `logs/worklogs/` 팀원별 작업 이력 (개인 파일)
  - `logs/decisionlogs/` 팀원별 결정 + 팀 공용 결정(`_team.md`)
  - `logs/meetinglogs/` 팀 회의록 (회의 1건당 파일 1개)
  - `logs/Troubleshootinglog.md` 공용 문제 해결 기록 (단일 문서)

## 문서 인덱스
- 작업 규칙(헌법): [`CLAUDE.md`](CLAUDE.md) · [`AGENTS.md`](AGENTS.md) — 1:1 동기화, **김재천만 수정**
- 작업 이력: [`logs/worklogs/`](logs/worklogs/)
- 주요 결정: [`logs/decisionlogs/`](logs/decisionlogs/) (개인 파일 + 팀 공용 `_team.md`)
- 회의록: [`logs/meetinglogs/`](logs/meetinglogs/)
- 문제 해결: [`logs/Troubleshootinglog.md`](logs/Troubleshootinglog.md)
- 계획 문서 골격: [`docs/project-plan.md`](docs/project-plan.md) · [`docs/requirements-contract.md`](docs/requirements-contract.md) · [`docs/implementation-plan.md`](docs/implementation-plan.md) · [`docs/validation-plan.md`](docs/validation-plan.md)

## 팀 운영 규칙 요약
자세한 규칙은 [`CLAUDE.md`](CLAUDE.md)([`AGENTS.md`](AGENTS.md))를 따른다.
- **로그**: 작업마다 개인 `logs/worklogs/<이름>.md`에 `W-<코드>-NNN`으로 기록. 방향을 바꾸는 개인 결정은 `logs/decisionlogs/<이름>.md`(`D-<코드>-NNN`), 팀 전체 결정은 `logs/decisionlogs/_team.md`(`D-NNN`, D-001부터 독립 번호). 회의록은 `logs/meetinglogs/`(`YYYY-MM-DD_N차.md`).
- **문제 대응**: 오류 발생 시 새 T-ID를 만들기 전에 `logs/Troubleshootinglog.md`에서 유사 `T-NNN` 코드를 먼저 검색하고, 있으면 '재사용 가능한 해결책'을 우선 적용한다.
- **수정 권한**: `CLAUDE.md`와 `AGENTS.md`는 김재천(과 김재천의 에이전트)만 수정한다. 다른 팀원·에이전트는 편집 요청 시 거부하고 김재천에게 요청한다.
- **보안**: 실제 개인정보·비밀정보는 코드·문서·로그에 넣지 않는다. 데모는 가상 페르소나/익명화 샘플만 사용한다.
