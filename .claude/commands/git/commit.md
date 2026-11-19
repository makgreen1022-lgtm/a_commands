Description

.gitignore 생성, origin 연결, prefix 규칙에 맞춘 커밋까지 한 번에 처리

Git Commit 자동화

아래 순서대로 commit 작업을 진행해 줘. 각 단계는 이미 완료된 상태라면 과감하게 생략하고 다음 단계로 넘어가.

1. .gitignore 생성
생략 조건: 프로젝트 루트에 .gitignore 파일이 이미 있으면 이 단계를 건너뛴다.
생성할 경우 아래 항목을 모두 포함한다.
에디터/IDE: VS Code(.vscode/), JetBrains(.idea/) 등
OS: macOS(.DS_Store 등), Windows(Thumbs.db, desktop.ini 등)
환경변수 파일: .env, .env.*, *.local 등 일반적인 환경변수/비밀 파일
기타 일반 항목: 로그, 캐시, 빌드 산출물, 의존성 폴더(node_modules/ 등)
2. Remote 연결
생략 조건: origin remote가 이미 연결되어 있으면 이 단계를 건너뛴다.
remote 이름: origin
주소: https://github.com/makgreen1022-lgtm/a_commands.git
bash
git remote add origin https://github.com/makgreen1022-lgtm/a_commands.git
3. Commit
입력된 커밋 메시지: $ARGUMENTS
변경 내용과 메시지를 보고 아래 규칙 중 가장 적절한 prefix를 붙여 커밋한다.
형식: <prefix>: <메시지>
커밋 prefix 규칙
prefix	용도
feat	새로운 기능 추가
fix	버그 수정
docs	문서 수정 (README 등)
style	코드 포맷 변경 (세미콜론, 공백 등)
refactor	리팩토링 (기능 변화 없음)
test	테스트 코드 추가/수정
chore	빌드, 설정, 패키지, 기타 작업
perf	성능 개선
ci	CI 설정 수정
build	빌드 시스템 수정
revert	커밋 되돌리기
커밋 메시지 예시 (Few-shot)
입력 ($ARGUMENTS)	결과 커밋 메시지
로그인 기능 추가	feat: 로그인 기능 추가
회원가입 시 이메일 중복 체크 오류 수정	fix: 회원가입 시 이메일 중복 체크 오류 수정
README에 설치 방법 작성	docs: README에 설치 방법 작성
gitignore 추가 및 초기 설정	chore: gitignore 추가 및 초기 설정
유저 서비스 함수 분리	refactor: 유저 서비스 함수 분리
목록 조회 쿼리 속도 개선	perf: 목록 조회 쿼리 속도 개선
GitHub Actions 배포 워크플로 수정	ci: GitHub Actions 배포 워크플로 수정