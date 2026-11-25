# mission1

## 프로젝트 개요
내 컴퓨터에 개발자용 '작업실' 꾸미기

## 실행환경
- Windows
- Docker version 29.9.2
- git version 2.56.0.windows.4

## 수행 항목 체크리스트
 - [O] 터미널 기본 조작 및 폴더 구성
 - 권한 변경 실습
 - Docker 설치/점검
 - [O] hello-world 실행
 - Dockerfile 빌드/실행
 - 포트 매핑 접속(2회)
 - 바인드 마운트 반영
 - 볼륨 영속성
 - [O] Git 설정 + VSCode GitHub 연동

## 검증방법(어떤 명령으로 무엇을 확인했는지) + 결과 위치 링크

## 트러블슈팅 2건 이상(문제 - 원인 가설 - 확인 - 해결/대안) 

##터미널 조작 로그 기록

 - ls          # 파일 목록 (ls -l 은 상세, ls -a 는 숨김 파일 포함)
 - pwd         # 현재 위치 확인
 - mkdir dir   # 폴더 생성
 - cd dir      # 폴더 이동

파일 현재 위치 확인 및 파일 목록

<img alt="image" src="https://github.com/user-attachments/assets/c2f26652-bf6c-484c-a0c9-b1dadcd3a68d" />

폴더 이동 및 폴더 생성

<img alt="image" src="https://github.com/user-attachments/assets/87a9f9e2-68c7-488e-ac08-783c8f37a1ff" />

파일 만들기 및 내용 추가

<img alt="image" src="https://github.com/user-attachments/assets/9793f2c9-1170-492b-9a62-0f4621baf584" />

파일 복사

<img alt="image" src="https://github.com/user-attachments/assets/f5ee65a1-0005-44e6-8d42-b8011211420f" />

## Docker (도커)의 개념

- Docker란 항구 컨테이너에 비유할 수 있습니다.
- 프로그램과 프로그램이 필요한 모든 것을 하나의 박스에 담아서, 어떤 컴퓨터에서든 똑같이 실행되게 해주는 도구입니다.
- (1) Image (이미지) : 설계도
- (2) Container (컨테이너) : 실제로 실행 중인 것
- (3) Dockerfile (레시피) : 이미지를 만들기 위한 레시피


<img alt="image" src="https://github.com/user-attachments/assets/a62e46bc-f68f-4ec7-bfc4-5843369fbc51" />

<img alt="image" src="https://github.com/user-attachments/assets/4f5ca7ab-1f35-451f-aad0-52d17e114d36" />

<img alt="image" src="https://github.com/user-attachments/assets/f6db5b13-0f8d-4529-a126-178bfa924571" />

- 이미지 다운로드

<img alt="image" src="https://github.com/user-attachments/assets/86777bb2-c369-4544-be0d-1b3c3c08c240" />

<img alt="image" src="https://github.com/user-attachments/assets/6276a8d2-3e3e-44d4-8ff0-92e3247d195c" />





## Git과 GitHub의 연동

Git 사용자 정보 및 기본 브랜치 설정

<img alt="image" src="https://github.com/user-attachments/assets/c4992641-af91-4381-92b4-51785e30a27d" />

코드 주소를 복사합니다.

<img alt="image" src="https://github.com/user-attachments/assets/2b3bf178-a754-4e6d-bc73-2c371cb21a9e" />

Git을 GitHub에 연동합니다.

GitHub에 코드를 업데이트 합니다.

<img alt="image" src="https://github.com/user-attachments/assets/8b02130a-278b-4164-9fca-b768a75da00e" />

* 민감한 개인정보는 가렸습니다.

## 절대 경로와 상대 경로의 차이

- 절대 경로: 경남 창원시 마산회원구 합성동 합성로 00
- 상대 경로: 합성동 합성로 00

- 절대 경로: C:\users\nkmn989108\mission1
- 상대 경로: ../../users/nkmn989108




