■ 작업 순서
부모 저장소 -> Fork -> 내 저장소 -> Cloning(깃허브데스크탑) -> 내 데스크탑
내 데스크탑 -> push origin -> 내 저장소 -> pull request(깃허브) -> 부모 저장소

■ vscode 기능
파란색 - 수정 / 초록색 - 추가
M - modified
U - untracked
A - added
HEAD -> main --/ 내 컴퓨터의 main브런치로 커밋, HEAD: 이전 커밋들이 모두 합쳐졌다는 의미 그리고 '현재위치'를 표시함
origin/main --/ origin: 원격저장소(github.com), main: main브런치

■ 원격 저장소 연결 [remote]
git remote add origin <주소> --/ remote: 원격저장소관리명령어, add: 추가명령어, origin: 이름(다른이름사용가능)

■ 원격 저장소 리스트 [remote]
git remote -v

■ 원격 저장소 연결삭제
git remote remove <이름>

■ 커밋 이력 보기 [log]
git log

■ log 나오기
'q'

■ stage 영역에 추가(커밋되기 전 영역) [add]
git add <파일명>
git add . (현재 폴더에 있는 모든 파일)

■ git 커밋하기 [commit]
git commit -m "<메시지>" --/ -m: 메시지라는 뜻

■ 원격저장소에 올리기(github.com) [push]
git push origin main(생략가능 1개뿐이면) --/ git을 push한다 origin(원격저장소이름)에 main(컴퓨터브랜치이름)내용을

■ 원격저장소의 커밋내용 받기 [pull]
git pull origin main --/ origin의 내용을 내 컴퓨터 main브랜치로 받는다

■ 원격저장소 복제 [clone]
git clone <저장소 주소> <폴더이름(생략가능)>

■ 커밋시점 이동하기 [checkout]
git checkout <커밋 id> --/ 커밋 id는 git log를 이용하면 보임

■ 현재시점커밋으로 이동하기 [checkout]
git checkout main

■ 현재커밋을 삭제하고 과거커밋으로 이동 [reset]
git reset --hard HEAD^ --/ reset: 상태변경, hard: 삭제, HEAD: 현재위치, ^: 단계(^=1단계뒤, ^^=2단계뒤). 커밋내용(파일)을 '삭제'하고 과거커밋으로 돌아감
예) git reset --soft HEAD^ --/ 과거커밋으로 돌아가면서 커밋직전 상태(stage)로 돌아감
예) git reset HEAD^ --/ mixed reset이라고 하며 과거커밋으로 돌아가면서 파일들이 커밋전 상태(unstage)로 돌아감

■ 현재커밋을 삭제하고 과거커밋으로 이동하고 다시 커밋작업을 하고싶을 경우 원격저장소의 커밋내용도 과거로 돌려야함
git push origin main --force --/ 원격저장소로 현재커밋을 강제로 push (문제가 생겨도 그냥 덮어씀)

■ 새로운 브랜치 생성 [checkout]
git checkout -b <브랜치 이름> --/ -b: 브랜치

■ 브랜치 리스트 보기
git branch

■ 브랜치 삭제
git branch -d <브랜치이름> --/ d: 삭제명령

■ 마지막 커밋 수정
git commit --amend --no-edit --/ amend: 수정하다, no-edit: 메시지를 수정하지 않는다. 현재작업중인파일을 마지막 커밋에 추가하는 기능
예)git commit --amend -m "<메시지>" --/ 커밋의 메시지를 수정하다

■ 깃 상태 표시
git status

■ 깃 제외파일 생성
touch .gitignore

■ 깃 stage에 있는 파일 삭제
git rm -r <폴더이름>/ --cashed --/ rm: 삭제명령, -r: 폴더삭제명령, (이름)/: 폴더라면 이름뒤에 '/'를 넣어준다, cashed: 캐쉬된 파일들(stage영역에 있다면 캐쉬됬다는 의미)