# Unity CLI MCP 사용설명서
- 종류: 유튜브 영상
- 링크: https://youtu.be/6A-hEWNxObY?si=yYZH0BjabKY4b1J7
- 시작일: 2026-09-22

## Unity CLI
- 텍스트로만 구성된 명령어를 통해 작업을 수행하는 인터페이스
- CLI을 통해서 원격으로 유니티를 조작

## Unity CLI 시작하기
1. 유니티 허브를 통해 cli 설치
2. 터미널에 `unity`를 쳐서 시작
3. `unity --version`으로 버전 확인, `unity upgrade`로 버전 업그레이드
4. `unity auth login`으로 로그인, `unity license activate`로 라이센스 활성화
5. `unity editors`를 통해서 설치할 수 있는 에디터 목록이 뜸, `unity install lts`을 통해서 에디터 설치
6. `unity templates list`를 통해서 해당 버전에서 제공하는 템플릿이 뜸, 여기서 원하는 템플릿을 복사
7. `unity projects new 'name' --template '6번 단계 복사한 템플릿' --editor-version '에디터 버전'`
8. 생성한 프로젝트 경로로 이동 후 `unity open`을 통해서 해당 프로젝트를 열 수 있음

## Unity Pipeline
- 유니티의 새로운 워크플로우
- 유니티 Pipeline패키지를 통해서 유니티 에디터 바깥에서 다양한 환경을 통해 작업 수행 가능
- ex: Terminal, Custom UI, AI Agent

## Unity CLI Mcp
- 새로운 워크플로우 아래의 MCP
- 이제 에디터에서 MCP를 연결하는 것이 아닌 CLI에서 MCP를 연결
- 에디터에서 오버헤드를 발생시키지 않고 여러 AI 모델과 함께 개발 작업을 수행

## Unity MCP 시작하기
1. 사용하고자 하는 AI 설치
2. `unity mcp configure 'agent'` configure 명령어를 통해 지원하는 MCP 목록을 확인하고 알맞은 이름을 골라서 구성 파일 생성
3. AI 스킬 주입, `github.com/Unity-Technologies/skills` 유니티 관련 스킬이 작성된 깃허브에서 파일 다운로드
4. AI 프로젝트 추가, 생성해둔 유니티 프로젝트 폴더를 AI의 프로젝트 루트 폴더로 지정, Unity CLI 테스트를 위해 프로젝트 실행을 스킬로 작업하도록 프롬프트 작성
5. 파이프라인 설치, `unity pipline install`로 파이프라인 설치, 하지만 유니티 스킬을 습득한 AI Agent는 알아서 Pipeline 패키지 설치를 권장
6. MCP 연결, `unity status` Unity CLI에서 MCP 상태를 점검 가능, 이후 에디터를 열어둔 상태로 AI에서 MCP 접속 명령
7. CLI 게임 개발, 잘 정돈된 계획을 전달하여 AI 스스로 CLI 명령어를 사용하여 장면 및 스크립트, 에셋 제작 및 조립과 테스트 진행
