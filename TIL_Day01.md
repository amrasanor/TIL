# TIL 1일차
## Markdown
---
### Markdown이란?
> 개발 중 내용 정리를 위한 문서 작성에 용이한 경량 마크업 언어
- 제목: #, ##, ###, ...
- 목록: 기호 목록과 숫자 목록 사용 가능
  1. 기호 목록: -, *, +
  2. 숫자 목록: 1. 2. 3.
- 강조
  1. 기울임: \*글자\* or \_글자\_ (*예시*)
  2. 굵게: \*\*글자\*\* or \_\_글자\_\_ (**예시**)
  3. 취소선: \~\~글자\~\~ (~~예시~~)
- 코드
  1. 중간에 쓰기(인라인): \`내용\` (`print('예시')`)
  2. 블록으로 쓰기: \`\`\`언어 이름 내용 \`\`\`
    ```python
    print('예시')
    ```
- 링크: \[링크 설명\](링크 내용)
- 이미지: !\[이미지 설명\](링크 내용)
- 인용: >, >>, >>>
- 표: 세로줄은 |, 가로줄은 -로 표시
    | 예시 | 내용 |
    | - | - |
    | TIL | Day01 |
    | Markdown | Git/Github |
- 수평선: ---, ***, ___
- 실습한 내용: [README.MD](https://github.com/amrasanor/TIL/blob/master/README.MD)
---

## Git / GitHub
---
### Git이란?
> 분산형 버전 관리 시스템. 파일을 버전별로 저장하므로 관리하고 수정하기 좋음
- 저장소 구조
![Git](https://hg-edu.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F7142d992-3d01-481c-9d4e-e818c6e185d8%2FUntitled.png?table=block&id=21898201-d9ba-411d-bcb1-edc47c377142&spaceId=f7ab64f0-6613-4035-b609-06b6865d9b61&width=2000&userId=&cache=v2)
  - Working Directory: 사용자의 작업 공간
  - Staging Area: add했을 때 파일이 저장되는 곳
  - Repository: commit한 결과물이 저장되는 곳
- git 명령어
  1. git init: 현재 디렉토리를 git으로 관리하겠다는 선언
  2. git status: 현재 파일의 저장 상태를 보여 줌
  3. git add: 사용자가 컴퓨터에 저장한(Ctrl + s) 파일을 Staging area에 올리는 명령어
  4. git commit: Staging area에 저장한 파일을 commit으로 저장, 하나의 버전을 만드는 명령어
  5. git log: 이 git의 commit 내역을 조회
### GitHub란?
> 무료 Git 저장소로, 온라인에 repository를 올려 유저들끼리 공유하고 참조할 수 있음
- 원격 저장소: 로컬 저장소와 원격 저장소를 연결하는 과정을 거쳐야 함
  - git remote: 로컬 저장소에 원격 저장소를 등록
    - 등록: git remote add <이름> <주소>
    - 조회: git remote -v
    - 연결 해제: git remote rm <이름>
  - git push: 로컬 저장소에 commit한 것을 원격 저장소에 업로드
    - git push <저장소 이름> <브랜치 이름>
    - git push -u <저장소 이름> <브랜치 이름>으로 하면 즐겨찾기가 되어, 이후에는 git push만 쳐도 업로드됨