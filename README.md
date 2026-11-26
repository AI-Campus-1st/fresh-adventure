# fresh-adventure

AI-Campus-1st 캡스톤 프로젝트 fresh-adventure의 메인 레포입니다.

| 항목 | 내용 |
| --- | --- |
| 프로젝트명 | fresh-adventure |
| 제품명 | fresh-adventure |
| 팀명 | 땅굴탐험대 |
| 제품 카테고리 | Fresh Food Marketing Intelligence |
| 핵심 가치 | Golden Time Discovery (판매 골든타임 발견) |

## 프로젝트 개요

fresh-adventure는 중소 규모 온라인 신선식품 판매사의 MD·마케터를 위한 신선식품 마케팅 인텔리전스 제품입니다(개발 예정).
외부 시장 데이터(네이버 데이터랩, KOSIS, KAMIS, 공영도매시장, 기상청, 관세청, 특일정보)를 통합해
잠재적 판매 골든타임을 찾고, 선제적인 마케팅·행사 시점 결정을 돕습니다. 원가 위험이 있는 품목도 함께 알려 줍니다.

- 승인된 PTS 기준: [docs/planning/PTS.md](docs/planning/PTS.md) (v0.2, 2026-11-26 승인)
- 최신 기획안: [docs/proposal/proposal_v3.2.md](docs/proposal/proposal_v3.2.md) (1차 확정본, PTS 기준으로 정렬 예정)

여기에 적힌 기능은 모두 **계획 단계**입니다. 기획안 v3.1은 이전 가칭 "FreshLens"를 사용합니다.

| 항목 | 내용 |
| --- | --- |
| 프로젝트 기간 | 2026-11-24 ~ 2027-01-07 |
| 최종 경연 | 2027-01-08 |
| 팀 인원 | 4명 |

## 레포 목록

| 레포 | 공개 | 역할 |
| --- | --- | --- |
| [fresh-adventure](https://github.com/AI-Campus-1st/fresh-adventure) | Public | 프로젝트 문서, 관리, 공유 계약(데이터·API), 산출물 |
| [fresh-adventure-data](https://github.com/AI-Campus-1st/fresh-adventure-data) | Private | 데이터 수집, 전처리, 분석, 검증, 적재 |
| [fresh-adventure-fe](https://github.com/AI-Campus-1st/fresh-adventure-fe) | Public | 사용자 화면, 대시보드, 데이터 시각화 |
| [fresh-adventure-be](https://github.com/AI-Campus-1st/fresh-adventure-be) | Private | API 서비스, DB 조회, 비즈니스 로직, AI·LLM 연동 |

Private 레포는 팀원만 접근할 수 있습니다.

## 레포별 책임 범위

- **fresh-adventure (이 레포):** 승인된 문서, 프로젝트 관리, 공유 아키텍처 명세, 공유 데이터·API 계약, 주간일지, 아키텍처 결정 기록(ADR), 공개 산출물을 관리합니다.
  운영 코드, 인증 정보, 제한된 데이터는 두지 않습니다.
- **fresh-adventure-data:** 데이터를 수집·처리하고 분석 결과 테이블을 만듭니다. 원본 데이터는 Git에 올리지 않습니다.
- **fresh-adventure-be:** 분석 결과를 API로 제공하고 AI·LLM 기능을 연결합니다. 분석 계산을 다시 구현하지 않습니다.
- **fresh-adventure-fe:** 대시보드와 시각화를 보여 줍니다. 비밀값을 두지 않고, 외부 서비스는 백엔드를 거쳐서만 호출합니다.

## 문서 안내

| 경로 | 내용 |
| --- | --- |
| [docs/proposal/](docs/proposal/) | 버전별 기획안 (최신: v3.2) |
| [docs/planning/](docs/planning/) | PTS 정의, 범위, 일정, 요구사항 |
| [docs/architecture/](docs/architecture/) | 시스템 아키텍처 명세 |
| [docs/data/](docs/data/) | 데이터 출처, 스키마, 데이터 사전 |
| [docs/analytics/](docs/analytics/) | 분석 방법론과 지표 정의 |
| [docs/contracts/](docs/contracts/) | 레포 간 공유 데이터·API 계약 |
| [docs/design/](docs/design/) | UI/UX 디자인과 와이어프레임 |
| [docs/management/](docs/management/) | 회의록, 역할, 프로젝트 관리 |
| [docs/weekly/](docs/weekly/) | 주간일지 |
| [docs/adr/](docs/adr/) | 아키텍처 결정 기록 |
| [docs/testing/](docs/testing/) | 테스트 전략과 검증 보고서 |
| [docs/deployment/](docs/deployment/) | 배포·운영 가이드 |
| [docs/conventions.md](docs/conventions.md) | 브랜치·커밋·PR·비밀값 관리 규칙 |
| [assets/](assets/) | 다이어그램, 스크린샷, 브랜딩 자료 |
| [deliverables/](deliverables/) | 발표 자료, 보고서, 회고 |

## 현재 상태

- Phase 01(PTS 정의) 완료: PTS v0.2 승인 (2026-11-26)
- 레포 초기 구조 구성 완료 (메인·FE). data·BE 레포 로컬 초기화는 대기 중입니다.
- 애플리케이션 기능, 데이터 파이프라인, 분석 결과는 아직 구현되지 않았습니다.
- 프런트엔드·백엔드 기술 스택은 팀 승인 대기 중입니다.

## 보안

이 레포는 **Public**입니다. API 키, `.env` 파일, 인증 정보, 원본 데이터, 네이버 데이터랩 수집값은 절대 올리지 마세요.
