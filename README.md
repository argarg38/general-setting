# general-setting

Claude Code 공통 설정 (MCP 서버 + 플러그인).

## 포함된 연결

| 이름 | 종류 | 설정 위치 |
|---|---|---|
| Supabase (공식) | 원격 MCP `https://mcp.supabase.com/mcp` | `.mcp.json` |
| Vercel (공식) | 원격 MCP `https://mcp.vercel.com` | `.mcp.json` |
| Chrome DevTools MCP | 로컬 MCP `npx chrome-devtools-mcp@latest` | `.mcp.json` |
| oh-my-claudecode | 플러그인 (`oh-my-claudecode@omc`) | `.claude/settings.json` |

## 처음 사용할 때

1. 이 레포에서 `claude` 실행 → 마켓플레이스/플러그인 설치 및 프로젝트 MCP 서버 승인 프롬프트를 수락.
2. `/mcp` 실행 → `supabase`, `vercel` 각각 **Authenticate** 선택해 브라우저 OAuth 로그인.
3. oh-my-claudecode 초기 설정: `/oh-my-claudecode:omc-setup`.
4. Chrome DevTools MCP는 Node.js 20+ 와 로컬 Chrome이 필요합니다.

### 선택 옵션

- Supabase를 특정 프로젝트·읽기 전용으로 제한하려면 URL을
  `https://mcp.supabase.com/mcp?project_ref=<프로젝트ID>&read_only=true` 로 바꾸세요.
