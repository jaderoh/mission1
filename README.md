# mission1

## 프로젝트 개요
내 컴퓨터에 개발자용 '작업실' 꾸미기

## 실행환경
- Windows
- Docker version 29.9.2
- git version 2.56.0.windows.4

## 중요 개념
- (1) 절대 경로와 상대 경로
- (2) 파일 권한의 의미(r/w/x)와 755, 644 같은 표기의 규칙
- (3) Docker와 Docker의 이미지, 컨테이너, dockerfile
- (4) 포트 매핑이 필요한 이유
- (5) Docker 볼륨(영속 데이터)
- (6) Git과 GitHub의 역할 차이 (로컬 버전관리 vs 원격 협업 플랫폼)

## (1) 절대 경로와 상대 경로의 차이

- 절대 경로: 경남 창원시 마산회원구 합성동 합성로 00
- 상대 경로: 합성동 합성로 00

- 절대 경로: C:\users\nkmn989108\mission1
- 상대 경로: ../../users/nkmn989108

## (2) 파일 권한의 의미(r/w/x)와 755, 644 같은 표기의 규칙
r / w / x의 의미
권한	파일에서	디렉터리에서
- r (read)	내용을 읽을 수 있음	안에 어떤 파일이 있는지 목록을 볼 수 있음 (ls) = 4
- w (write)	내용을 수정할 수 있음	안에서 파일을 만들거나 삭제·이름 변경 가능 = 2
- x (execute)	프로그램/스크립트로 실행할 수 있음	그 디렉터리로 들어갈 수 있음 (cd, 내부 파일 접근) = 1
- owner, group, others 순서로 세 자리로 나열한 게 755, 644 같은 표기이다.

- 명령어 예시: chmod 755 main.py

## (3) Docker와 Docker의 이미지, 컨테이너, dockerfile

- Docker란 항구 컨테이너에 비유할 수 있다.
- 프로그램과 프로그램이 필요한 모든 것을 하나의 박스에 담아서, 어떤 컴퓨터에서든 똑같이 실행되게 해주는 도구이다.
- (1) Image (이미지) : 설계도
- (2) Container (컨테이너) : 실제로 실행 중인 것
- (3) Dockerfile (레시피) : 이미지를 만들기 위한 레시피

## (4) 포트 매핑이 필요한 이유

- 포트 매핑은 호스트의 포트와 컨테이너의 포트를 연결해서 바깥에서 컨테이너 안의 서비스에 접속할 수 있게 해 주는 설정이다.
- 포트 매핑이 주는 이점 :
- 외부 접근 허용: 격리된 컨테이너 안의 서비스를 브라우저나 다른 시스템에서 사용할 수 있다.
- 포트 충돌 방지: 같은 이미지를 여러 개 띄울 때, 컨테이너 내부는 모두 80번이어도 호스트 쪽을 8080, 8081, 8082처럼 다르게 지정해 충돌 없이 실행할 수 있다.
- 선택적 노출: 필요한 포트만 열기 때문에 불필요한 포트가 외부에 노출되지 않아 보안상 유리하다.

## (5) Docker 볼륨(영속 데이터)

- 컨테이너는 기본적으로 임시적이다.
- 컨테이너가 사라져도 남아야 하는 데이터가 영속 데이터(persistent data)인데, DB데이터나 업로드 파일 등이 있다.
- 이를 컨테이너 밖에 저장하는 방법이 볼륨 같은 마운트 기능이다.

- 볼륨 vs 바인드 마운트 :
- 볼륨: DB 데이터, 운영 환경의 영속 데이터 (Docker가 경로와 권한을 관리해 줌)
- 바인드 마운트: 개발 중 소스 코드 공유, 호스트의 설정 파일을 컨테이너에 주입할 때

## (6) Git과 GitHub의 역할 차이 (로컬 버전관리 vs 원격 협업 플랫폼)

- Git은 코드를 업데이트하는 것을 저장하는 버젼 업그레이드 시스템이다.
- GitHub는 Git 저장소(repository)를 인터넷에 올려서 호스팅해 주는 서비스로, 협업 기능을 제공한다. 

## 수행 항목 체크리스트
 - [O] 터미널 기본 조작 및 폴더 구성
 - 권한 변경 실습
 - [O] Docker 설치/점검
 - [O] hello-world 실행
 - [O] Dockerfile 빌드/실행
 - [O] 포트 매핑 접속(2회)
 - [O] 바인드 마운트 반영
 - 볼륨 영속성
 - [O] Git 설정 + VSCode GitHub 연동

## 검증방법(어떤 명령으로 무엇을 확인했는지) + 결과 위치 링크

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

<img alt="image" src="https://github.com/user-attachments/assets/98ee8c96-1a27-434e-a244-c290717319df" />


<도커 삭제>
<img alt="image" src="https://github.com/user-attachments/assets/00428fe0-bdf5-415e-8e7a-d353e7553e94" />

<Dockerfile 빌드/실행>

- app.py
<img alt="image" src="https://github.com/user-attachments/assets/da86c916-7b4c-4beb-b56a-00dc597ebba1" />

- requirements.txt
<img alt="image" src="https://github.com/user-attachments/assets/f8400182-637b-48c2-ad31-453f627c674a" />

- Dockerfile
<img alt="image" src="https://github.com/user-attachments/assets/afcc1c0d-50ac-479b-9f26-26e8f0283313" />


- 터미널
<img alt="image" src="https://github.com/user-attachments/assets/fd2beaf2-28ce-4c9a-b3b3-f7bd16a1c534" />

- Dockerfile 실행하기
<img alt="image" src="https://github.com/user-attachments/assets/6b4971df-07ec-47d3-9ae3-aea425c9d34c" />

<img alt="image" src="https://github.com/user-attachments/assets/3c76aa88-b959-4593-babf-2288bfbcc03b" />

<포트 매핑>

<img alt="image" src="https://github.com/user-attachments/assets/c3d22112-7f66-4365-b886-5d94ceab9dc9" />

 - http://localhost:8081/
<img alt="image" src="https://github.com/user-attachments/assets/e4fe6bda-41a9-4e9f-80c4-ed5448d32584" />

<img alt="image" src="https://github.com/user-attachments/assets/ea3fcb00-284f-4ed6-aa68-41b0a4aeb23e" />


## 바인드 마운트 반영

- 바인드 마운트는 내 PC의 폴더를 컨테이너 안에 그대로 연결하는 방식. 파일을 PC에서 수정하면 컨테이너에 즉시 반영되고, 반대로 컨테이너가 만든 파일도 PC에 남는다.

<img alt="image" src="https://github.com/user-attachments/assets/38ef7d74-20ee-4e41-8a03-404ffbc2cd64" />
<img alt="image" src="https://github.com/user-attachments/assets/ec5bda8c-ec61-4f8c-bc5c-2eac8e91e52c" />



## Git과 GitHub의 연동

Git 사용자 정보 및 기본 브랜치 설정

<img alt="image" src="https://github.com/user-attachments/assets/c4992641-af91-4381-92b4-51785e30a27d" />

코드 주소를 복사합니다.

<img alt="image" src="https://github.com/user-attachments/assets/2b3bf178-a754-4e6d-bc73-2c371cb21a9e" />

Git을 GitHub에 연동합니다.

GitHub에 코드를 업데이트 합니다.

<img alt="image" src="https://github.com/user-attachments/assets/8b02130a-278b-4164-9fca-b768a75da00e" />

* 민감한 개인정보는 가렸습니다.

- Git Log

<img alt="image" src="https://github.com/user-attachments/assets/1e442a38-b211-4fc3-b2da-4ece5da8751d" />

## 트러블슈팅 2건 이상(문제 - 원인 가설 - 확인 - 해결/대안) 

 - 포트 매핑에서 오류가 있었습니다. 원래 돌아가던 이미지를 지우고 다시 dockerfile을 빌드하여 포트매핑을 하니 정상적으로 실행되었습니다.
 - http://localhost:8081/
<img alt="image" src="https://github.com/user-attachments/assets/e4fe6bda-41a9-4e9f-80c4-ed5448d32584" />

<img alt="image" src="https://github.com/user-attachments/assets/ea3fcb00-284f-4ed6-aa68-41b0a4aeb23e" />






