# Study

## Git 을 활용한 스터디 방식
<img src="./attached/mori2.png" width="300px" height="300px"  title="Github_Logo"/>

강사: 모리 

안녕! 오늘은 함께 '깃(Git)'이라는 도구에 대해 배워볼 거야. 깃은 컴퓨터에서 파일들을 관리하고, 여러 사람이 함께 작업할 때 도움을 주는 아주 멋진 툴이란다. 마치 시간 여행을 할 수 있는 마법의 상자처럼, 우리가 했던 작업을 기억해주고, 다시 되돌아갈 수도 있게 해준단다! 시작해볼까?

## 핵심 기능🐤🐤

### 1. 깃 설치하기
먼저, 깃을 컴퓨터에 설치해야 해. [깃 공식 홈페이지](https://git-scm.com/)에 가서 자신의 운영체제에 맞는 깃을 다운로드하고 설치하면 돼. 설치가 끝나면, 컴퓨터의 터미널(또는 명령 프롬프트)을 열고 `git --version`을 입력해서 잘 설치되었는지 확인해봐!

### 2. 깃 기본 설정

깃을 사용하기 전에 사용자 이름과 이메일 주소를 설정해야 해. 이 정보는 깃이 누가 어떤 변경을 했는지를 기록할 때 사용된단다. 터미널에서 다음 명령어를 입력해보자:

```bash
git config --global user.name "너의 이름"
git config --global user.email "너의 이메일 주소"
```

config는 configuration(설정)의 약자야! 즉, 너의 이름과, 너의 이메일을 git에 광범위(global)하게 설정하겠다는 뜻이야! 🐣

### 3. 깃 저장소 만들기

깃에서는 '저장소(repository)'라고 불리는 곳에 모든 파일과 변경 기록을 저장해. 자, 이제 너의 첫 번째 깃 저장소를 만들어 볼까? 원하는 폴더로 가서 다음 명령어를 입력해봐:

```bash
git init
```

이 명령어는 그 폴더에 깃 저장소를 만들고, 이제부터 그 폴더에 있는 파일들의 변경 사항을 깃이 기억하게 해줄 거야.

>**토막 상식**
> git init을 하면 실제로 어떤 일이 일어날까?  이 명령은 사실 `.git`  이라는 디렉토리를 만들어. 파일 숨김을 해제하면 볼 수 있단다. 이 디렉토리가 우리가 원하는 마법같은 버전관리를 해주는 거야!

### 4. 변경 사항 기록하기 (Commit)

파일을 새로 만들거나 수정했다면, 깃에게 그 변경 사항을 기억하라고 말해줘야 해. 이걸 '커밋(commit)'이라고 해. 그런데 기억하라고 하기전에 사실 더 해야할 일이 있단다.  

바로 `git add` 명령어를 통해 해당 파일을  '스테이징(stage)'해야 해. 
스테이징이란 뭘까? 바로 깃에게 이 파일들을 감시하라고 알리는 거야! 
보이는 무대(stage)에 올린다고 생각하면 좋아.
즉 깃의 눈에 보이는 곳에 우리 파일들을 놔주는 거지! 
이를 통해 git은 비로소 어떤 파일을 모니터링 할 지 알게 되지:

```bash
git add 파일명
```

`git commit` 전에 우리는 `git add`를 사용해.
어떤 파일의 변경 사항을 기억하려면 당연히 눈에 먼저 보여야겠지?

그 다음에는 이렇게 커밋을 만들어:

```bash
git commit -m "변경 사항에 대한 설명"
```

### 5. 깃 브랜치 (Branch)

깃의 '브랜치(branch)'는 깃을 사용하면서 정말 중요한 개념 중 하나야. 브랜치를 사용하면 마치 마법의 책에서 이야기의 다른 길을 선택하는 것처럼, 하나의 프로젝트에서 여러 가지 다른 작업을 동시에 진행할 수 있어. 각 브랜치는 독립적으로 작업을 진행할 수 있기 때문에, 한 부분에서 실험을 하거나 새로운 기능을 추가하면서도, 메인 프로젝트는 안정적인 상태를 유지할 수 있어.

#### 1. 브랜치 만들기

새로운 브랜치를 만들고 싶을 때는 이 명령어를 사용해:

```bash
git branch 브랜치이름
```
예를 들어, 'feature-login'이라는 새 기능을 개발하기 위한 브랜치를 만들고 싶다면, 다음과 같이 입력해:

```bash
git branch feature-login
```

#### 2. 브랜치 확인하기
현재 프로젝트에 어떤 브랜치들이 있는지 보고 싶다면, 이 명령어를 사용해:

```bash
git branch
```
이 명령어는 모든 브랜치를 나열해주고, 현재 네가 작업하고 있는 브랜치 앞에 별표(\*)를 표시해 줄 거야.

#### 3. 브랜치로 이동하기

다른 브랜치로 작업을 옮기고 싶다면, '체크아웃(checkout)' 명령어를 사용해:

```bash
git checkout 브랜치이름
```

예를 들어, 'feature-login' 브랜치로 작업을 옮기고 싶다면:

```bash
git checkout feature-login
```

이 명령어를 실행하면 깃은 너를 해당 브랜치로 이동시키고, 그 브랜치의 모든 파일과 상태로 너의 작업 환경(맥은 finder, 윈도우는 explorer 상태)을 바꿔줄 거야.

#### 4. 브랜치 삭제하기

브랜치의 작업이 끝나고 더 이상 필요하지 않다면, 다음 명령어로 브랜치를 삭제할 수 있어:

```bash
git branch -d 브랜치이름
```

브랜치를 삭제하기 전에는 해당 브랜치의 변경사항이 다른 브랜치에 합쳐졌는지 확인하는 것이 중요해. 안 그러면 네가 한 모든 작업이 사라질 수 있으니까!

### 브랜치 합치기 (Merge)

다른 브랜치에서 작업을 마치고 그 변경사항을 메인 프로젝트(예를 들면 'master' 브랜치)에 추가하고 싶을 때는 '병합(merge)'을 사용해:

```bash
git checkout master
git merge feature-login
```

이렇게 하면 'feature-login' 브랜치의 모든 변경사항이 'master' 브랜치에 추가되어, 하나의 통합된 프로젝트가 될 거야.

브랜치를 이용하면 여러 사람이 동시에 다양한 작업을 할 수 있고, 모든 작업을 안전하게 관리할 수 있어. 처음에는 조금 복잡하게 느껴질 수 있지만, 조금씩 연습하다 보면 금방 익숙해질거야!

### 6. 코드 공유하기 (Push와 Pull)

너의 코드를 다른 사람과 공유하거나, 다른 사람의 코드를 받아오고 싶을 때는 '푸시(push)'와 '풀(pull)'을 사용해. 깃허브 같은 곳에 너의 코드를 올리려면 이렇게 해:

```bash
git push origin 브랜치이름
```

`origin` 은 기본으로 설정되어 있는 원격 저장소야! 이 곳에 너의 branch 를 푸시해서 저장하겠다는 거지. 

다른 사람의 최신 코드를 받아오려면 이 명령어를 사용해:

```bash
git pull origin 브랜치이름
```

`origin` 으로부터 끌어온다(pull)고 생각하면 쉽지?

### 7. 포크(Fork)

깃허브에서 다른 사람의 프로젝트를 너의 계정으로 복사하는 것을 '포크(fork)'라고 해. 이렇게 하면 다른 사람의 프로젝트에 너만의 변경을 해볼 수 있어. 그리고 그 변경 사항을 원래 프로젝트에 적용해달라고 요청할 수도 있지!

### 8. 풀 리퀘스트 (Pull Request)

'풀 리퀘스트'는 정말 중요해. 이건 네가 만든 변경 사항을 다른 사람에게 보내서, 그 사람의 프로젝트에 네 변경 사항을 포함시켜 달라고 요청하는 거야. 마치 "내가 좀 도와줄게!" 하고 손을 내미는 것과 비슷해. 이렇게 해서 모두가 함께 더 좋은 프로젝트를 만들 수 있지.

좀더 자세히 설명하자면 풀 리퀘스트는 마치 네가 만든 멋진 그림을 친구에게 보여주고, 친구의 그림책에 넣어달라고 부탁하는 것과 같아. 네가 그림을 그리고 나면, 친구가 그 그림을 보고, 모든 친구들이 좋아할지 얘기하면서, 그림책에 넣을 준비를 해.

**풀 리퀘스트의 단계별 설명**
#### 1. 포크(Fork)하기
먼저, 깃허브에서 네가 기여하고 싶은 프로젝트를 찾아. 그 프로젝트의 페이지에서 'Fork' 버튼을 누르면, 그 프로젝트의 복사본이 네 깃허브 계정으로 복사돼. 이제 이 복사본에서 마음껏 그림을 그릴 수 있어!

#### 2. 클론(Clone)하고 작업하기
그 다음에는 네 컴퓨터로 그 복사본을 가져와야 해. 이걸 '클론(clone)'이라고 해. 터미널에서 이 명령어를 사용해:

```bash
git clone https://github.com/네계정/프로젝트이름.git
```
이제 네 컴퓨터에 프로젝트의 복사본이 생겼고, 네가 원하는 변경을 할 수 있어.

#### 3. 브랜치 만들기
네가 작업할 새로운 브랜치를 만들어야 해. 이렇게 하면 원본 프로젝트와 구분해서 네가 무슨 변경을 했는지 쉽게 볼 수 있어.

```bash
git checkout -b 너의브랜치이름
```

#### 4. 변경 사항 커밋하고 푸시하기
네가 작업을 마치고 난 후, 그 변경사항을 네 깃허브의 브랜치로 보내야 해. 이걸 '푸시(push)'라고 하지:

```bash
git add .
git commit -m "네가 한 변경사항 설명"
git push origin 너의브랜치이름
```

#### 5. 풀 리퀘스트 만들기

이제 깃허브로 가서, 네가 방금 푸시한 브랜치 페이지로 가. 거기에서 'Pull Request' 버튼을 클릭해. 그리고 네가 왜 이 변경사항을 원본 프로젝트에 추가하고 싶은지 설명을 적어. 그 후 'Create Pull Request' 버튼을 클릭하면 돼.

#### 예시
예를 들어, 네가 '레시피 북'이라는 프로젝트에서 '초콜릿 케이크' 레시피를 개선한 걸 공유하고 싶다고 생각해보자. 네가 한 변경사항을 풀 리퀘스트로 보내고, 프로젝트 주인이 그 변경사항을 보고 좋다고 생각하면, 네 레시피가 그 프로젝트에 추가될 거야.

풀 리퀘스트는 깃허브에서 정말 중요한 과정이야. 이를 통해 사람들은 서로의 작업에 기여하고, 더 나은 소프트웨어를 만들 수 있지. 게다가, 모두가 네 그림(또는 코드)를 볼 수 있으니까, 함께 배우고 성장하는 기회도 되고!
 
## 기타 기능🐤🐤

### 1. 깃 상태 확인하기 (Status)

깃에서 무슨 일이 일어나고 있는지 궁금할 때는 언제든지 이 명령어를 사용해:

```bash
git status
```
이 명령어를 통해 어떤 파일이 변경되었는지, 어떤 파일이 커밋(commit)을 기다리고 있는지 알 수 있어. 너의 깃이 지금 어떤 상태인지 알려줄 거야.

### 2. 깃 로그 보기 (Log)

깃에서 지금까지 일어난 모든 커밋의 기록을 보고 싶다면, 이 명령어를 써봐:

```bash
git log
```
이 기록을 통해 누가, 언제, 무슨 변경을 했는지 볼 수 있어. 시간 여행을 하는 것처럼 과거의 기록들을 볼 수  있지!

### 3. 충돌 해결하기 (Merge Conflicts)

때때로, 두 사람이 같은 파일의 같은 부분을 수정했을 때 '충돌(conflict)'이 발생할 수 있어. 이건 마치 두 친구가 같은 색연필을 동시에 쓰려고 할 때 생기는 문제와 비슷해. 깃은 너에게 이 충돌을 해결하라고 알려줄 거야. 충돌이 발생하면 깃은 충돌이 난 부분을 표시해주고, 너는 어느 부분을 남길지 결정해서 충돌을 해결해야 해.  이 부분은 심화 과정으로 남길게!

깃은 정말 흥미롭고 유용한 도구야. 하지만 처음에는 조금 복잡할 수 있으니, 천천히 하나씩 배워가면서 익숙해지면 좋겠어! 이상 모리였어~🐥


> 더 깊이있게 git을 배우고 싶니?
>
> 한국어 강의
>[코딩애플 쉽게 설명하는 git 강의 1~3편](https://www.youtube.com/watch?v
>[생활코딩 지옥에서 온 깃](https://www.youtube.com/watch?v=hFJZwOfme6w&list=PLuHgQVnccGMA8iwZwrGyNXCGy2LAAsTXk)
> 
> 한국어 자료
> [깃 공식 문서](https://git-scm.com/book/ko/v2)
> [깃 안내서](https://subicura.com/git/guide/basic.html#git-status-%E1%84%92%E1%85%A7%E1%86%AB%E1%84%8C%E1%85%A2-%E1%84%89%E1%85%A1%E1%86%BC%E1%84%90%E1%85%A2-%E1%84%92%E1%85%AA%E1%86%A8%E1%84%8B%E1%85%B5%E1%86%AB)
> 
> 해외 강의
> [free code camp git and github](https://www.youtube.com/watch?v=RGOj5yH7evk)
