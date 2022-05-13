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
6. 나의 repo에 PR이 생성됨을 확인할 수 있다.
