# 2주차 GitHub

## 1. git

- git은 소스 코드의 변화를 추적하고 협업을 지원한다
- 코드의 수많은 분기를 만들 수 있다.
- 코드의 가지들을 브랜치(branch)라고 부른다.

## 2. git의 기능

- 분기 합치기
- 변화 추적(버전 관리)
- 특정 시점으로 되돌리기

## 3. 파일의 상태

- 추적 x(UnTracked)
- 변경 x(UnModified)
- 변경 o(Modified)
- Staged

## 4. 내 컴퓨터 내부

- Working Directory(작업공간)
    - vscode 처럼 내가 코딩하는 공간
    - `add`를 통해서 staging area로 보낸다(Stage Fix)
- Staging Area
    - `commit`을 통해서 repository로 보낸다
    - `commit`을 할때 수정사항을 글로 써서 저장한다
- Repository(.git directory)
    - git에서 관리해주는 저장소

<aside>
📌 Staging Area가 존재하는 이유는 논리적으로 끊어주는 역할.
나중에 확인할 때 전에 코드 작성자가 왜 따로 commit을 했는지 알 수 있다.

</aside>

## 5. 서버

- Remote Repository
    - 서버가 관리하는 저장소( ex. github)
    - `push` 명령어를 통해서 내 컴퓨터에서 remote repository에 변화를 전송한다
    - 협업자는 `pull` ,`fetch` 를 통해 접근 할 수 있다.
    - `pull` 은 협업자의 directory에 파일이 합쳐진다.

<aside>
📌 `clone` : clone repository 는 원격 저장소를 복제한 저장소다. 이건 다른사람의 
소스코드 복사본을 생성하는 것과 같으며, 개발을 할 때 보통 클론 저장소에서 작업을
진행하게 된다. 이런 상황에 원격 저장소에 변경 사항이 생기면, 그 내용을 가져와
클론 저장소를 최신 상태로 유지해야 한다.

</aside>

<aside>
📌 `fetch` : 로컬  git에게 원경 저장소에서 최신 메타데이터 정보를 확인하라는 명령을 전달한다. 단, 원격 저장소에 변경사항이 있는지 확인만 하고, 변경된 데이터를 로컬 git에 실제로 가져오지는 않는다.
(기능을 확인하려고 있는 것, working directory에는 영향을 주지 않는다.)

</aside>

<aside>
📌 `pull` : 원격 저장소에서 변경된 메타데이터 정보를 확인할 뿐만 아니라 최신 데이터를 복사해서 로컬 git에 가져온다.

</aside>

<aside>
📌 commit message convention : 추후 반영

</aside>

## 2. 실습

```
echo "# test1" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
```

> `git init` 은 파일에 git을 초기화하는 명령어이다.
> 
> 
> `commit -m` 을 통해 커밋을 하고 커밋시에 메시지를 추가할 수 있다
> 
> `git branch -M main` 은 브랜치 이름을 main으로 지은 것이다
> 
> `git push -u origin main` 은 .git repository에 있는 로컬 파일을 github 서버에 `push` 하는 명령어
> 

## 3. 추가 과제

[spring initializr로 project 만들어보기](2%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20GitHub%20ae53ff37111f4e0fba575649294e905b/spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c.md)

# spring initializr로 project 만들어보기

### spring initializr을 이용해서 project 만들어보기

- [spring initializr](https://start.spring.io/)는 spring boot 기반으로 spring 관련 프로젝트를 생성해주는 사이트이다.

### 1) 웹페이지 접속후 프로젝트 만들기

![스크린샷 2023-03-23 오후 2.35.33.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-23_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_2.35.33.png)

1. Project : 사용할 빌드 툴 선택
2. language : 사용할 언어 선택
3. spring boot : 버전 선택
    1. snapshot : 현재 개발중인 버전
    2. M : 아직 정식 릴리즈 되지 않은 버전
    3. 아무것도 없는것: 정식 릴리즈 버전
4. Dependancy : 스프링 프로젝트에서 사용할 라이브러리
    - web project를 추가하려면 spring web을 필수로 추가해야한다.
5. Generate 클릭해서 프로젝트 생성!

### 2) zip download

프로젝트 파일을 다운로드했고, 프로젝트를 열어보려면 구글링을 해보니 [IntelliJ IDEA](https://www.jetbrains.com/ko-kr/idea/download/#section=mac) 를 다운로드해야했다.

### 3) JDK download

IntelliJ를 다운받고 이제 프로젝트를 실행하려는데 빌드가 안돼서 확인해보니까 JDK를 따로 다운받아야 했다.

![스크린샷 2023-03-23 오후 3.43.42.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-23_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_3.43.42.png)

<aside>
📌 여기서 JDK 항목을 누르면 download JDK를 해서 JDK를 다운받을 수 있다

</aside>

![스크린샷 2023-03-23 오후 3.50.45.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-23_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_3.50.45.png)

![스크린샷 2023-03-23 오후 3.50.13.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-23_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_3.50.13.png)

<aside>
📌 여기서 1차 딥빡. jdk 버전을 1.8 에서 18 사이로 하라는 말이지??

</aside>

### 1)로 다시 돌아가서 프로젝트를 다시 만들었다.

![스크린샷 2023-03-23 오후 5.11.05.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-23_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_5.11.05.png)

> java 버전이 17이네 그럼 java17을 받아야겠다고 생각해서 다운을 받으려는데
m1칩은 아직 모든 호환이 되지 않는 버전이 있어서 맞는 버전으로 다운을 받아야했다.
여기서 2차 딥빡(M1칩은 **Mac/AArch64/arm64**로 받아야한다.)
> 

> 오라클 최신버전은 유료고 adoptopenjdk에서 다운받으려니까 16까지밖에 없네?
[AZUL](https://www.azul.com/downloads/#download-openjdk) 에서 받거나 oracle에서 구버전을 받아야겠다고 생각해서  [오라클](https://jdk.java.net/archive/)에서 다운을 받았다.
> 

<aside>
📌 링크를 타고 접속을 하면 아래의 java 17버전을 확인할 수 있다.

</aside>

![스크린샷 2023-03-24 오전 2.39.23.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-24_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_2.39.23.png)

<aside>
📌 다운로드를 받은 후 jdk 파일을 java 디렉터리 안에 넣어야 한다.
아래의 코드를 통해 jdk폴더를 복사 붙여넣기 하면 된다.

</aside>

```powershell
cd /Library/Java/JavaVirtualMachines
```

### 4) jdk 설정

![스크린샷 2023-03-24 오전 2.42.10.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-24_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_2.42.10.png)

![스크린샷 2023-03-24 오전 2.44.06.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-24_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_2.44.06.png)

<aside>
📌 File>Project Structure… >platform settings > SDKs

</aside>

위의 순서로 클릭을 하면 내 컴퓨터에 깔린 jdk들을 확인할 수 있고 본인의 project에 맞는 java 버전에 맞는
jdk 를 설정해 주면 된다. Project에 맞는 java 버전은 아까 spring initializr에서 프로젝트 만들때 맨 밑의 
항목이다. 나는 17이니까 jdk도 17로 설정해줬다.

![스크린샷 2023-03-24 오전 2.45.30.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-24_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_2.45.30.png)

### 5) build

짜잔 드디어 빌드가 된다. 이 화면 볼려고 개고생했다. 사실 java 버전 당연히 맞게 해야지 할수도 있는데 처음이라
몰랐다. 다른 분들은 같은 실수를 반복하지 말기를…

![스크린샷 2023-03-24 오전 2.47.51.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-24_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_2.47.51.png)

### 6) run

끝난줄 알았지?? 아직 아니란다~

<aside>
📌 `run`을 하고 싶은데 뭔가 이상하다. Demo2Application 왼쪽 이미지 위에 커서를 올리면 
source 를 다시 설정하라고 뜬다. 이런 경우에는 demo 파일 우클릭 한후
mark directory as > source root 를 하면 된다.

</aside>

![스크린샷 2023-03-24 오전 3.16.48.png](spring%20initializr%E1%84%85%E1%85%A9%20project%20%E1%84%86%E1%85%A1%E1%86%AB%E1%84%83%E1%85%B3%E1%86%AF%E1%84%8B%E1%85%A5%E1%84%87%E1%85%A9%E1%84%80%E1%85%B5%20a384c7e0f876434ca044440909500c4c/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-24_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_3.16.48.png)