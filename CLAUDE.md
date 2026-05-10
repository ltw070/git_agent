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

### 작업 규모별 방식 선택

#### MCP 사용 (토큰 효율적)
- **작은 파일 변경**: < 5KB 파일 생성/수정
- **단일 파일 변경**: 한 번에 1-2개 파일
- **API 작업**: 리포지토리 생성, PR 생성, 이슈 관리
- 도구:
  - `mcp__github-general__create_repository`: 리포지토리 생성
  - `mcp__github-general__create_or_update_file`: 파일 생성/수정 (< 5KB)
  - `mcp__github-general__create_pull_request`: PR 생성
  - `mcp__github-general__push_files`: 소수 파일 업로드

#### Bash + Git 사용 (토큰 절약)
- **큰 파일 변경**: > 10KB 파일 수정
- **대량 파일 변경**: 3개 이상 파일 동시 변경
- **로컬 완성 후 일괄 푸시**: 복잡한 변경사항
- 방식:
  ```bash
  git add .
  git commit -m "type(scope): 메시지"
  git push origin branch
  ```

### 토큰 절약 이유
- MCP: 전체 파일 내용 전송 (100KB = ~25,000 토큰)
- Bash: diff만 전송 (100KB 변경 = ~500 토큰) ← **50배 절약**

## Git Commit Rule

Git Commit 시 @doc/COMMIT_CONVENTION.md 파일을 참고하여 커밋 메시지를 작성합니다.
- Type, Scope, Subject 형식을 따릅니다.
- Commit Message는 한글을 사용합니다.
- Subject는 50자 이내로 작성합니다.
