# Block 0: 환경 확인

> README의 Step 0에서 Git, Python, Node.js, Claude Code를 이미 설치했다.
> 이 블록에서는 설치가 제대로 되었는지 확인하고, 터미널 기본 개념을 익힌다.

> **Phase A 시작 시 반드시 아래 형태로 출력한다:**
> ```
> 📖 공식 문서: https://docs.anthropic.com/en/docs/claude-code/overview
> 📖 설치 가이드: https://docs.anthropic.com/en/docs/claude-code/getting-started
> ```

## EXPLAIN

### 터미널이 뭔가요?

터미널은 컴퓨터에게 글자로 명령을 내리는 창이다.

- **마우스로 하는 것**: 폴더 클릭 → 파일 더블클릭 → 프로그램 실행
- **터미널로 하는 것**: 명령어 입력 → Enter → 끝

지금 여러분이 Claude와 대화하고 있는 이 화면이 바로 터미널이다.

> 비유: 터미널 = 카카오톡 채팅창. 상대방(컴퓨터)에게 메시지(명령어)를 보내면 답장(결과)이 온다.

### PATH가 뭔가요?

PATH는 **프로그램의 주소록**이다.

터미널에서 `python`이라고 치면, 컴퓨터가 PATH 목록을 뒤져서 Python이 어디 설치되어 있는지 찾는다. PATH에 등록되지 않으면 "찾을 수 없습니다" 에러가 난다.

> 비유: 핸드폰 연락처에 번호를 저장해야 이름으로 전화할 수 있는 것과 같다. PATH에 등록 = 연락처에 저장.

### 설치한 도구들의 역할

| 도구 | 왜 필요한가 |
|------|------------|
| **Git** | 파일 변경 이력 관리. Claude Code가 코드를 수정할 때 "되돌리기"가 가능해진다 |
| **Python** | Claude Code가 데이터 분석, 차트 생성 등을 할 때 내부적으로 사용 |
| **Node.js** | 스킬 관리 등 Claude Code 확장 기능에 필요 |
| **Claude Code** | AI와 터미널에서 대화하면서 작업하는 도구. 오늘의 주인공 |

## EXECUTE

아래 명령어들을 Claude에게 입력해서 설치 상태를 확인한다:

```
아래 명령어들을 실행해서 설치가 잘 되었는지 확인해줘:
- git --version
- python --version
- node --version
- npm --version
```

> Claude가 각 도구의 버전을 확인하고 결과를 보여줄 것이다.
> 모든 도구에서 버전 번호가 출력되면 성공이다.
> 만약 문제가 있으면 Claude에게 "○○ 설치가 안 된 것 같아. 어떻게 해야 해?"라고 물어보면 된다.

## QUIZ

> Block 0은 퀴즈 없음. 설치 확인만 진행한다.

```json
AskUserQuestion({
  "questions": [{
    "question": "설치 확인이 모두 완료되었나요?\n\ngit, python, node, npm 버전이 모두 정상 출력되면 완료입니다.",
    "header": "설치 확인",
    "options": [
      {"label": "모두 완료!", "description": "4가지 모두 정상 동작 → Block 1로 이동"},
      {"label": "트러블슈팅 필요", "description": "설치 중 에러 발생 — Claude에게 도움 요청"}
    ],
    "multiSelect": false
  }]
})
```

> "트러블슈팅 필요" 선택 시: 에러 메시지를 물어보고, 일반적인 해결법을 안내한다.
> - PATH 문제: 터미널을 닫았다가 새로 열어보기
> - Python PATH 누락: Python 재설치 시 "Add to PATH" 체크
> - 버전이 안 나오는 도구: README Step 0을 다시 따라하기
