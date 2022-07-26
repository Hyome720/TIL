# Branch란?

- 기능 단위의 별도의 작업 공간
- 각각의 Branch 작업은 독립적
- Master Branch (모두가 확인 가능)
  - A Branch (A만 확인 가능)
  - B Branch (B만 확인 가능)
- git branch {branch 이름}
  - 브랜치 생성
- git branch
  - 브랜치 목록 확인

- git switch {branch 이름}
  - 브랜치로 이동
- git merge {branch 이름}
  - 브랜치 병합
  - :wq 입력하고 나오기
  - 병합한 branch가 필요 없어졌다면 삭제햣 

- git log --oneline --graph
  - branch가 갈라지고 합쳐지는 과정을 그래프로 보여줌
  - git log --oneline -a --graph