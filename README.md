■ vscode 기능
파란색 - 수정 / 초록색 - 추가
M - modified
U - untracked
A - added
HEAD -> main -- 내 컴퓨터 작업환경 → 내 컴퓨터의 main브런치로 커밋
origin/main -- origin: 원격저장소(github.com), main: main브런치

■ 커밋 이력 보기
git log

■ log 나오기
'q'

■ stage 영역에 추가(커밋되기 전 영역)
git add (파일명)
git add . (현재 폴더에 있는 모든 파일)

■ git 커밋하기
git commit -m "(메시지)" -- -m: 메시지라는 뜻

■ 원격저장소에 올리기(github.com)
git push origin main -- git을 push한다 origin(원격저장소)에 있는 main(브런치이름)에