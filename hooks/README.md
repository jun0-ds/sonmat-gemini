# Hooks

Gemini CLI는 현재 공식 훅 시스템을 제공하지 않습니다.
`session-start.sh`는 수동 실행 또는 셸 프로파일에서 호출할 수 있습니다.

```bash
# ~/.bashrc 또는 ~/.zshrc에 추가 (선택)
# gemini 시작 전 도메인 감지
alias gemini-sonmat='eval "$(~/.gemini/extensions/sonmat/hooks/session-start.sh)" && gemini'
```
