
✨ **중요 내용 요약**  ✨
``` 
풀이 제출 요일 : 금/토/일 선택
file name : 정길연_9822.java
commit message : [정길연] 백준 9822번 문제풀이
PR Title : [1주차] 정길연 풀이제출
```

---------------------------------------

# 1) Git 과 Github란
```
Git에 대해 이야기하기전에, 우리가 하는 프로젝트는 spring, react, docker 등을 사용해서 서비스를 만들게 돼요.  
그러면 6-7명이 함께 서비스를 만들때 누가 어디 코드를 추가하고 변경하는지 알아야합니다.

학교에서 보고서같은거 만들때 이렇게 파일을 주고 받으신 경험이 분명있을거라 생각하는데요. 
현재 우리가 진행할 프로젝트인경우 폴더가 여러개 존재하고, 파일 또한 열몇개가 생기기때문에 어떤 파일의 어디 부분이 변경됐는지 수동으로는 파악자체가 불가해요. 
그래서 우리는 같은 파일을 가지고 변경 사항을 관리하기 위해 분산 버전 관리 시스템인 Git을 이용합니다.

Git은 본인의 코드와 수정내역을 관리하고 돕는 분산 버전 관리 시스템입니다.

하지만 Git자체는 로컬 저장소를 사용하기 때문에 다른 사람들과 공유가 불가하다는 점이 있습니다.

그래서 우리는 다른 사람들과 같은 파일을 관리하기위해 Github를 사용합니다.
Github는 Git을 기반으로 소스코드를 관리해주고 코드를 공유할 수 있는 원격저장소입니다.
```

---------------------------------------

# 2) Git repository PC로 가져오는 방법 

### 1. 본 레포지토리를 fork합니다.
![화면 캡처 2023-03-31 171255](https://user-images.githubusercontent.com/52391627/229064425-23faec82-2a5c-405b-89cf-8751fef14518.png)
* Owner : 본인, create fork 클릭
* fork하면 본인 레포지토리가 생성됩니다.
![화면 캡처 2023-03-31 171551](https://user-images.githubusercontent.com/52391627/229065122-ad9754aa-02b5-478b-861e-86b6525d001d.png)
* 🎁 알아보면 도움되는 것: fork vs clone, branch


### 2.  fork한 레포지토리를 clone합니다.
* clone을 누르면 url이 보이는데, 이를 복사해줍니다.
![화면 캡처 2023-03-31 171748](https://user-images.githubusercontent.com/52391627/229066668-34c6557d-a451-4428-bc05-237f5e3eaca7.png)


### 3. 본인이 사용하는 IDE(ex. Eclipse, IntelliJ, VScode)의 초기 화면에서  **Get from VCS**  와 같은 기능을 찾아주고, url를 붙여넣어 프로젝트를 실행해줍니다. 
* Eclipse 와 Git repositoey 연결 방법
https://hgko1207.github.io/2020/05/18/eclipse-git-clone/
* VScode 와 Git repositoey 연결 방법
![image](https://user-images.githubusercontent.com/52391627/229070780-7a1efbe8-e21a-4a47-b50d-2b1ef6220f10.png)


### 4. IDE에서 문제를 풀어줍니다. 


---------------------------------------

# 3) Github에 올리는 방법

### 1문제당 1commit을 해줍니다. 
  * Commit message 컨벤션 : **[정길연] 백준 1893번 문제풀이**
  * Commit 방법 : 터미널에서 다음 명령어를 입력해줍니다. (이때, git을 처음 사용하는 PC는 **git bash** 프로그램을 설치해줘야합니다)
  * 터미널로 직접 명령어로 치는 방법이 있고, IDE자체에서 지원하는 기능이 있는데 명령어가 익숙지 않다면 IDE별로 찾아보시길 바랍니다.
  ```
   git commit -m "[정길연] 백준 1893번 문제풀이"
  ```
  
> Commit이 뭔데..? 

* git add를 통해 원하는 폴더내의 수정내역들을 스테이징 에리아에 올립니다. 
 스테이징 에리아(Staging Area)는 깃 커밋을 하기 전에 저장되는 깃 공간을 의미해요. 
```
 - git repository
    - 저장소로, 파일이나 폴더를 저장해두는 곳이다. Local Repository와 Remote Repository로 나뉜다.
- staging area
    - Working directory에서 작업한 파일을 local repository에 전달하기 위해 파일들을 분류하는 공간이다.
- working directory
    - 개발자가 소스코드를 수정하며 개발하는 공간이다.
```


* 스테이지에 올린 파일 수정내역들을 git commit 명령어를 이용해 로컬저장소에 저장해줍니다. 여기까지하면 로컬에만 저장될뿐, 나와 같이 프로젝트를 진행하는 다른 개발자는 변경내역을 확인할 수 없어요. 

![image](https://user-images.githubusercontent.com/52391627/229071235-78b433ac-5c13-4674-bd6a-11bde42d6497.png)


* 따라서 원격저장소인 github에 올려야합니다. 이때 우리는 git push 명령어를 사용해요. 이렇게 원격저장소에 올리면 다른 개발자는 변경내역을 확인할 수 있습니다. 

![image](https://user-images.githubusercontent.com/52391627/229071504-1faffde1-e76a-447a-b779-4623daf171c0.png)

* 하지만 본인이 작업하고 있는 PC에는 자동으로 적용되지않습니다. 그래서 다른 개발자는 git pull명령어를 이용해서 변경된 내역들을 끌어옵니다. 

---------------------------------------

# 4) 문제 제출 방법 
* 문제풀이는 1주에 한 번씩 제출합니다 (금/토/일 중 원하는 날)
* 문제풀이제출은 **Pull Request** 를 통해 합니다.

## 1. PR 생성 방법
* 본인 repository로 가서  **Pull Request** 누르고,  **New Pull Request** 을 선택해줍니다.

![화면 캡처 2023-03-31 175331](https://user-images.githubusercontent.com/52391627/229074567-8706d624-8c3a-4812-8151-c301bb19fbfc.png)

* 1. Base repository : 내가 Pull Request(이하 PR)을 보낼 원본 레포지포리다. (fork해온 레포지토리)
* 2. Head reposityor : 내가 작업한 '내' repository 이다.
  * 현재는 단순 문제풀이 제출 repository지만, 앞으로 프로젝트를 할 땐, **branch** 를 사용할 것이기 때문에 미리 ** branch도 어떤 것을 가리키고 있는 지 확인하는 습관 ** 을 들이자.
* 3. **Create Pull Request**
![화면 캡처 2023-03-31 175532](https://user-images.githubusercontent.com/52391627/229074997-0a99e8dc-5730-468a-8db8-c6da37c20a46.png)

## 2. PR 보내기
* Title 양식 : [1주차] 정길연 풀이제출
* Content : 특별한 내용이 없다면 생략가능 (특별한 내용 : 못푼 문제, 다른 방법으로 여러개 푼 문제..등)
![image](https://user-images.githubusercontent.com/52391627/229076361-c16746d6-81d2-4d3d-ab89-619f372d6179.png)
> PR을 보내면?
* 꼭 !!!!!!!!!!!!!!!!!! **This branch has no conflicts with the base branch** 문구 확인 필수
   * 현재는 별 문제 없겠지만, 프로젝트를 진행하면 충돌나는 경우가 다수 있다. 
![화면 캡처 2023-03-31 180508](https://user-images.githubusercontent.com/52391627/229077167-dbffb9db-9f43-488e-95be-447dc4939505.png)
ubusercontent.com/52391627/229076361-c16746d6-81d2-4d3d-ab89-619f372d6179.png)
