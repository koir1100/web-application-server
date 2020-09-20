# 실습을 위한 개발 환경 세팅
* https://github.com/slipp/web-application-server 프로젝트를 자신의 계정으로 Fork한다. Github 우측 상단의 Fork 버튼을 클릭하면 자신의 계정으로 Fork된다.
* Fork한 프로젝트를 eclipse 또는 터미널에서 clone 한다.
* Fork한 프로젝트를 eclipse로 import한 후에 Maven 빌드 도구를 활용해 eclipse 프로젝트로 변환한다.(mvn eclipse:clean eclipse:eclipse)
* 빌드가 성공하면 반드시 refresh(fn + f5)를 실행해야 한다.

# 웹 서버 시작 및 테스트
* webserver.WebServer 는 사용자의 요청을 받아 RequestHandler에 작업을 위임하는 클래스이다.
* 사용자 요청에 대한 모든 처리는 RequestHandler 클래스의 run() 메서드가 담당한다.
* WebServer를 실행한 후 브라우저에서 http://localhost:8080 으로 접속해 "Hello World" 메시지가 출력되는지 확인한다.

# 각 요구사항별 학습 내용 정리
* 구현 단계에서는 각 요구사항을 구현하는데 집중한다. 
* 구현을 완료한 후 구현 과정에서 새롭게 알게된 내용, 궁금한 내용을 기록한다.
* 각 요구사항을 구현하는 것이 중요한 것이 아니라 구현 과정을 통해 학습한 내용을 인식하는 것이 배움에 중요하다. 

### 요구사항 1 - http://localhost:8080/index.html 로 접속시 응답
* 1단계는 bufferedreader에 관한 내용이므로, 자바 표준 입출력 관련하여 많이 다뤄봤던 내용이라 조금 찾아보니 되었음.
* 2단계 역시 공백(\\s) 문자를 통해 header 파일에 쓰여진 내용을 분리하는 내용이라 특별히 어려운 부분은 없었음. 다만 유틸 클래스를 통해 단위 테스트를 해야 되는 부분은 수행하지 않았음.
* 3단계는 특별한 부분이 없는 줄 알았는데 책 집필 시점과 현재 웹 수행 과정이 약간 달라서 그런지 CSS 파일을 브라우저에서 표현이 되지 않는 증상이 확인되었다.
* 이를 보완하고자 링크의 맨 마지막 점 이후 단어, 즉 확장자가 css인 경우라면 HTTP 헤더에 text/css 파일이라고 알려주는 부분을 수정하였다. 하지만 굳이 헤더에 content-type을 명시해야 될까? 오히려 생략하니 문제없이 잘 진행되어 의아했다... (9월 21일 0:35)

### 요구사항 2 - get 방식으로 회원가입
* 

### 요구사항 3 - post 방식으로 회원가입
* 

### 요구사항 4 - redirect 방식으로 이동
* 

### 요구사항 5 - cookie
* 

### 요구사항 6 - stylesheet 적용
* 

### heroku 서버에 배포 후
* 