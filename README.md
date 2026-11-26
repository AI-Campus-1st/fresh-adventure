# FreshLens 🥬 — 땅굴탐험대

> 데이터로 찾는 신선식품 판매 타이밍과 타깃

온라인 식품몰 MD·마케터가 **누구에게, 언제, 어떤 신선식품을, 얼마에** 팔지 공공 데이터(네이버 데이터랩, KOSIS, KAMIS, 공영도매시장, 기상청 등)로 결정하도록 돕는 웹 대시보드와 AI 마케팅 리포트입니다.

이 레포는 팀의 **메인 레포**로, 기획 문서와 주간일지를 관리합니다. 코드는 아래 레포에서 관리합니다.

## 레포 목록

| 레포 | 역할 | 공개 | 주요 기술 |
| --- | --- | --- | --- |
| [fresh-adventure](https://github.com/AI-Campus-1st/fresh-adventure) | 메인 — 기획 문서, 주간일지, 협업 규칙 | Public | Markdown |
| [fresh-adventure-data](https://github.com/AI-Campus-1st/fresh-adventure-data) | 데이터 파이프라인 — API 수집, ETL, DW·마트, 분석·예측 | Private | Python, Pandas, PostgreSQL, S3 |
| [fresh-adventure-fe](https://github.com/AI-Campus-1st/fresh-adventure-fe) | 프런트엔드 — 웹 대시보드 | Public | (팀 합의 후 확정, 예: React + Plotly.js) |
| [fresh-adventure-be](https://github.com/AI-Campus-1st/fresh-adventure-be) | 백엔드 — 화면용 API, AI 리포트 | Private | FastAPI, Docker, EC2 |

> Private 레포는 팀원만 접근할 수 있습니다.

## 아키텍처 흐름

```
[공공 API] ──▶ data: 수집기 ──▶ S3(원본) ──▶ ETL ──▶ RDS PostgreSQL(DW·마트·분석 결과)
                                                          │
                                         be: FastAPI ◀────┘ ──▶ LLM API (AI 리포트)
                                              │
                                         fe: 웹 대시보드 (S3 + CloudFront)
```

## 문서

| 문서 | 위치 |
| --- | --- |
| 기획안 | [docs/proposal](docs/proposal) |
| 주간일지 | [docs/weekly](docs/weekly) |
| 협업 규칙 (브랜치·커밋·PR·API 키) | [docs/conventions.md](docs/conventions.md) |

## 폴더 구조

```
fresh-adventure/
├── README.md                 # 프로젝트 소개, 레포 목록
├── docs/
│   ├── conventions.md        # 협업 규칙
│   ├── proposal/             # 기획안 (버전별 파일)
│   └── weekly/               # 주간일지
│       ├── README.md         # 작성 규칙, 일지 목록
│       └── _template.md      # 주간일지 템플릿
└── .github/
    └── pull_request_template.md
```

## 팀

| 직무 | 역할 | 이름 |
| --- | --- | --- |
| 경영 | PM·비즈니스 전략 | |
| 마케팅 | 수요·타깃·프로모션 전략 | |
| 데이터분석 | 분석·예측 리드 | |
| BI엔지니어 | 파이프라인·대시보드 | |

> ⚠️ 이 레포는 **Public**입니다. API 키, `.env`, 원본 데이터, 데이터랩 수집값은 절대 올리지 마세요.
