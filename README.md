# sonmat (손맛) for Gemini CLI

> 엄마가 하면 맛있던데 왜 내가 하면...?

범용 자율 루프 확장 for Gemini CLI.
[Claude Code 버전](https://github.com/jun0-ds/sonmat)의 Gemini CLI 포팅.

## 설치

```bash
# ~/.gemini/extensions/ 에 클론
git clone https://github.com/jun0-ds/sonmat-gemini.git ~/.gemini/extensions/sonmat
```

## 특징

- **System 1/2 이중 프로세스** — 빠른 판단(스킬)과 깊은 분석(워커)을 상황에 따라 자동 전환
- **범용 루프 엔진** — 개발, ML/DL, 데이터 분석, 문서, 글쓰기 등 도메인별 자율 반복
- **경량 규율 주입** — core.md + 도메인 규율이 워커에 실제로 전달됨

## 구조

```
sonmat-gemini/
├── gemini-extension.json
├── skills/
│   ├── loop/        # 범용 자율 루프 프로토콜
│   ├── guard/       # 가드레일 (커밋 전 검증, 스코프 체크)
│   ├── plan/        # 마일스톤/페이즈 관리 (progress.md)
│   ├── benchmark/   # 비교실험 프레임워크
│   └── discipline/  # 도메인별 규율 파일
├── agents/
│   └── sonmat-worker.md
└── hooks/
```

## 사용법

설치 후 Gemini CLI를 시작하면 `contextFileName`으로 지정된 GEMINI.md를 통해 규율이 로드됩니다.

> **Note**: Gemini CLI는 현재 공식 훅 시스템이 없습니다. 도메인 자동 감지는 `hooks/session-start.sh`를 수동 실행하거나 셸 alias로 연결하세요. 자세한 내용은 `hooks/README.md` 참조.

## 라이선스

MIT
