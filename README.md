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

### 4.4 수정 내역 메모 남기기

- 한줄 작업 메모

```bash
git commit -m "깃 작업 관련 설명글 작성"
```

- 여러 줄 메모 작성하기 (제목, 상세내용)

```bash
git commit
```

### 4.5. commit 내용 컨벤션 알아보기

```bash
[커밋타입] : 커밋 메세지(옵션)
```

- 커밋타입 : 작업의 분류
- 옵션 : 이슈 또는 수정이 된 작업커밋 번호 또는 추가 정보
- 커밋 메세지 : 무엇을 했는지 짧은 내용으로

#### 4.5.1 커밋타입

- `[feat]` : 새로운 기능 추가
- `[fix]` : 버그 수정
- `[docs]` : 문서 수정(README.md)
- `[style]` : 코드의 스타일 변경(띄워쓰기, 세미콜론 등)
- `[refector]` : 코드 리펙토링(기능 변경 말고 코드 정리 등)
- `[test]` : 테스트 코드 추가
- `[chore]` : 기타(빌드 설정, 패키지 업데이트 등)

#### 4.5.2 옵션

- 만약 '회원가입 로그인 기능 추가' 라면
- 아래는 이슈 #23 번을 해결하고 기능을 추가했다는 예시

```
[feat] : 회원가입 로그인 기능 추가(#23)
```

#### 4.5.3 커밋 내용

- Enter 키를 기준으로 제목과 내용을 구분함

```
[docs] : 커밋 제목

커밋 상세 내용 작성
```

### 4.6 커밋 내용 확인

- 기존의 commit 된 내용을 확인 -상세보기

```bash
git log
```

-간략하게 보기

```bash
git log --oneline
```

- 특정 commit 상세 보기

```bash
git show 커밋 아이디
```

#### 4.6.1 각 항목 관련 사항 이해하기

- commit : 고유한 커밋 번호(아이디)
- Author : 작성자
- Date : 날짜
- 메세지 : 상세 내용

### 4.7 브랜치 작업해보기

- `나뭇가지` 라는 의미로 원 줄기로부터 파생되는 것
- 원 `소스`로부터 파생한 새롭게 `분기한 소스` 관리
- 브랜치 생성시에는 add와 commit이 완료되어야 함

#### 4.7.1. 브랜치 생성하기

```bash
git add .
git commit -m "[docs] : 브랜치 실습 test 생성하기"
git branch test
```

#### 4.7.2 브랜치 목록 보기

```bash
git branch -v
```

#### 4.7.3. 브랜치 이동하기

```bash
git switch test
```

#### 4.7.4. 브랜치 삭제하기

```bash
git branch -d test
```

#### 4.7.5. 브랜치 합치기

- 브랜치를 하나로 합쳐주기
- 주의사항 : `main에서 test를 합치기`

```bash
git merge 합쳐주고자 하는 브랜치명
```

### 4.8 git 브랜치 충돌 해결해 보기

- 깃 브랜치를 merge 하면 많이 발생함
- `login 브랜치`에서 로그인 기능을 구현함

# GitHub
