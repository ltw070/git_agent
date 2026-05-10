# Git과 Github 실습

이 프로젝트에서는 Git과 Github에 대한 실습을 진행합니다.

## 사용 파일

README.md 파일만 사용합니다.

## Claude Code 작업 우선순위

### 로컬 환경 우선 확인
- 새로운 작업을 시작하기 전에 로컬 계정, 로컬 토큰, 로컬 설정을 먼저 확인하세요
- 기본/전역 계정 사용 전에 로컬 자격증명 존재 여부를 확인하세요
- `.mcp.json`, `.env`, `~/.ssh/config`, 프로젝트 설정 파일 등 로컬 설정을 우선적으로 읽으세요
- 로컬 설정이 없을 때만 기본/전역 계정을 사용하세요

## GitHub 접근 규칙

### MCP를 우선으로 사용
- GitHub 관련 작업 (리포지토리 생성, 파일 업로드, PR 생성 등)은 **MCP(github-general)를 우선으로 사용**합니다.
- SSH나 HTTP를 통한 직접 연결은 보조 수단으로만 사용합니다.
- MCP 도구:
  - `mcp__github-general__create_repository`: 리포지토리 생성
  - `mcp__github-general__create_or_update_file`: 파일 생성/수정
  - `mcp__github-general__create_pull_request`: PR 생성
  - `mcp__github-general__push_files`: 다중 파일 업로드

## Git Commit Rule

Git Commit 시 @doc/COMMIT_CONVENTION.md 파일을 참고하여 커밋 메시지를 작성합니다.
- Type, Scope, Subject 형식을 따릅니다.
- Commit Message는 한글을 사용합니다.
- Subject는 50자 이내로 작성합니다.
