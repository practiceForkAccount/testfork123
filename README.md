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
9. 원본 repo에서 확인 후 merge 됐으면, 대부분 github에서 나의 repo에도 자동 merge 해준다.
10. 로컬의 main 브랜치에 원격 저장소 내용을 pull 해온다.
    : 이때 작업 branch에서 로컬 main branch로 checkout 하려면 작업 내역이 없어야한다. 즉, add나 commit을 해둬야한다는 것!
11. 사용했던 branch를 삭제해준다.
