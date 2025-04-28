# Git

## 1. Git 프로그램 설치

- 프로그램 다운로드 : https://git-scm.com/
- 64-bit Git for Windows Setup.

## 2. Git 버전 확인

- 윈도우 키보드 + R 키보드 : `cmd`

```
git -version
```

- 출력창 확인

## 3. VSCode에 Git 설정하기

### 3.1 터미널 환경을 git bash 로 설정하기

- 윈도우, 맥, 리눅스 의 명령창을 통일하기 위함.
- manage(관리) > settings(설정) 선택
- 설정 화면 > `default:Windows` 입력
- `Git Bash` 선택
- 설정화면 닫고 VSCode 재실행 추천

### 3.2 VSCode 에서 Git 옵션 설정하기

- 터미널 실행 : `ctrl+백틱`

```bash
git --version
```

- 기본 브랜치명을 `main` 으로 설정

```bash
git config --global init.default main
```

- 윈도우, 맥, 리눅스 환경에서 Enter 키 처리를 통일함.

```bash
git config --global core.autocrlf true
```

- git commit 명령을 VSCode에서 작성하도록 설정

```bash
git config --global core.editor "code --wait"
```

-깃 사용자 아이디 저장

```bash
git config --global user.name "아이디"
```

-깃 사용자 아이디, 이메일 확인

```bash
git config --global user.name
```

-깃 사용자 이메일 저장

```bash
git config --global user.email "이메일"
```

-깃 사용자 이메일 확인

```bash
git config --global user.email
```

## 4. Git 작업하기(실습)

### 4.1. git 프로젝트 관리 초기화 하기

```bash
git init
```

### 4.2. git 현재 상태 파악

```bash
git status
```

### 4.3 git 현재 수정된 내용,파일, 폴더 등을 저장

- 원하는 파일만 저장하기

```bash
git add README.md
```

- 모든 파일 저장하기

```bash
git add .
```

### 4.4 수적 내역 메모 남기기

```bash
git commit -m "한줄메모"
```

# GitHub
