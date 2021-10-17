클라이언트(사용자): 데이터 발생(입력) 
웹 서버: 웹을 통해서 클라이언트에 요청을 받고, 클라이언트가 서버에 접속하게 도와줌 (데이터 전송만 가능) 
Application Server: 웹 서버와 데이터베이스를 연결해줌 

=> 합쳐서 WAS(Web Application Server)를 이용하기도 함

@WebServlet("/HelloServlet")//servlet을 접근할 이름을 annotation으로 설정
www.ssafy.com/HelloServlet이런식

4로 시작하는 error -> client 에러
5로 시작하는 error -> server 에러

파라미터를 이용해서 client -> server로(name을 따라감)

servlet -> java에 html을 삽입
jsp -> html에 java를 삽입

server page

jsp, asp, php

jsp 스크립팅 요소들
1. 선언 
<%! 멤버변수나 메서드 % >

2. 스크립트릿
client 요청시 매번 호출되는 영역으로, servlet변환시 service method에 해당하는 영역, response, request에 관련된 코드
<% ~~~ % >

3. 표현식
데이터를 브라우저에 출력할때에 사용
= out.print
<%= 문자열 % >

4. 주석
<%-- 주석내용 --% >
html주석과 다른점 -> 자바가 서버영역에서 먼저 실행되기때문에.. 실행순서에 의해 다르다

jsp 지시자(directive)
어떻게 jsp 페이지를 처리할것인가에 대한 정보를 제공
모든 jsp에선 session을 사용할 수 있음

jsp에서는 servlet과달리 request, response, session, out, application 등 기본 객체가 존재하여, 선언하지 않아도 사용이 가능하다
application은 web application 프로젝트 처리와 관련된 객체를 의미한다

jsp기본객체의 영역 - 크기별
application > session > request > pagecontext
전체 -> 인가된 사용자 -> 페이지에서 페이지

웹페이지 이동
foward(request, response) - 전달
내가만든 서버 프로젝트 내에서만 전달가능 - 외부 경로로는 불가능

sendRedirect(location)
http로부터해서 context root 밑의 모든 경로를 다써줘야함
외부 경로로포함 다른경로 가능

page context -> request -> session -> application
                    fowarding

foward & redirect
페이징의 동작임에는 유사한것처럼 보이나 둘은 완전히 다르다

request
client -> web server

redirect
서버 내에서 진행하는 ... 요청자들의 작업들을 처리(응답의 유형 ex) html, json, xml, redirect ....)

response
web server -> client
서버에서 java code 수행 후 response 보냄
