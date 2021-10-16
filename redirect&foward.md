redirect와 foward의 차이

redirect는
web container차원에서의 페이지 이동, 실제로 웹 브라우저에서 client는 다른 페이지로 이동했는지 알수가 없다!
새로운 response와 request가 생성된다.

시스템의 변화가생기는 로직에는 redirect를 서야 새로고침등의 request가 있을경우에 적용되지않음

foward는
사용자가 최초로 요청한 요청정보는 다음 URL에서도 유효하다.  다른 web container에 있는 주소로 이동이 가능하다!

페이지의 이동만 담당
