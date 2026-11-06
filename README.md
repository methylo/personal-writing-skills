# 나만의 글쓰기 (personal-writing-skills)

경험과 메모로 칼럼 한 편을 완성하는 글쓰기 스킬 두 개입니다. 메인 스킬 **나만의 글쓰기**(`write-personal`)가 설계부터 최종 점검까지 단계를 이끌고, 정본 스킬 **내 글 정본**(`write-standard`)이 필자의 문체·표현 기준을 맡습니다. 두 스킬을 함께 등록해야 합니다.

**ChatGPT용**(강의에서 쓴 원본)과 **Claude용**(변환본) 두 가지를 제공합니다. 쓰는 서비스에 맞는 폴더를 고르세요.

## 두 스킬의 관계

| 스킬 | 호출 이름 | 맡는 일 |
|---|---|---|
| 나만의 글쓰기 | `write-personal` | 메모 → 설계·독자 추천 → 구성 → 초안 → 독자·편집자 검토 → 수정 → 최종 점검. 사실·근거·구성·분량을 관리합니다. |
| 내 글 정본 | `write-standard` | 문체, AI 흔적 지우기, 표현·표기 사전, 자기 표현 방식, 내 기준 칸. 메인 스킬이 3단계 초안부터 6단계 최종 점검까지 읽어 적용합니다. |

기본값은 대학교 신문 칼럼, 20대 대학생 독자, 공백 포함 900~1,000자입니다. 요청에 매체·독자·분량을 적으면 그 글에만 바꿔 적용합니다.

## 구성

```text
personal-writing-skills/
├── chatgpt/                       ChatGPT용 (강의 원본)
│   ├── skills/
│   │   ├── write-personal/        SKILL.md · agents/openai.yaml · assets/icon.svg · references/ 5개
│   │   └── write-standard/        SKILL.md · agents/openai.yaml · assets/icon.svg
│   └── downloads/                 업로드용 zip 2개
└── claude/                        Claude용 (변환본)
    ├── skills/
    │   ├── write-personal/        SKILL.md · references/ 5개
    │   └── write-standard/        SKILL.md
    └── downloads/                 업로드용 zip 2개
```

`write-personal/references/`에는 메모 작성 안내(01), 단계별 출력 견본(02), 칼럼 구조 견본(03), 새 대화 이어 가기·제출 전 안전 수칙(04), 초보자 수정 도움(05)이 들어 있습니다.

## ChatGPT에 등록하기

1. 아래 zip 두 개를 내려받습니다.
   - [write-personal.zip](./chatgpt/downloads/write-personal.zip?raw=1)
   - [write-standard.zip](./chatgpt/downloads/write-standard.zip?raw=1)
2. ChatGPT의 스킬 등록 화면에서 두 파일을 하나씩 올립니다.

원고는 ChatGPT의 글쓰기 블록으로 나옵니다. 등록 화면의 위치와 명칭은 ChatGPT 버전과 요금제에 따라 다를 수 있습니다.

## Claude에 등록하기

- **Claude 앱(claude.ai·데스크톱)**: 아래 zip 두 개를 내려받아 설정 → 기능(Capabilities) → 스킬(Skills)에서 하나씩 업로드합니다.
  - [write-personal.zip](./claude/downloads/write-personal.zip?raw=1)
  - [write-standard.zip](./claude/downloads/write-standard.zip?raw=1)
- **Claude Code**: `claude/skills/` 안의 두 폴더를 `~/.claude/skills/`에 복사합니다.

Team·Enterprise 요금제는 관리자가 스킬 기능을 켜야 등록할 수 있습니다.

### ChatGPT용과 달라진 점

| 항목 | ChatGPT용 | Claude용 |
|---|---|---|
| 원고 형식 | 글쓰기 블록(`:::writing`) | `원고 · 3단계 초안` 이름표 아래 구분선(`---`) 사이에 제목·본문 |
| 정본 찾기 | 개인 스킬 폴더 규칙으로 찾음 | 스킬 목록에서 `write-standard`를 찾음 |
| 부가 파일 | `agents/openai.yaml`, `assets/icon.svg` | 없음 (Claude는 쓰지 않음) |
| 문서 정리 | 원본 그대로 | 지난 버전 문구 삭제, '최종 점검'으로 용어 통일, 여러 파일에 반복된 정본 설명 규칙을 SKILL.md 한 곳으로 모음 |

단계, 기본값, 정본 기준, 견본 내용은 두 버전이 같습니다.

## 사용 방법

```
나만의 글쓰기 스킬로 아래 경험과 메모를 글로 정리해줘.

[내 경험과 메모]
```

단계 번호를 말하지 않아도 됩니다. 메모나 초안을 넣고 "다음", "검토해줘", "반영해줘"로 이어 갑니다. 매 단계 끝에 현재 단계와 다음 단계를 안내합니다.

## 내 기준 넣기

`write-standard/SKILL.md`의 **4. 자기 표현 방식**과 **6. 내 기준 칸**을 자기 값으로 채운 뒤 다시 업로드하면, 그때부터 쓰는 모든 글에 반영됩니다. 적용 우선순위는 6 내 기준 → 4 자기 표현 방식 → 1~3 기본 기준입니다.

## 강의 연결

2026년 11월 3일 울산대학교 「AI 글쓰기 스킬을 활용한 나만의 글쓰기」 특강의 실습 자료입니다. 강의에서는 ChatGPT용을 사용했습니다.

## 라이선스

CC BY-NC 4.0 — 출처를 밝히면 비상업적 목적으로 공유·수정할 수 있습니다. [LICENSE](./LICENSE) 참고.

© 2026 HONGS LAB (홍순성)
