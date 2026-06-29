<div align="center">

# 📈 주식 지능형 분석 시스템

[![GitHub stars](https://img.shields.io/github/stars/ZhuLinsen/daily_stock_analysis?style=social)](https://github.com/ZhuLinsen/daily_stock_analysis/stargazers)
[![CI](https://github.com/ZhuLinsen/daily_stock_analysis/actions/workflows/ci.yml/badge.svg)](https://github.com/ZhuLinsen/daily_stock_analysis/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-Ready-2088FF?logo=github-actions&logoColor=white)](https://github.com/features/actions)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)](https://hub.docker.com/r/zhulinsen/daily_stock_analysis)

<p align="center">
  <img src="https://trendshift.io/api/badge/trendshift/repositories/18527/daily?language=Python" alt="#1 Python Repository Of The Day | Trendshift" width="250" height="55"/>&nbsp;<a href="https://hellogithub.com/repository/ZhuLinsen/daily_stock_analysis" target="_blank"><img src="https://api.hellogithub.com/v1/widgets/recommend.svg?rid=6daa16e405ce46ed97b4a57706aeb29f&claim_uid=pfiJMqhR9uvDGlT&theme=neutral" alt="Featured｜HelloGitHub" width="230" /></a>
</p>

> 🤖 AI 대형 모델 기반 A주/홍콩주/미국주/일본주/한국주 관심 종목 지능형 분석 시스템입니다. 매일 자동으로 분석하고 기업 WeChat/Feishu/Telegram/Discord/Slack/이메일로 "의사결정 대시보드"를 발송합니다.

[**제품 미리보기**](#-제품-미리보기) · [**기능**](#-기능) · [**빠른 시작**](#-빠른-시작) · [**발송 예시**](#-발송-예시) · [**문서 센터**](docs/INDEX.md) · [**전체 가이드**](docs/full-guide.md)

[简体中文](README.md) | [English](docs/README_EN.md) | [繁體中文](docs/README_CHT.md) | 한국어

</div>

## 💖 스폰서

<div align="center">
  <p align="center">
    <a href="https://open.anspire.cn/?share_code=QFBC0FYC" target="_blank"><img src="./docs/assets/anspire.png" alt="Anspire Open 모델 및 검색 서비스" width="300" height="141" style="width: 300px; height: 141px; object-fit: contain;"></a>
    <a href="https://serpapi.com/baidu-search-api?utm_source=github_daily_stock_analysis" target="_blank"><img src="./docs/assets/serpapi_banner_zh.png" alt="실시간 금융 뉴스 검색 데이터 수집 - SerpApi" width="300" height="141" style="width: 300px; height: 141px; object-fit: contain;"></a>
  </p>
</div>

## 🖥️ 제품 미리보기

<p align="center">
  <img src="docs/assets/readme_workspace_tour_20260510.gif" alt="DSA Web 작업대 데모" width="720">
</p>

## ✨ 기능

| 기능 | 범위 |
|------|------|
| AI 의사결정 보고서 | 핵심 결론, 점수, 추세, 매수/매도 가격대, 위험 경고, 촉매 요인, 실행 체크리스트 |
| 다중 시장 데이터 집계 | A주, 홍콩주, 미국주, ETF: 시세, K선, 기술 지표, 자금 흐름, 매물대, 뉴스, 공시, 펀더멘털. 일본주/한국주(`.T` / `.KS` / `.KQ`): YFinance 일봉과 기본 시세, 기술 지표를 지원하며 `capital_flow`, `dragon_tiger`, `boards` 및 일부 고급 블록은 시장 경계에 따라 `not_supported`로 강등됩니다. 자세한 내용은 [시장 지원 범위](docs/market-support.md)를 참고하세요. |
| Web / 데스크톱 작업대 | 수동 분석, 작업 진행률, 히스토리 보고서, 전체 Markdown, 백테스트, 포지션, 설정 관리, 라이트/다크 테마 |
| Agent 전략 질의 | 다중 턴 질의, 이동평균/Chan 이론/파동/추세/핫테마/이벤트/성장/기대 재평가 등 15개 내장 전략, Web/Bot/API 지원 |
| 스마트 가져오기와 자동완성 | 이미지, CSV/Excel, 클립보드 가져오기. 종목 코드/이름/병음/별칭 자동완성 |
| 자동화와 알림 | GitHub Actions, Docker, 로컬 스케줄 작업, FastAPI 서비스, 기업 WeChat/Feishu/Telegram/Discord/Slack/이메일 발송 |

> 기능 세부 사항, 필드 계약, 펀더멘털 P0 타임아웃 의미, 거래 규율, 데이터 소스 우선순위, Web/API 동작은 [전체 설정 및 배포 가이드](docs/full-guide.md)를 참고하세요.

### 기술 스택과 데이터 소스

| 유형 | 지원 |
|------|------|
| AI 모델 | [Anspire](https://open.anspire.cn/?share_code=QFBC0FYC), [AIHubMix](https://aihubmix.com/?aff=CfMq), Gemini, OpenAI 호환, DeepSeek, Tongyi Qianwen, Claude, Ollama 로컬 모델 등 |
| 시세 데이터 | [TickFlow](https://tickflow.org/auth/register?ref=WDSGSPS5XC), AkShare, Tushare, Pytdx, Baostock, YFinance, Longbridge |
| 뉴스 검색 | [Anspire](https://open.anspire.cn/?share_code=QFBC0FYC), [SerpAPI](https://serpapi.com/baidu-search-api?utm_source=github_daily_stock_analysis), [Tavily](https://tavily.com/), [Bocha](https://open.bocha.cn/), [Brave](https://brave.com/search/api/), [MiniMax](https://platform.minimaxi.com/), SearXNG |
| 소셜 심리 | [Stock Sentiment API](https://api.adanos.org/docs)(Reddit / X / Polymarket, 미국주 전용, 선택) |

> 전체 규칙은 [데이터 소스 설정](docs/full-guide.md#数据源配置)을 참고하세요.

## 🚀 빠른 시작

### 방법 1: [GitHub Actions(권장)](https://www.bilibili.com/video/BV11FEb66EXG/)

> 5분 안에 배포할 수 있고, 비용과 서버가 필요 없습니다.

#### 1. 저장소 Fork

오른쪽 위 `Fork` 버튼을 클릭하세요. 가능하다면 Star도 눌러 주세요.

#### 2. Secrets 설정

`Settings` → `Secrets and variables` → `Actions` → `New repository secret`

**AI 모델 설정(최소 하나 필요)**

먼저 모델 서비스 제공자를 하나 선택해 API Key를 입력하세요. 다중 모델, 이미지 인식, 로컬 모델, 고급 라우팅이 필요하면 [LLM 설정 가이드](docs/LLM_CONFIG_GUIDE.md)를 참고하세요.

| Secret 이름 | 설명 | 필수 |
|------------|------|:----:|
| `ANSPIRE_API_KEYS` | [Anspire](https://open.anspire.cn/?share_code=QFBC0FYC) API Key. 하나의 Key로 글로벌 인기 대형 모델과 웹 검색을 사용할 수 있으며 무료 한도가 포함됩니다. | **권장** |
| `AIHUBMIX_KEY` | [AIHubMix](https://aihubmix.com/?aff=CfMq) API Key. 전체 모델군을 전환해 사용할 수 있으며 이 프로젝트에서 10% 할인을 받을 수 있습니다. | **권장** |
| `GEMINI_API_KEY` | Google Gemini API Key | 선택 |
| `ANTHROPIC_API_KEY` | Anthropic Claude API Key | 선택 |
| `OPENAI_API_KEY` | OpenAI 호환 API Key(DeepSeek, Tongyi Qianwen 등 지원) | 선택 |
| `OPENAI_BASE_URL` / `OPENAI_MODEL` | OpenAI 호환 서비스를 사용할 때 입력 | 선택 |

> Ollama는 로컬 또는 Docker 배포에 더 적합하며, GitHub Actions에서는 클라우드 API 사용을 권장합니다.

**알림 채널 설정(최소 하나 필요)**

| Secret 이름 | 설명 |
|------------|------|
| `WECHAT_WEBHOOK_URL` | 기업 WeChat 봇 |
| `FEISHU_WEBHOOK_URL` | Feishu 봇 |
| `TELEGRAM_BOT_TOKEN` + `TELEGRAM_CHAT_ID` | Telegram |
| `DISCORD_WEBHOOK_URL` | Discord Webhook |
| `SLACK_BOT_TOKEN` + `SLACK_CHANNEL_ID` | Slack Bot |
| `EMAIL_SENDER` + `EMAIL_PASSWORD` | 이메일 발송 |

더 많은 채널, 서명 검증, 그룹 이메일, Markdown 이미지 변환 설정은 [알림 채널 상세 설정](docs/full-guide.md#通知渠道详细配置)을 참고하세요.

**관심 종목 설정(필수)**

| Secret 이름 | 설명 | 필수 |
|------------|------|:----:|
| `STOCK_LIST` | 관심 종목 코드. 예: `600519,hk00700,AAPL,7203.T,005930.KS` | ✅ |

**뉴스 소스 설정(권장)**

뉴스 소스는 심리, 공시, 이벤트, 촉매 요인의 품질에 큰 영향을 줍니다. 검색 서비스를 하나 이상 설정하는 것을 권장합니다.

| Secret 이름 | 설명 | 필수 |
|------------|------|:----:|
| `ANSPIRE_API_KEYS` | [Anspire AI Search](https://aisearch.anspire.cn/): 중국어 콘텐츠에 최적화되어 A주 뉴스와 심리 검색에 적합합니다. 같은 Key를 Anspire 대형 모델에도 재사용할 수 있습니다. | **권장** |
| `SERPAPI_API_KEYS` | [SerpAPI](https://serpapi.com/baidu-search-api?utm_source=github_daily_stock_analysis): 검색 엔진 결과 보강, 실시간 금융 뉴스에 적합 | **권장** |
| `TAVILY_API_KEYS` | [Tavily](https://tavily.com/): 범용 뉴스 검색 API | 선택 |
| `BOCHA_API_KEYS` | [Bocha Search](https://open.bocha.cn/): 중국어 검색 최적화, AI 요약 지원 | 선택 |
| `BRAVE_API_KEYS` | [Brave Search](https://brave.com/search/api/): 개인정보 보호 우선, 미국주 정보 보강 | 선택 |
| `MINIMAX_API_KEYS` | [MiniMax](https://platform.minimaxi.com/): 구조화 검색 결과 | 선택 |
| `SEARXNG_BASE_URLS` | 자체 구축 SearXNG 인스턴스: 무할당량 백업, 사설 배포에 적합 | 선택 |

더 많은 검색 소스, 소셜 심리, 강등 규칙은 [검색 서비스 설정](docs/full-guide.md#搜索服务配置)을 참고하세요.

#### 3. Actions 활성화

`Actions` 탭 → `I understand my workflows, go ahead and enable them`

#### 4. 수동 테스트

`Actions` → `每日股票分析` → `Run workflow` → `Run workflow`

#### 완료

기본적으로 매 **영업일 18:00(베이징 시간)** 자동 실행되며, 수동 실행도 가능합니다. 기본값에서는 비거래일(A/H/US 휴장일 포함)에 실행하지 않습니다. 강제 실행, 거래일 검사, 중단점 재개 규칙은 [전체 가이드](docs/full-guide.md#定时任务配置)를 참고하세요.

### 방법 2: [클라이언트 설정 튜토리얼](https://www.bilibili.com/video/BV11FEb66Eyr/) / 로컬 실행 / Docker 배포

```bash
# 프로젝트 클론
git clone https://github.com/ZhuLinsen/daily_stock_analysis.git && cd daily_stock_analysis

# 의존성 설치
pip install -r requirements.txt

# 환경 변수 설정
cp .env.example .env && vim .env

# 분석 실행
python main.py
```

자주 쓰는 명령:

```bash
python main.py --debug
python main.py --dry-run
python main.py --stocks 600519,hk00700,AAPL
python main.py --market-review
python main.py --schedule
python main.py --serve-only
```

> Docker 배포, 스케줄 작업, 클라우드 서버 접근은 [전체 가이드](docs/full-guide.md)를 참고하세요. 데스크톱 클라이언트 패키징은 [데스크톱 패키징 설명](docs/desktop-package.md)을 참고하세요.

## 📱 발송 예시

### 의사결정 대시보드

```text
🎯 2026-02-08 의사결정 대시보드
총 분석 3개 종목 | 🟢매수:0 🟡관망:2 🔴매도:1

📊 분석 결과 요약
⚪ 중우고신(000657): 관망 | 점수 65 | 상승
⚪ 영정주식(600105): 관망 | 점수 48 | 횡보
🟡 신래응재(300260): 매도 | 점수 35 | 하락

⚪ 중우고신 (000657)
📰 핵심 정보
💭 시장 심리: 시장은 회사의 AI 속성과 높은 실적 성장에 주목하고 있으며 심리는 긍정적입니다. 다만 단기 차익 실현과 주요 자금 유출 압력을 소화해야 합니다.
📊 실적 전망: 심리 정보에 따르면 2025년 3분기 누적 실적이 전년 대비 크게 증가했고 펀더멘털이 견조해 주가를 지지합니다.

🚨 위험 경고:

위험 1: 2월 5일 주요 자금이 3.63억 위안 순매도되어 단기 매물 압력에 유의해야 합니다.
위험 2: 매물 집중도가 35.15%로 높아 상승 저항이 커질 수 있습니다.
위험 3: 과거 규정 위반과 구조조정 관련 위험이 언급되어 지속 관찰이 필요합니다.
✨ 긍정 촉매:

촉매 1: 회사가 AI 서버 HDI 핵심 공급업체로 인식되며 AI 산업 발전 수혜가 기대됩니다.
촉매 2: 2025년 3분기 누적 비경상손익 제외 순이익이 전년 대비 407.52% 급증했습니다.
📢 최신 동향: 회사는 AI PCB 마이크로 드릴 분야의 선도 기업으로 평가되며 글로벌 주요 PCB/기판 업체와 깊게 연결되어 있습니다. 후속 자금 흐름을 관찰해야 합니다.

---
생성 시간: 18:00
```

### 시장 리뷰

```text
🎯 2026-01-10 시장 리뷰

📊 주요 지수
- 상하이종합: 3250.12 (🟢+0.85%)
- 선전성분: 10521.36 (🟢+1.02%)
- 차이넥스트: 2156.78 (🟢+1.35%)

📈 시장 개요
상승: 3920 | 하락: 1349 | 상한가: 155 | 하한가: 3

🔥 섹터 흐름
강세: 인터넷 서비스, 문화 미디어, 소금속
약세: 보험, 항공공항, 태양광 장비
```

## ⚙️ 설정 설명

전체 환경 변수, 모델 채널, 알림 채널, 데이터 소스 우선순위, 거래 규율, 펀더멘털 P0 의미, 배포 설명은 [전체 설정 가이드](docs/full-guide.md)를 참고하세요.

## 🖥️ Web 인터페이스

Web 작업대는 설정 관리, 작업 모니터링, 수동 분석, 히스토리 보고서, 전체 Markdown 보고서, Agent 질의, 백테스트, 포지션 관리, 스마트 가져오기, 라이트/다크 테마를 제공합니다. 실행 방법:

```bash
python main.py --webui
python main.py --webui-only
```

`http://127.0.0.1:8000`에 접속해 사용할 수 있습니다. 인증, 스마트 가져오기, 검색 자동완성, 히스토리 보고서 복사, 클라우드 서버 접근 등은 [로컬 WebUI 관리 인터페이스](docs/full-guide.md#本地-webui-管理界面)를 참고하세요.

## 🤖 Agent 전략 질의

사용 가능한 AI API Key를 설정하면 Web `/chat` 페이지에서 전략 질의를 사용할 수 있습니다. 명시적으로 끄려면 `AGENT_MODE=false`를 설정하세요.

- 이동평균 골든크로스, Chan 이론, 파동 이론, 상승 추세, 핫테마, 이벤트 드리븐, 성장 품질, 기대 재평가 등 내장 전략 지원
- 실시간 시세, K선, 기술 지표, 뉴스, 위험 정보 호출 지원
- 다중 턴 질의, 대화 내보내기, 알림 채널 전송, 백그라운드 실행 지원
- 사용자 정의 전략 파일과 다중 Agent 오케스트레이션 지원(실험적)

> Agent 세부 매개변수, `skill` 명명 호환성, 다중 Agent 모드, 예산 가드레일은 [전체 가이드](docs/full-guide.md#本地-webui-管理界面)와 [LLM 설정 가이드](docs/LLM_CONFIG_GUIDE.md)를 참고하세요.

## 🧩 관련 프로젝트

> DSA는 일상 분석 보고서에 집중합니다. 아래 두 같은 계열 프로젝트는 각각 종목 선별, 전략 검증, 전략 진화를 다루며 필요에 따라 함께 사용할 수 있습니다. 현재는 독립적으로 유지보수되며, 향후 DSA의 후보 종목 가져오기, 백테스트 검증, 보고서 연동을 우선 탐색할 예정입니다.

| 프로젝트 | 포지셔닝 |
|------|------|
| [AlphaSift](https://github.com/ZhuLinsen/alphasift) | 다중 팩터 종목 선별과 전체 시장 스캔. 종목 풀에서 후보 종목을 추출하는 데 사용 |
| [AlphaEvo](https://github.com/ZhuLinsen/alphaevo) | 전략 백테스트와 자기 진화. 전략 규칙을 검증하고 반복을 통해 전략 매개변수와 조합을 탐색 |

## 📬 문의와 협력

<table>
  <tr>
    <td width="92" valign="top"><strong>협력 이메일</strong></td>
    <td valign="top">
      <a href="mailto:zhuls345@gmail.com">zhuls345@gmail.com</a><br>
      프로젝트 문의, 배포 지원, 기능 확장
    </td>
    <td align="center" rowspan="3" valign="middle" width="148">
      <a href="http://xhslink.com/m/tU520DWCKT" target="_blank"><img src="./docs/assets/xiaohongshu_tick.jpg" width="112" alt="Xiaohongshu QR 코드"></a><br>
      <sub>스캔해서 Xiaohongshu 팔로우</sub>
    </td>
  </tr>
  <tr>
    <td width="92" valign="top"><strong>Xiaohongshu</strong></td>
    <td valign="top"><a href="http://xhslink.com/m/tU520DWCKT">Xiaohongshu 팔로우 환영</a></td>
  </tr>
  <tr>
    <td width="92" valign="top"><strong>문제 제보</strong></td>
    <td valign="top"><a href="https://github.com/ZhuLinsen/daily_stock_analysis/issues">Issue 제출</a></td>
  </tr>
</table>

## 📄 License

[MIT License](LICENSE) © 2026 ZhuLinsen

2차 개발이나 인용 시 이 저장소 출처를 표시해 주세요. 프로젝트의 지속적인 유지보수를 지원해 주셔서 감사합니다.

## ⚠️ 면책 조항

이 프로젝트는 학습과 연구 용도로만 제공되며 어떠한 투자 조언도 구성하지 않습니다. 주식 시장에는 위험이 있으며 투자는 신중해야 합니다. 작성자는 이 프로젝트 사용으로 발생하는 어떠한 손실에도 책임지지 않습니다.

---
