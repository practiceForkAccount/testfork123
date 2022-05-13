# testfork

### fork 후 협업하는 방법

1. 레포지토리를 fork 한다.
2. fork 해온 나의 repo를 local에서 clone 한다. -> 자동으로 origin remote 생성!
3. 원본 레포지토리를 'upstream'으로 remote에 추가해준다.

--- 코드 수정 준비 끝

4. 로컬에서 branch를 생성한다.
   : `git branch -b <branch명>`
5. 해당 branch에서 코드 작업 후 add, commit, push한다.
   : 이때 push는 `git push origin <branch명>`
6. 나의 repo에 PR 요청이 온 것을 확인할 수 있다.
7. fetch를 통해 원본 repo의 변경사항을 미리 확인한다.
   : `git fetch upstream` -> `git checkout upstream/main`
8. 변경된 사항이 없다면 나의 repo에서 원본 repo로 PR을 만든다.
   : PR 후 사용했던 원격 branch를 github에서 삭제해줄 수 있다.
9. 원본 repo에서 확인 후 merge 됐으면, 대부분 github에서 나의 repo에도 자동 merge 해준다.
   (+) 나의 repo에 자동 merge가 되어 있지 않으면 Fetch upstream을 통해 반영해준다.
10. 사용했던 branch를 삭제해준다.

- 로컬의 경우
  확인 `git branch` / 삭제 `git branch -d <브랜치명>`

- 원격의 경우
  확인 `git branch -r` / 삭제 `git push origin --delete <브랜치명>`

* 원격 브랜치를 삭제할 경우 간혹가다 해당 브랜치가 없다고 한다. 그런 경우는, 8번에서 삭제한 것처럼 원격에서는 삭제됐지만 로컬에는 아직 반영이 안된 것.
  따라서 `git fetch -p origin`을 통해 원격 정보를 로컬에 받아온다.

11. 로컬의 main 브랜치에 원격 저장소 내용을 pull 해온다.

### 원격 브랜치를 삭제하지 않고 계속 사용하는 경우

1. (1)~(8)까지 동일한 작업을 진행하고, 브랜치는 삭제하지 않는다.
2. push를 진행하기에 앞서 commit 이력도 쌓아본다.
3. 제대로 진행하고 있다면 나의 repo에서 Fetch upstream에 Fetch and merge 버튼이 활성화 되는것 같다.
4. branch를 삭제하지 않고 기존에 있던 branch에 들어가면 `This branch is 2 commits ahead, 1 commit behind forkTestRepo/testfork:main.` 이러한 메시지가 github에서 보인다.
5. 따라서 fork를 했을 때 기존의 branch를 이어서 쓰는것은 좋지않아보인다... 아니면 다른 방법이 있을까?!
