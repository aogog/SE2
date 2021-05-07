https://github.com/aogog/SE2
# 보고서

## 1. 빈문서 상태
먼저 github에 repository를 생성한 후, 아래의 그림을 따라 주소를 복사한다.
![basic](./2/basic1.png "basic")

git을 사용할 수 있는 환경을 준비 한 후, github와 연동할 로컬 저장소(디렉토리)를 생성 한 후 해당 디렉토리로 이동한 후 아래의 그림과 같이 명령어를 수행한다.
![init](./2/init.png "init")
git init 명령어는 해당 로컬 저장소를 Git 저장소로 이용하겠다는 의미이다. 따라서 위 그림에서는 soft 디렉토리가 Git 저장소로 이용된다.

위의 과정이 완료 되었으면 아래의 그림과 같이 git config를 설정해준다.
![config](./2/config.png "confing")
위의 과정은 git을 처음 실행했을때 한번만 해주면 되는 과정으로, 사용자의 이름, 이메일을 설정할때 사용한다.

### 2. git remote

로컬 저장소를 생성했으면, 원격저장소(github)과 연동을 시키기위해 1번에서 복사한 주소를 이용하여 아래의 그림과 같이 실행한다.
![remote](./2/remote.png "remote")
위 과정으로 github과 로컬저장소가 연동이되었다.

### 3. git pull & push

현재 로컬저장소는 github과 연동되어있지만 아무런 데이터도 없는 상태이다. 따라서 github에서 README.md 데이터를 가져와야한다.
github에서 데이터를 로컬저장소로 갖고 올 수 있는 명령어인 pull은 아래와 같이 실행 할 수 있다.
![pull](./2/pull.png "pull")
위 그림은, github의 main 의 데이터를 해당 branch로 갖고오는 과정이다.

pull과는 반대로 `git push origin <branch>` 명령어는 해당 branch를 github로 보내는 명령어이다.
![push](./2/push.png "push")

### 4. git add & commit (status)
git pull 을 통해 main branch를 작업 branch로 만든 후, `new.md` 라는 파일을 수정한다. 그리고, `git add new.md` 명령어를 통해 new.md가 추가되었다는 정보를 전달해준다. 이 때, `git add -A` 명령어를 이용하면, 변경된 모든 파일을 전달해주므로 간편하다.
`git commit` 명령어는 해당 변경에 대한 commit를 남기는 명령어로, 대부분 `git commit -m "message"` 처럼, -m 옵션을 사용하요 message를 남길 때 사용한다.
![add](./2/add.png "add")
main 에서는 프로젝트의 목차에 해당하는 Order만을 추가 한 후, 각각 P1,P2,P3 branch로 나눠서 작업할 수 있게 해준다.
이 때, commit에 접근할 수 있는 방법중 하나인, hash가 있지만, `tag`명령어를 사용하면 더 쉽게 commit에 접근할 수 있다.
tag 추가방법은 commit와 유사한데, 아래의 그림처럼 `git tag <태그명>`처럼 태그를 추가하고, commit한 뒤 push를 해주어, tag를 달 수 있다.
![tag](./2/tag.png "tag")
![branch1](./2/branch.png "branch")
위 그림을 2번 반복하여 P1,P2,P3 branch를 만든다.
즉, P1,P2,P3,main 에는 Order정보만을 갖고있는 new.md가 생성된 상태이다.

대부분 수정 후 add 및 commit명령어를 수행하지만, 해당 branch의 상태를 알고 싶을 때 `git status`명령어를 사용하면 아래의 그림처럼 해당 branch에서 수정된 파일이 있는지 확인할 수 있다.
![status](./2/status.png "status")

### 5. git branch & checkout

git branch <이름> 으로 실행하면 해당 이름을 가진 branch를 생성하고, 단순히 git branch 를 실행하면 현재 branch 및 현재 작업 branch(*)를 보여주고 checkout <이름> 명령어는 branch를 해당 branch로 이동시켜주는 명령어이다.
![branch](./2/checkout.png "branch&checkout")
***  
이제 P2의 입장에서 해당 프로젝트를 진행한다고 가정한다. 위 그림처럼
`git checkout P2`명령어를 통해 P2 branch로 작업 환경을 변경한다.

P2의 분야는 7~16번 기능이므로, `new.md`파일에 7~16번 파일을 추가한다. 이 때, P2는 한번에 7~16번 기능을 모두 완료한 후, github에 push 했다고 가정한다.
![pushp2](./2/pushp2.png "pushp2")
위 그림처럼, `new.md`파일을 수정 한 후, `git add -A` 명령어를 수행하여 변경된 파일을 모두 추가한 다음, commit 을 남겨준 뒤, `git push origin P2`명령어를 통해 로컬저장소에 있는 P2 branch의 파일들을 github에 전송한다.

P2의 입장에서 자신의 할 일을 모두 완료했으니 main과 합치는 작업만 하면 역할이 끝난다.

### 6. git merge
이때, main branch로 이동 한후, `git merge P2` 명령어를 수행해주면 된다.
![mergep2](./2/mergeP2.png "mergeP2") 
위 그림은, main과 P2 branch가 merge가 되는 과정인데, 이 때 P2는 main의 `new.md`를 수정하지않고 단순히 추가하는 과정만 진행하였으므로, main의 `new.md`와 conflict되는 부분이 없다.
따라서 아무런 제약없이 main과 merge가 되는 것을 볼 수 있다.
* * *
P2가 작업을 끝낸 뒤, P3가 자신이 맡은 분야를 수행하기 시작했다.
P2와 마찬가지로 P3도 한번에 자신이 맡은 분야 17~23번 기능을 추가했다. 따라서, P2와 마찬가지로 `git add -A` 명령어 수행 후, commit를 남긴 다음, `git push origin P3` 명령어 수행을 통해 자신이 한 작업을 github에 추가한다.

이 때, P3는 main에서는 `new.md`를 수정하지 않았지만, 이미 P2가 main과 merge한 상태이므로, P3는 main의 `new.md`를 수정했다고 보면된다.
따라서 위의 P2가 main과 merge하는 상황과는 다르게 conflict가 아래의 그림처럼 발생한다.
![mergep3](./2/mergeP3.png "mergep3")
이런 경우, 사용자가 직접 합치려는 파일을 수정하여 사용해야한다.
![mergehead](./2/mergehead.png "mergehead")
위 그림처럼 `<<<<<< HEAD`부분을 발견할 수 있는데, 해당 부분부터 `========`부분까지가 HEAD가 가리키는 부분이고 그 밑에서 부터 `>>>>>>> (branch 이름)`까지가 해당 branch의 부분이다.
위 부분에서 사용자가 conflict하는 부분을 수정 한후 `git add -A` 명령어 수행 후, `git merge <branch 이름>`을 수행해 주면, 정상적으로 merge가 수행된다. 정상적으로 merge가 되었음을 확인하면
`git push origin main` 명령어를 통해 merge된 파일을 github에 push 해준다.
![mergep2p3](./2/mergep2p3.png "p2p3")
***
### 7. git rebase & log
P2와 P3가 모든 작업을 완료 한 후, P1(1~6)이 프로젝트를 시작했다.
P2,P3의 때와 마찬가지로, 자신이 맡은 부분을 작업 한 후, add 및 commit를 수행한다.
하지만 P1은 P2,P3와는 다르게 해당 프로젝트를 여러번에 걸쳐 진행했다. 즉, 첫번째 commit에서는 1~4번 기능을, 두번째 commit에서는 5번기능을 추가했고, 세번째 commit에서는 추가했던 5번 기능을 수정했고, 마지막 네번째 commit에서는 5번과 6번을 추가했다.
즉, P1은 4번의 add와 4번의 commit를 실행하여 자신이 맡은 부분을 완성했다.
P1이 단순히 push를 실행하면, P1의 commit history에는 4번의 commit가 추가되겠지만, 여러명이 함께하는 프로젝트에서 중요하지 않은 commit는 없애는 것이 가독성이 좋기때문에 P1은 해당 commit를 하나의 commit로 만들기 위해 `rebase` 명령어를 실행하기로 했다.

먼저, 4번의 commit를 수정하기 위해 아래 그림처럼 `git rebase -i @~4` HEAD에서부터 4번의 commit를 `-i` 대화형으로 진행한다는 뜻이다.
이때, 사용자가 이용한 commit의 기록을 보기위해선 `git log` 명령어를 사용하면 된다.
![log](./2/log.png "log")
위 그림처럼 사용자가 commit한 기록을 볼 수 있다. 이를 바탕으로 rebase 명령어를 수행하면 된다.
![rebase1](./2/rebase1.png "rb1")
위 그림처럼 명령어를 수행하면 다음과 같은 그림이 등장한다.
![rebase2](./2/rebase2.png "rb2")
위 그림을 보면, 4번의 pick가 등장한다.
그림에서 알 수 있듯이 pick,reword,edit,squash 등 여러가지 command가 있다.
이 중에서, P1은 4개의 commit를 하나의 commit로 합치기 위해, 맨 위의 commit를 reword command를 이용하여 add 1~6으로 변경하고,
나머지 commit는 squash command를 이용하기로했다.
위 설명처럼 진행하고 Exit를 하면, 다음과 같은 그림이 등장한다.
![rebase3](./2/rebase3.png "rb3")
위 그림은, 사용자가 나타내려고 하는 통합된 commit를 작성할 수 있는 화면이다. 위 그림에서 add 1~4를 add 1~6으로 수정해주면, 통합된 commit의 설명은 add 1~6으로 수정된다.
![rebase4](./2/rebase4.png "rb4")
위 그림처럼 진행되는데, 여기서 통합된 commit에 대한 설명들을 작성할 수 있다.
위 과정을 모두 마치고 Exit를 실행하면, 아래와 같은 그림이 나오면서 rebase가 완료된다.
![rebase5](./2/rebase5.png "rb5")
모든 rebase 과정이 완료 되었으므로, 해당 데이터를 github에 push해주어야 한다.
이 때, 이미 존재하는 commit에 덮어쓰기를 해야하므로, `git push -f origin P1`명령어를 통해, 강제로 덮어쓰기를 실행한다.
![rebasep](./2/rebasepush.png "rbp")
위 그림처럼 진행되었다면, github의 상태는 아래와 같다.
![github](./2/github.png "gith")
위 그림의 `...`을 클릭하면 사용자가 통합한 commit에 대한 설명을 볼 수 있다. 즉, rebase를 사용하면, commit가 여러번 나오는 것에 비해 commit상태가 매우 깔끔한 것을 볼 수 있다.
***
### 8. git rebase(2)
P1이 자신이 맡은 부분을 전부 완료하였으므로, P2,P3의 코드와 merge하는 과정만이 남았다.
P1은 merge를 사용하는 대신`rebase`를 사용하기로 하였다.
즉, main의 모든 commit 뒤에 P1의 commit를 추가하려고 했다.
![rbp1](./2/rebasep1.png "rbp1")
merge와 마찬가지로, main과 P1이 conflict가 발생했다.
![rbp2](./2/rebase2p1.png "rpb2")
위 그림처럼 conflict하는 부분을 수정 한뒤, add를 실행해 주고,
`rebase --continue` 명령어를 통해 conflict를 수정 한 뒤,계속 진행해준다.
이제, main branch로 이동 한 후, P1과 merge 명령어를 실행하면 모든 merge과정이 완료된다.
***
### 9. git clone <url>
P1,P2,P3 세 사람의 코드를 모두 main에 합치게 된 P1은 해당 프로젝트를 백업하기 위하여, `git clone <주소>` 명령어를 통해 백업해두기로 했다.
![clone](./2/clone.png "clone")
위 그림처럼 P1은 해당 프로젝트를 soft-clone라는 디렉토리에 clone명령어를 통해 백업을 진행해두었다.
***
### 10. git reset --hard
P2가 실수로 main branch에서 `reset --hard` 명령어를 실행하여, P3와 merge한 시점으로 리셋되어버렸다.
![rest](./2/resethard.png "reset")
github의 상황은 아래와 같다
![reset](./2/reset.png "res")
***
다행히 clone을 통해 P1이 프로젝트를 백업해둬서 데이터를 복구하는데에 어려움은 없었다.
또한, P1은 단순히 main에 merge한 것이 아니라, `rebase`명령어를 통해 main에 P2,P3가 commit 한 후 commit를 추가하여서, P1의 branch를 보면 main과 똑같은 것을 알 수 있다.
![good](./2/good.png "good")

## main 이 최종 new.md 파일이 아니라 P1 branch가 최종 md파일입니다. (reset --hard 명령어를 통해 main의 new.md를 reset했습니다.)
***
| Command | Use |Link |
| ---|---|---|
| Add | O | https://github.com/aogog/SE2/commit/bbd845ff6c862b67a2044c64396101956d5370ba|
| Branch | O | https://github.com/aogog/SE2/tree/P1|
| Checkout | O | .md파일 5번째 설명|
| Clone | O | .md 파일 9번째 설명|
| Commit | O | .md 파일 4번째 설명|
| Config | O | .md 파일 1번째 설명|
| Init | O | .md 파일 1번째 설명|
| Log | O | .md 파일 7번째 설명|
| Merge | O | https://github.com/aogog/SE2/commit/1b59426c576fdee50c4a8c7e946b976525bf98f5|
| Pull | O | .md 파일 3번째 설명|
| Push | O | .md 파일 3번째 설명|
| Rebase | O | https://github.com/aogog/SE2/commit/b5619fdb06c23b7a86fe2f29bbe0cbe2ff2f90cd|
| Remote | O | .md 파일 2번째 설명|
| Reset --hard | O | .md 파일 10번째 설명|
| Status | O | .md 파일 4번째 설명|
| Tag | O | https://github.com/aogog/SE2/tags|
