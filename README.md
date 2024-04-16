# Study

## Git을 활용한 스터디 방법

안녕하세요 오늘은 여러분과 함께 '깃(Git)'이라는 도구에 대하여 배워보겠습니다. 깃은 컴퓨터에서 파일들을 관리하고, 여러 사람이 함께 작업할 때 도움을 주는 아주 유용한 툴입니다. 마치 시간 여행을 할 수 있는 타임머신처럼, 우리가 했던 작업을 기억해주고, 다시 되돌아갈 수도 있게 해주는 툴입니다. 시작해보겠습니다.

## 핵심 기능🐤🐤

### 1. 깃 설치하기
먼저, 깃을 컴퓨터에 설치하셔야 합니다. [깃 공식 홈페이지](https://git-scm.com/)에 방문하셔서 자신의 운영체제에 맞는 깃을 다운로드하고 설치하시면 됩니다. 설치가 완료되면, 컴퓨터의 터미널(또는 명령 프롬프트)을 열고 `git --version`을 입력하여 잘 설치되었는지 확인해 보세요.

### 2. 깃 기본 설정

깃을 사용하기 전에 사용자 이름과 이메일 주소를 설정하셔야 합니다. 이 정보는 깃이 누가 어떤 변경을 했는지를 기록할 때 사용됩니다. 터미널에서 다음 명령어를 입력해 보세요:

```bash
git config --global user.name "github에 설정한 당신의 이름"
git config --global user.email "github 상 당신의 이메일 주소"
```

### 3. 깃 저장소 만들기

깃에서는 '저장소(repository)'라고 불리는 곳에 모든 파일과 변경 기록을 저장합니다. 이제 여러분의 첫 번째 깃 저장소를 만들어 볼까요? 원하는 폴더로 가서 다음 명령어를 입력해 보세요:

```bash
git init
```

이 명령어는 그 폴더에 깃 저장소를 만들고, 이제부터 그 폴더에 있는 파일들의 변경 사항을 깃이 기억하게 해줍니다.

### 4. 변경 사항 기록하기 (Commit)

파일을 새로 만들거나 수정하셨다면, 깃에게 그 변경 사항을 기억하라고 말씀드려야 합니다. 이것을 '커밋(commit)'이라고 합니다. 그러나 기억하라고 하기 전에 사실 더 해야 할 일이 있습니다.

바로 `git add` 명령어를 통해 해당 파일을 '스테이징(stage)'해야 합니다. 스테이징은 깃에게 이 파일들을 감시하라고 알리는 것입니다. 보이는 무대(stage)에 올린다고 생각하시면 좋습니다. 이를 통해 깃은 어떤 파일을 모니터링할지 알게 됩니다:

```bash
git add 파일명
```

그 다음에는 이렇게 커밋을 만드세요:

```bash
git commit -m "변경 사항에 대한 설명"
```

### 5. 깃 브랜치 (Branch)

깃의 '브랜치(branch)'는 깃을 사용하면서 정말 중요한 개념 중 하나입니다. 브랜치를 사용하면 마치 마법의 책에서 이야기의 다른 길을 선택하는 것처럼, 하나의 프로젝트에서 여러 가지 다른 작업을 동시에 진행할 수 있습니다. 각 브랜치는 독립적으로 작업을 진행할 수 있기 때문에, 한 부분에서 실험을 하거나 새로운 기능을 추가하면서도, 메인 프로젝트는 안정적인 상태를 유지할 수 있습니다.

#### 1. 브랜치 만들기

새로운 브랜치를 만들고 싶으시다면, 이 명령어를 사용하세요:

```bash
git branch 브랜치이름
```

#### 2. 브랜치 확인하기
현재 프로젝트에 어떤 브랜치들이 있는지 보고 싶으시다면, 이 명령어를 사용하세요:

```bash
git branch
```

#### 3. 브랜치로 이동하기

다른 브랜치로 작업을 옮기고 싶으시다면, '체크아웃(checkout)' 명령어를 사용하세요:

```bash
git checkout 브랜치이름
```

#### 4. 브랜치 삭제하기

브랜치의 작업이 끝나고 더 이상 필요하지 않으시다면, 다음 명령어로 브랜치를 삭제하실 수 있습니다:

```bash
git branch -d 브랜치이름
```

브랜치를 삭제하기 전에는 해당 브랜치의 변경사항이 다른 브랜치에 합쳐졌는지 확인하는 것이 중요합니다. 그렇지 않으면 여러분이 한 모든 작업이 사라질 수 있습니다.

### 브랜치 합치기 (Merge)

다른 브랜치에서 작업을 마치고 그 변경사항을 메인 프로젝트(예를 들면 'master' 브랜치)에 추가하고 싶으시다면, '병합(merge)'을 사용하세요:

```bash
git checkout master
git merge feature-login
```

이렇게 하면 'feature-login' 브랜치의 모든 변경사항이 'master' 브랜치에 추가되어, 하나의 통합된 프로젝트가 됩니다.

브랜치를 이용하면 여러 사람이 동시에 다양한 작업을 할 수 있고, 모든 작업을 안전하게 관리할 수 있습니다. 처음에는 조금 복잡하게 느껴질 수 있지만, 조금씩 연습하다 보면 금방 익숙해지실 겁니다.

### 6. 코드 공유하기 (Push와 Pull)

여러분의 코드를 다른 사람과 공유하거나, 다른 사람의 코드를 받아오고 싶으시다면, '푸시(push)'와 '풀(pull)'을 사용하세요. 깃허브 같은 곳에 여러분의 코드를 올리려면 이렇게 하세요:

```bash
git push origin 브랜치이름
```

다른 사람의 최신 코드를 받아오려면 이 명령어를 사용하세요:

```bash
git pull origin 브랜치이름
```

### 7. 포크(Fork)

깃허브에서 다른 사람의 프로젝트를 여러분의 계정으로 복사하는 것을 '포크(fork)'라고 합니다. 이렇게 하면 다른 사람의 프로젝트에 여러분만의 변경을 해볼 수 있습니다. 그리고 그 변경 사항을 원래 프로젝트에 적용해달라고 요청할 수도 있습니다.

### 

### 8. 풀 리퀘스트 (Pull Request)

'풀 리퀘스트'는 정말 중요합니다. 이것은 여러분이 만든 변경 사항을 다른 사람에게 보내서, 그 사람의 프로젝트에 여러분의 변경 사항을 포함시켜 달라고 요청하는 것입니다. 마치 "제가 도와드리겠습니다!" 하고 손을 내미는 것과 비슷합니다. 이렇게 해서 모두가 함께 더 좋은 프로젝트를 만들 수 있습니다.

**풀 리퀘스트의 단계별 설명**
#### 1. 포크(Fork)하기
먼저, 깃허브에서 여러분이 기여하고 싶은 프로젝트를 찾습니다. 그 프로젝트의 페이지에서 'Fork' 버튼을 누르면, 그 프로젝트의 복사본이 여러분의 깃허브 계정으로 복사됩니다. 이제 이 복사본에서 마음껏 그림을 그릴 수 있습니다.

#### 2. 클론(Clone)하고 작업하기
그 다음에는 여러분의 컴퓨터로 그 복사본을 가져와야 합니다. 이것을 '클론(clone)'이라고 합니다. 터미널에서 이 명령어를 사용하세요:

```bash
git clone https://github.com/당신의계정/프로젝트이름.git
```
이제 여러분의 컴퓨터에 프로젝트의 복사본이 생겼고, 여러분이 원하는 변경을 할 수 있습니다.

#### 3. 브랜치 만들기
여러분이 작업할 새로운 브랜치를 만드세요. 이렇게 하면 원본 프로젝트와 구분해서 여러분이 무슨 변경을 했는지 쉽게 볼 수 있습니다.

```bash
git checkout -b 당신의브랜치이름
```

#### 4. 변경 사항 커밋하고 푸시하기
여러분이 작업을 마치고 난 후, 그 변경사항을 여러분의 깃허브의 브랜치로 보내셔야 합니다. 이것을 '푸시(push)'라고 합니다:

```bash
git add .
git commit -m "당신이 한 변경사항 설명"
git push origin 당신의브랜치이름
```

#### 5. 풀 리퀘스트 만들기

이제 깃허브로 가서, 여러분이 방금 푸시한 브랜치 페이지로 가세요. 거기에서 'Pull Request' 버튼을 클릭하시고 여러분이 왜 이 변경사항을 원본 프로젝트에 추가하고 싶은지 설명을 적으세요. 그 후 'Create Pull Request' 버튼을 클릭하세요.

#### 예시
예를 들어, 여러분이 '레시피 북'이라는 프로젝트에서 '초콜릿 케이크' 레시피를 개선한 것을 공유하고 싶다고 생각해 보세요. 여러분이 한 변경사항을 풀 리퀘스트로 보내고, 프로젝트 주인이 그 변경사항을 보고 좋다고 생각하면, 여러분의 레시피가 그 프로젝트에 추가될 것입니다.

풀 리퀘스트는 깃허브에서 정말 중요한 과정입니다. 이를 통해 사람들은 서로의 작업에 기여하고, 더 나은 소프트웨어를 만들 수 있습니다. 게다가, 모두가 여러분의 그림(또는 코드)를 볼 수 있기에, 함께 배우고 성장하는 기회도 됩니다.

 
## 기타 기능🐤🐤

### 1. 깃 상태 확인하기 (Status)

깃에서 무슨 일이 일어나고 있는지 궁금할 때는 언제든지 이 명령어를 사용합니다:

```bash
git status
```
이 명령어를 통해 어떤 파일이 변경되었는지, 어떤 파일이 커밋(commit)을 기다리고 있는지 알 수 있습니다. 여러분의 깃이 지금 어떤 상태인지 알려줍니다.

### 2. 깃 로그 보기 (Log)

깃에서 지금까지 일어난 모든 커밋의 기록을 보고 싶다면, 이 명령어를 써보세요:

```bash
git log
```
이 기록을 통해 누가, 언제, 무슨 변경을 했는지 볼 수 있습니다. 시간 여행을 하는 것처럼 과거의 기록들을 볼 수 있습니다.

### 3. 충돌 해결하기 (Merge Conflicts)

때때로, 두 사람이 같은 파일의 같은 부분을 수정했을 때 '충돌(conflict)'이 발생할 수 있습니다. 이건 마치 두 친구가 같은 물건을 동시에 쓰려고 할 때 생기는 문제와 비슷합니다. 깃은 여러분에게 이 충돌을 해결하라고 알려줄 것입니다. 충돌이 발생하면 깃은 충돌이 난 부분을 표시해주고, 여러분은 어느 부분을 남길지 결정해서 충돌을 해결해야 합니다.  이 부분은 심화 과정으로 남기겠습니다!

깃은 정말 흥미롭고 유용한 도구입니다. 하지만 처음에는 조금 복잡할 수 있으니, 천천히 하나씩 배워가면서 익숙해지면 좋겠습니다! 이상 입니다~🐥


> 더 깊이있게 git을 배우고 싶니?
>
> 한국어 강의
>[코딩애플 쉽게 설명하는 git 강의 1~3편](https://www.youtube.com/watch?v=sly2u8BIi9E)
>[생활코딩 지옥에서 온 깃](https://www.youtube.com/watch?v=hFJZwOfme6w&list=PLuHgQVnccGMA8iwZwrGyNXCGy2LAAsTXk)
> 
> 한국어 자료
> [깃 공식 문서](https://git-scm.com/book/ko/v2)
> [깃 안내서](https://subicura.com/git/guide/basic.html#git-status-%E1%84%92%E1%85%A7%E1%86%AB%E1%84%8C%E1%85%A2-%E1%84%89%E1%85%A1%E1%86%BC%E1%84%90%E1%85%A2-%E1%84%92%E1%85%AA%E1%86%A8%E1%84%8B%E1%85%B5%E1%86%AB)
> 
> 해외 강의
> [free code camp git and github](https://www.youtube.com/watch?v=RGOj5yH7evk)
