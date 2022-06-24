# django_polls
voting sites with django and python

## 실행 방법
### 1. image build
`docker build -t dahye913/first_django:1.0.0 .`

### 2. container 생성
`docker run -it -d -v %cd%:/usr/src/app/workspace -p 8000:8000 ahye913/first_django:1.0.0`
- port number : 8000

### 3. 소스 실행
- 해당 container 접속 후, 아래 명령어 수행 
    - `python3 manage.py runserver 0.0.0.0:8000`
> 소스 수정이 용이하고, 다양한 명령어 수행을 위해 이와 같이 작성했습니다.
> container 수행과 동시에 runserver를 실행하고 싶은 경우, dockerfile에서 CMD 명령 주석을 참고하여 변경합니다.

## 웹페이지 설명 
### 1. admin 페이지
- http://127.0.0.1:8000/admin/
    - POLLS 의 Questions에 원하는 질문 등록
    - POLLS 의 Choices에 해당 질문에 부합하는 선택지 등록

### 2. polls 투표 페이지
- http://127.0.0.1:8000/polls/
    - 질문 선택 시, 각 질문의 답변 선택 가능
    - 답변 선택 시, 재 투표 가능