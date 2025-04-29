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

- 추후 GitHub 협업에서 상세히 알아보자.

# GitHub

## 1. GitHub 회원가입하기

- https://github.com

## 2. GitHub 프로젝트 (Repository) 생성하기

- 만약 til_git 프로젝트를 생성했다면 GitHub 에도 생성하자.
- public 으로 셋팅 : 외부로 소스 공개
- description 을 작성하자 : 프로젝트 설명

## 3. GitHub 인증하기

### 3.1. 무조건 GitHub에 로그인된 상태로 시도

### 3.2. '윈도우 > 자격 증명 관리자 > Windows 자격 증명` 에서 GitHub 확인

- 새로 생성하길 권장함
- PC 정리 또는 자리 이동 시 반드시 삭제해야 함

## 4. GitHub 프로젝트 연결하기

### 4.1. 원격 저장소 주소 지정하기

- `remote` : 원격(인터넷) 을 말함
- `add` : 추가하기
- `origin`
  - http 주소를 간략하게 별칭을 준 것
  - 단어는 마음대로 해도 됨
  - `원격 이름`이라고 함

```bash
git remote add origin https://github.com/아이디/repository이름.git
```

### 4.2. 원격 저장소 목록 보기

```bash
git remote -v
```

### 4.3. 원격 저장소에 소스 등록하기

- 습관적으로 하면 좋은 작업

```bash
git add .
git commit -m "[docs] : 최초등록"
```

- 소스 업로드 = push 라고 함

```bash
git push -u origin main
```

- `-u` 옵션을 붙였다면 이후로는 `git push` 만 하면 됨.

### 4.4. 원격 저장소 관리하기

- 목록 보기

```bash
git remote -v
```

- 삭제하기

```bash
git remote remove 원격이름
```

- 추가하기

```bash
git remote add 원격이름 https주소
```

- 이름 바꾸기

```bash
git remote rename 옛이름 새이름
```

### 4.5. 추천 작업 순서

```bash
git add .
git commit -m "메모 내용"
git push origin main
```

## 5. GitHub의 소스를 복사(clone)해서 작업하는 법

- 깃허브 주소를 주의하기
- https 로 진행중이므로 `https` 기준
- 기준이 `ssh`면 인증을 다시 해야함

### 5.1. 실습

- ex) 서울로 출장을 갔다. (PC없이) 서울 사무소에서 PC를 지금 받았다.
- PC에 환경 설정 진행 (VSCode, Git)
- student/`test` 폴더 생성
- GitHub 사이트의 프로젝트를 `clone` 한다.
- GitHub 사이트에 Repository 를 clone 한다.

### 5.2. clone

```bash
git clone 주소 .
```

- . 찍어서 하면 폴더 안에 있는 것들이 clone (없으면 폴더째로)

### 5.3. clone 이후의 작업

```bash
git status
```

```bash
git branch -v
```

```bash
git branch 새이름
git switch 새이름
```

```bash
git add .
git commit -m "작업내용"
```

```bash
git push origin 새이름
```

### 5.4. git push 이후 작업

- jeju 폴더는 clone 을 하여 진행함.
- `til_git 폴더는 clone 을 할 필요가 있을까요?`
  - til_git 폴더는 이미 git 셋팅이 되어 있다. 그래서 clone 은 필요 없다.

### 5.5. 기존 프로젝트에서 GitHub 브랜치 적용하기(단계)

- 기존 프로젝트에서는 clone 하지 않고 fetch를 사용함
- 1. fetch 는 GitHub에서 모든 브랜치 가져옮

```bash
git fetch --all
```

- 2. 브랜치 목록 보기(로컬, GitHub 포함 전체)

```bash
git branch -a
```

- git fetch --all 해야 가져와서 볼 수 있음

- 3. `새롭게 작업한 GitHub 브랜치`를 `로컬 브랜치로 생성 > 즉시 작업` 하기

```bash
git switch --track -c 생성브랜치명 원격브랜치명
```

- ex) `git switch --track -c jeju remote/origin/seoul`
  - git branch -a 를 해야 원격브랜치명을 알 수 있어 적용 가능

## 6. GitHub 브랜치 삭제하기

- GitHub의 브랜치 모두 내려받기

```bash
git fetch --all
```

- 로컬 및 GitHub 브랜치 목록 모두 보기

```bash
git branch -a
```

- GitHub의 브랜치 삭제하기

```bash
git push 저장소이름 --delete 브랜치이름
```

- ex) `git push origin --delete remotes/origin/jeju`

## 7. 가능하면 브랜치는 삭제하지 않기 권장

## 8. 가능하면 commit의 내용은 삭제 및 수정하지 않기 권장
