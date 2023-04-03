# 3주차 GitHub 심화
- 노션 링크 : https://dramatic-elbow-87e.notion.site/3-GitHub-10436461f27a4353a8a4c2225ef02e43
## 1. branch(분기)

- branch의 실체는 포인터이다.
- 정의 : 가장 마지막 commit을 가리키는 포인터
- *가 붙어있는 브랜치가 현재 활성화된 브랜치이다.

### 1) branch 생성

```powershell
git branch testing
#새로운 브랜치를 만드는 코드
#testing 이라는 브랜치를 만든다
```

> 브랜치를 생성하는 명령어는 `git branch`이며 첫번째 매개변수는 생성하려는 브랜치명이고 
두번째는 분기해 나올 브랜치명이다.
> 
- 다른 예시
    
    ```powershell
    git branch RB_1.0 master
    ```
    
    > 위의 코드는 master branch에서 RB_1.0 이라는 브랜치를 생성한다.
    > 

```powershell
git checkout testing
#checkout : 원하는 브랜치로 넘어가는 것
#testing branch로 넘어간다.
```

### 2) branch 삭제

**git branch -D (브랜치)**

로컬 브랜치를 삭제하려면 아래 명령어를 사용한다.

```powershell
git branch -D #브랜치명
```

## **브랜치명 변경하기**

**git branch -m [브랜치명] [새로운 브랜치명]**

마스터 브랜치명을 바꾸려면 다음과 같이 한다.

```
git branch -m master master2
```

## **브랜치 생성과 체크아웃**

**git checkout -b (새로운 브랜치)**

브랜치 생성과 체크아웃을 한번에 하려면 `git checkout -b (branch이름)`을 입력한다.

```powershell
git checkout -b utility
#Switched to a new branch 'utility'
```

새로운 브랜치가 생성되고 생성된 새로운 브랜치로 체크아웃된다.

- ※ git 2.23버전 부터 git checkout을 대신하여 switch와 restore가 나오게 되었다.
    
    checkout의 기능이 너무 많아 분리하였다고 볼 수 있다.
    
    - checkout: Switch branches or restore working tree files
    
    - switch: Switch branches 
    
    - restore: Restore working tree files
    
    ```powershell
    #기본 명령어
    git switch[브랜치명]
    #브랜치를 만들면서 브랜치 변경하는 명령어도 변경 되었다.
    git switch -c [브랜치명]
    #원격 브랜치와 같은 이름으로 로컬 브랜치를 생성하고 스위치 할 수 있다.
    git switch -t orogin/[원격브랜치명]
    ```
    

## **브랜치 관리**

### **현재 브랜치 확인하기**

**git branch**

**git branch -v**

현재 등록된 브랜치를 확인할려면 아래와 같이 한다.

```powershell
git branch
#*master
#gh-pages

```

등록된 브랜치의 상세한 정보를 볼려면 아래와 같이 한다.

```powershell
git branch -v
#* gh-pages e7f33f9 update html files
#master   5c7085b Merge branch 'master' of github.com:mylko72/BalladBest

```

### **브랜치 상태 확인**

현재 Checkout한 브랜치를 기준으로 `--merged`와 `--no-merged` 옵션을 사용하여 Merge된 브랜치인지 그렇지 않은지 필터링해 볼 수 있다.

- **-merged 옵션**

이미 Merge한 브랜치 목록을 확인한다.

```
 git branch --merged
 #iss53
#*master

```

iss53 브랜치는 Merge한 브랜치로 목록에 나타난다. 또 * 기호가 붙어있지 않으므로 `git branch -d` 명령으로 삭제해도 되는 브랜치다.

- **-no-merged 옵션**

반대로 현재 Checkout한 브랜치에 Merge하지 않은 브랜치를 살펴본다.

```
git branch --no-merged
testing

```

Merge 하지 않은 커밋을 담고 있는 브랜치는 `git branch -d` 명령으로 삭제되지 않는다. Merge하지 않은 브랜치를 강제로 삭제하려면 `-D` 옵션으로 삭제한다.

[branch를 원격 repository에 push 하기](https://www.notion.so/branch-repository-push-5678f723748e40868635013b2aea1a5f)

## 2. HEAD & master

모든 브랜치에는 HEAD 값이 존재하는데 HEAD란 해당 브랜치의 마지막 commit을 의미한다.
따라서, HEAD가 특정 commit에 찍혀 있는 경우 해당 브랜치의 마지막 commit이라는 것을 알 수 있다.
즉, HEAD는 특정 브랜치의 마지막 commit에 대한 포인터이다.

<aside>
📌 HEAD는 현재 checkout된 commit으로 **현재 작업중인 commit**을 가리킨다.

</aside>

[Branch를 시각화해서 이해해보자!](https://www.notion.so/Branch-7619c49702d6441fa0bbe63004909a8a)

## 3. Merge

main branch가 있고 새로운 branch를 만드는데

변화라는 건 기준이 있다. 기준은 공통 조상. 공통 조상을 기준으로 변화를 확인할 수 있다.

3-ways merge 전략.

### merge하는 방법

```powershell
git merge <commit>
```

위의 코드를 실행하면 HEAD가 가리키고 있던 commit에 지정한 커밋 내용이 merge된다.

## 4. conflict

merge 상황에서 충돌이 발생하는 경우가 있다. 이는 자동 병합에 실패한 경우이다.
각각의 브랜치에서 변경한 내용이 같은 파일의 같은 부분에서 수정된 것이라면 충돌이 일어난 부분은 일일이 수정해야한다. 
수정후 다시 merge하면 된다.

## 6. git commit 메시지 컨벤션

`Udacity Style`의 커밋 메시지 구조는 다음과 같이 생겼다.

```powershell
type: Subject

Body

Footer
```

Subject, Body, Footer에 들어가는 내용을 하나하나 살펴보자.

### Title

커밋 메시지 Title은 `docs: Update README.md`처럼 작성한다.`docs`는 type, `Update README.md`는 Subject이다.

### Subject

Subject는 크게 4가지의 특징을 가진다.

- 길이는 50자 이하로 작성한다.
- 동사원형(ex. Add, Update, Modify)로 시작한다.
- 첫 글자는 대문자이다.
- 끝에는 마침표를 붙이지 않는다.

### Type

Type은 크게 7가지가 있다.

- feat: 새로운 기능 추가
- fix: 버그 수정
- docs: 문서 수정
- style: 코드 포맷 변경, 세미콜론 누락, 코드 변경 없음
- refactor: 프로덕션 코드 리팩터링
- test: 테스트 추가, 테스트 코드 리팩터링, 프로덕션 코드 변경 없음
- chore: 빌드 테스크 업데이트, 패키지 매니저 환경설정, 프로덕션 코드 변경 없음

### Body

커밋 메시지는 대부분 Title만 읽어도 내용을 파악할 수 있다.따라서, Body는 선택사항으로 커밋 메시지에 부가적인 설명이 필요할 때 작성한다.

Body는 크게 3가지의 특징을 가진다.

- 길이는 72자 이하로 작성한다.
- Title과 Body 사이에는 한 줄의 공백을 추가한다.
- 커밋 메시지의 `What`과 `Why`에 대해 작성한다. `How`는 고려하지 않는다.

### Footer

Footer 역시 선택사항이다.해결한 이슈 커밋의 ID, 해결하기 위해 참고한 커밋의 ID 등을 작성한다.

[github message convention](https://velog.io/@archivvonjang/Git-Commit-Message-Convention) → 클릭하면 좀더 자세한 설명을 볼 수 있다.

[3주차 실습](https://www.notion.so/3-d69ec3e5129940c5ae34bfeb88965b1b)


# 실습 내용

# 1. Git Fork

오픈 소스 프로젝트를 공부하거나 Contributors가 되고 싶을 때, 해당 원격 저장소(Remote Repository)를 자신의 원격 저장소로 복사할 수 있다. 이를 Fork라 한다. 깃허브의 경우 공개된 모든 자료가 오픈 소스로 다른 사람의 자료를 Fork 할 수 있다. 즉, fork는 다른 계정의 원격 저장소를 내 계정으로 가지고 올 때 사용한다.

![스크린샷 2023-04-03 오후 12.28.44.png](/Users/bangbyeonghun/Desktop)

여기서 우측 상단의 Fork 버튼을 누르고 본인의 리포지토리에 추가하면 된다.

# 2. Git clone

앞서 노션 페이지에 [정리해놓은 글](https://www.notion.so/9b195d5cd3a04ad8810deba4a5b39871)을 참고하면 된다.

```powershell
git clone https://github.com/BangProx/webstudy-homework-BangProx.git
```

> 위의 코드를 통해 clone을 완료했다.
> 

# 3. git branch 생성하기

git branch를 master 브랜치에서 생성을 했다

```powershell
git branch BangProx
git switch Bangprox
```

> master 브랜치에 BangProx라는 브랜치를 새로 생성하였고 `switch` 를 이용해서 BangProx 브랜치로  이동하였다.
> 

# 4. 새로 만든 브랜치에 push 하기

```powershell
git push origin BangProx
```

![스크린샷 2023-04-03 오후 4.08.19.png](/Users/bangbyeonghun/Desktop)

> 근데 아차차 BangProx 파일을 add하고 commit하는걸 깜빡했다 ㅎㅎ. 다시 해보자
> 

![스크린샷 2023-04-03 오후 4.14.19.png](/Users/bangbyeonghun/Desktop)

> 위와 같이 문제 없이 push되는 것을 확인할 수 있다.
> 

# 5. Pull request 보내기

이제 github에 내가 clone한 리포지토리에 들어가서 pull request를 보내면 된다. 
Pull request를 하는 방법은 화면 상단의 Code 오른쪽에 있는 pull request 버튼을 누르면 된다.

![스크린샷 2023-04-03 오후 4.19.05.png](/Users/bangbyeonghun/Desktop)

> 이 화면의 상단을 보면 BangProx/web… 리포지토리의 BangProx 브랜치에서 binary-ho/web… 
리포지토리의 master 브랜치로 pull request를 보내는것을 알 수 있다.
> 

# 끝!