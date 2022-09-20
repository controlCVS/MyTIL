# MyTIL

0.1% 나아지는 나를 위해

## 2022-09-13 Tue

### RPA과정 1기 웹프로그래밍 기획과 기본

### GitBash(Linux) 명령어들

- `pwd` = print working directory 현재 작업중인 경로를 출력해줌
- `cd` = change directory 뒤에 입력하는 경로로 변경함 절대경로는'/'로 시작, 상위경로는'..', tap키로 자동완성
- `ls` = 현재 폴더에 존재하는 것들을 보여줌 option< -a 숨김파일 보임, -l 자세한 옵션 보여줌 >
- `mkdir` = 현재 폴더에 뒤에 입력하는 이름을 가진 하위 폴더 생성
- `rmdir` = 뒤에 작성하는 이름을 가진 폴더 삭제
- `history` = 입력했던 명령어들을 리스트로 보여줌, `!123` 으로 복구 가능 123번째 입력을 복사 가능
- `rm` = 뒤에 입력한 문자와 같은 이름의 파일 삭제

### vim 사용법

- vim 파일이름 으로 vim에디터에서 파일을 열 수 있음, 파일이 없다면 새로 생성함
- 명령 모드와 입력 모드
- 최초 vim 진입 시 명령 모드임, 명령 모드에서는 입력이 불가능하고 입력 모드로 전환해야 입력 가능
- 입력 모드로 진입하고 싶다면 `i`버튼을 눌러야함. 한글'ㅑ'는 인식 못하므로 한영키 확인 필수  
  입력이 완료된다면 `ESC`버튼으로 다시 명령 모드로 변환함
- 입력모드에서 사용 가능한 명령어  
  `:w`= 저장하기 `:q` = 나가기 `:wq` = 저장하고 나가기

### 마크다운 링크 문법

- 다음 링크를 참조 : [링크](https://gist.github.com/ihoneymon/652be052a0727ad59601)
- `[링크](https://gist.github.com/ihoneymon/652be052a0727ad59601)` 의 형식

### E325:ATTENTION 에러 발생 원인과 대처

#### 원인

1. 다른 사람이 그 파일을 사용하면 중복 사용으로 에러가 발생
2. 파일 크래쉬가 발생(비정상적 종료로 데이터 미저장)

#### 해결방법

1. 다른사람이 사용하는 파일 종료 혹은 내 컴퓨터에서 실행중이면 종료하고 다시 실행
2. 파일을 실행시키고 `recover` or `R`을 입력 > `ls -a`로 숨겨진 swp파일을 찾고 삭제

#### 버전 관리 시스템과 git

##### 버전 관리 시스템을 사용하는 이유

    1. 실행 취소, 재 실행이 가능함
    2. 버전간 소스코드 비교가 가능함
    3. 협업이 쉬워짐

##### 다양한 버전관리 방법

- 이름 변경하기 등의 방법이 있는데, 개발할 때는 git을 주로 사용함

#### 커밋

1. 커밋은 논리적 변경이 있을 때 만듦
2. 가능하면 커밋 크기가 작을수록 좋음

#### 커밋 이력 보기

`git log`

#### 리포지토리

- 정의 : 여러 파일을 하나로 모은 컬랙션
- 하나의 리포지토리를 모노-리포지토리 라고 부름

## 2022-09-20 Tue

#### 버전 되돌리기

- git bash에서 `git checkout commitnumber`로 commitnumber 버전으로 변경 가능
- 인터넷(Html)로 실행되는 것이라면 `강력 새로고침` 실행 후 진행

#### 로컬(GitBash)에서 repository 지정 및 취소

- `git init` = 현재 작업 폴더를 repository로 지정, .git 폴더가 생성됨
- `rm -r` = recrusive, 예하의 폴더를 지움
- `rm -f` = force, 권한을 강제로 주어 삭제
- `rm -rf` = .git 폴더 삭제, 저장소 해제, 저장소가 많으면 컴퓨터 부하발생

#### gitignore(gitignore.io)

- 코드파일 외 불필요한 파일, 패키지 등을 올리지 않도록 예외처리를 하는 코드 생성
- 운영체제, 편집기에서 나오는 옵션 파일들을 제외하고 git에 올릴 수 있도록 만들어줌

#### branch 만들기

- 이슈 하나당 브랜치 하나를 주로 만듬
- `git branch` = 현재 브랜치 확인
- `git branch 브랜치 이름` = 브랜치 이름에 해당되는 브랜치 생성
- `git checkout(switch) 브랜치 이름` = 브랜치 이름에 해당되는 브랜치로 이동
