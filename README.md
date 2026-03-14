# AI Native Camp - MD 에디션

> 5일 후, 당신의 업무 방식은 영구적으로 바뀐다.

패션 플랫폼 MD를 위한 Claude Code 5일 집중 캠프.
코딩 경험 없이도, CSV 데이터 전처리부터 AI 에이전트 활용까지.

## Step 0: 사전 준비

캠프를 시작하기 전에 아래 도구들을 설치합니다. Windows 기준으로 안내합니다.

### 사전 확인

| 항목 | 조건 |
|------|------|
| **OS** | Windows 10 이상 |
| **RAM** | 4GB 이상 |
| **네트워크** | 인터넷 연결 필수 (오프라인 사용 불가) |
| **계정** | Claude Pro, Max, Teams, Enterprise 중 하나 |

---

### 0-1. Git 설치

Git은 코드와 파일의 변경 이력을 관리하는 도구입니다. 캠프 자료를 다운로드하는 데도 필요합니다.

1. https://git-scm.com/download/win 에서 다운로드
2. 설치 중 기본 옵션 그대로 진행 (Next만 누르면 됨)
3. 설치 완료 후 바탕화면이나 시작 메뉴에서 **Git Bash** 실행
4. 아래 명령어로 확인:

```bash
git --version
```

버전이 출력되면 성공입니다.

> **Git Bash**는 Git 설치 시 함께 설치되는 터미널입니다. 이 캠프에서는 Git Bash를 기본 터미널로 사용합니다.

---

### 0-2. Node.js 설치

Node.js는 JavaScript 실행 환경입니다. Claude Code 스킬 관리에 필요합니다.

1. https://nodejs.org 에서 **LTS 버전** 다운로드 (왼쪽 초록 버튼)
2. 설치 중 기본 옵션 그대로 진행
3. **Git Bash를 닫았다가 다시 열고** 아래 명령어로 확인:

```bash
node --version
npm --version
```

두 개 모두 버전이 출력되면 성공입니다.

---

### 0-3. Python 설치

Python은 데이터 처리와 자동화에 사용되는 프로그래밍 언어입니다.

1. https://www.python.org/downloads/ 에서 최신 버전 다운로드
2. **설치 첫 화면에서 "Add Python to PATH" 체크박스를 반드시 체크!** (가장 중요)
3. "Install Now" 클릭
4. **Git Bash를 닫았다가 다시 열고** 아래 명령어로 확인:

```bash
python --version
pip --version
```

두 개 모두 버전이 출력되면 성공입니다.

---

### 0-4. Claude Code 설치

**PowerShell에서 설치** (시작 메뉴에서 "PowerShell" 검색):

```powershell
irm https://claude.ai/install.ps1 | iex
```

또는 **CMD에서 설치**:

```cmd
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

설치 후 **Git Bash**를 열고 아래 명령어로 확인:

```bash
claude
```

Claude가 인사하면 성공입니다. 계정 인증(로그인) 안내가 나오면 그대로 진행하세요.

---

### 설치 체크리스트

| # | 항목 | 확인 명령어 (Git Bash) | 통과 기준 |
|---|------|----------------------|----------|
| 1 | Git | `git --version` | 버전 출력 |
| 2 | Node.js | `node --version` | 버전 출력 |
| 3 | npm | `npm --version` | 버전 출력 |
| 4 | Python | `python --version` | 버전 출력 |
| 5 | pip | `pip --version` | 버전 출력 |
| 6 | Claude Code | `claude` | Claude 인사 또는 로그인 안내 |

> 6개 모두 통과하면 준비 완료!

---

## Step 1: 캠프 자료 다운로드

Git Bash에서 아래 명령어를 순서대로 실행합니다:

```bash
git clone https://github.com/koobch/NEO-cladue-camp.git
cd NEO-cladue-camp
claude
```

마지막 `claude` 명령어를 실행하면 Claude Code가 시작됩니다.

> 시작되면 `/day1-setup-and-data` 를 입력하세요. Day 1이 시작됩니다!

## Skills as Curriculum

이 캠프의 커리큘럼은 **Claude Code Skills 그 자체**다.

슬라이드를 넘기며 듣는 강의가 아니다. `/day1-setup-and-data`를 실행하면 Claude가 직접 가르치고, 질문하고, 실습을 안내한다. 매일 새로운 Skill이 열리고, 어제 배운 것 위에 오늘을 쌓는다.

Skill을 만드는 법을 Skill로 배운다. 이것이 이 캠프의 방식이다.

## 커리큘럼

| Day | Skill | 주제 |
|-----|-------|------|
| 1 | `day1-setup-and-data` | 기본 개념(CLAUDE.md/Memory/Skill) + CSV 전처리 실습 + 스킬 만들기 |
| 2 | `day2-review-and-features` | Day 1 퀴즈 복습 + 새 데이터로 실습 복습 + MCP, Hook, Plugin |
| 3 | `day3-mcp-deep-dive` | MCP 딥다이브 + Context Sync 스킬 구축 |
| 4 | `day4-clarify-and-github` | Clarify 플러그인 활용 + 나만의 스킬 만들기 + PRD & GitHub |
| 5 | `day5-agent-and-orchestration` | Subagent + Agent Teams + 멀티에이전트 패턴 + 세션 분석 + 콘텐츠 소화 |

## 샘플 데이터

Day 1 실습에 사용하는 패션 플랫폼 샘플 데이터:

| 파일 | 내용 |
|------|------|
| `data/products.csv` | 상품 마스터 (SKU, 브랜드, 카테고리, 가격, 재고, 시즌) |
| `data/sales.csv` | 일별 매출 (주문일, 수량, 매출, 반품, 채널) |
| `data/brands.csv` | 입점 브랜드 관리 (수수료율, 계약기간, 담당자) |

> 의도적으로 데이터 품질 이슈(날짜 형식 불일치, 카테고리명 불통일, 중복 등)가 포함되어 있습니다. 전처리 실습용입니다.

## 캠프가 끝나면

수료가 아니라 시작이다. Claude Code라는 불을 다루는 신인류 커뮤니티의 일원이 된다.
