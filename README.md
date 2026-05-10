# Git & GitHub 실습 프로젝트

이 프로젝트는 Git과 GitHub의 기본 개념과 실무 워크플로우를 학습하기 위한 실습 프로젝트입니다.

## 프로젝트 개요

- **목적**: Git 버전 관리와 GitHub 협업 워크플로우 습득
- **주요 학습 내용**:
  - Git 기본 명령어 (commit, push, pull, branch 등)
  - GitHub 기반 협업 (Pull Request, Code Review 등)
  - Git 커밋 컨벤션 준수
  - GitHub 이슈 및 프로젝트 관리

## 프로젝트 구조

```
.
├── README.md                      # 프로젝트 문서
├── CLAUDE.md                      # 프로젝트 작업 규칙
├── doc/
│   └── COMMIT_CONVENTION.md       # Git 커밋 메시지 컨벤션
└── .mcp.json                      # MCP 서버 설정 (로컬)
```

## 커밋 컨벤션

이 프로젝트는 **Conventional Commits** 스타일을 따릅니다.

### 커밋 메시지 형식
```
<type>(<scope>): <subject>

<body>

<footer>
```

### Type 종류
- `feat`: 새로운 기능 추가
- `fix`: 버그 수정
- `docs`: 문서 수정
- `style`: 코드 스타일 수정
- `refactor`: 코드 리팩토링
- `test`: 테스트 추가 또는 수정
- `chore`: 빌드, 의존성 등 기타 변경

### 커밋 메시지 작성 규칙
- **언어**: 한글 사용
- **Subject 길이**: 50자 이내
- **명령형**: "add" (added 아님)
- **첫 글자**: 소문자
- **마침표**: 사용하지 않음

### 예시
```
feat(auth): 로그인 기능 추가

사용자 인증을 위한 로그인 기능을 구현했습니다.
JWT 토큰 생성 및 localStorage 저장 기능 포함.

Fixes #45
```

## 학습 목표

- Git 저장소 생성 및 관리
- 커밋 히스토리 작성 및 관리
- 브랜치 생성 및 병합
- GitHub Pull Request 워크플로우
- 코드 리뷰 및 협업

## 시작하기

### 저장소 클론
```bash
git clone https://github.com/ltw070/git_agent.git
cd git_agent
```

### 브랜치 생성 및 작업
```bash
# 새 브랜치 생성
git checkout -b feature/your-feature-name

# 파일 수정 및 스테이징
git add .

# 커밋
git commit -m "feat(scope): 기능 설명"

# 원격 저장소에 푸시
git push origin feature/your-feature-name
```

### Pull Request 생성
1. GitHub 저장소에서 "New Pull Request" 클릭
2. 작업 브랜치를 메인 브랜치로 머지하도록 설정
3. PR 제목과 설명 작성
4. "Create Pull Request" 클릭

## 참고 자료

- [Git 공식 문서](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com)
- [Conventional Commits](https://www.conventionalcommits.org/ko/)
