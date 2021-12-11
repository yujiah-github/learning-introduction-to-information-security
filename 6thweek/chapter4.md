정보보호개론 6주차 - 4장 요약 과제
정보통신공학전공
201814140 유지아


웹과 HTTP의 이해
1-1. 웹의 이해
웹의 정식 명칭은 ‘월드 와이드 웹’ 이다. 웹은 세계적 규모의 거미집 또는 거미집 모양의 망이라는 뜻으로, 1989년 스위스 제네바의 유럽입자물리연구소 CERN에서 근무하던 팀 버너스 리가 연구 목적의 프로젝트로 시작했다.

1-2. HTTP 프로토콜
웹에서는 HTTP, SMTP, POP, FTP, Telnet 등 여러 프로토콜이 쓰인다. 가장 흔히 쓰이는 것은 HTTP이다. 이것을 이용하면 다양한 응용 프로그램에 접근하여 텍스트, 그래픽, 애니메이션을 보거나 사운드를 재생할 수 있다. HTTP는 웹 처리 전반에 걸친 토대가 되기 때문에 웹 서버를 HTTP 서버라고 부르기도 한다.

1-3. HTTP Request
GET, POST 등이 있다. get은 가장 일반적인 형태로 요청 데이터의 인수를 웹 브라우저의 URL을 통해 전송한다. post는 hTTP 헤더에 데이터를 전송한다. 내부의 구분자가 파라미터를 구분하고 서버가 각 구분자에 대한 내용을 해석하여 데이터를 처리하기 때문에 get 방식에 비해 처리 속도가 상대적으로 느리다.

1-4. HTTP Response
서버에서 쓰이는 프로토콜 버전, request에 대한 실행 결과 코드 및 간략한 실행 결과 설명문에 대한 내용이 담겨 있다. 100번대는 정보 전송, 200번대는 성공, 300번대는 리다이렉션, 400번대는 클라이언트 측 에러, 500번대는 서버 측 에러 등을 의미한다.

2. 웹 서비스의 이해
2-1. 프론트엔드
프론트엔드는 클라이언트, 즉 웹 브라우저에서 실행되는 프로그램 영역을 말한다. 그런 프로그램 중 가장 단순한 형태가 HTML이다. 웹 서버에 HTML 문서를 저장하고 있다가 클라이언트가 특정 HTML 페이지를 요청하면 해당 문서를 클라이언트에 전송한다. 클라이언트는 이 웹 페이지를 해석하여 웹 브라우저에 표현해주는데, 이런 웹 페이지를 정적인 웹 페이지라고 한다.

2-2. 백엔드
백 엔드는 웹 서비스를 제공하는 데 필요한 REST API를 제공하는 영역으로 흔히 JAVA, .NET,파이썬, 루비 자바스크립트 등이 사용된다. 백 엔드의 역할은 아주 단순한데, 클라이언트에 구현된 기능에 필요한 인자를 전달받고, 이 인자에 따라 함수처럼 그에 대한 결과만 전달한다. 함수는 URL에 따라 구분되며, 보통 그 결과는 제이슨 형태로 클라이언트에 전달된다.

3. 웹 해킹
웹 해킹은 웹 사이트의 구조와 동작 원리를 이해하는 데서부터 시작한다. 웹 스캔, 웹 프록시를 이용한 패킷 분석, 구글 해킹 등이 사용된다.

3-1. 웹 프록시를 통한 취약점 분석
웹 프록시는 웹의 구조를 파악하거나 취약점을 점검할 때 혹은 웹 해킹을 할 때 사용하는 툴이다. 일반적으로 웹 해킹에 사용되는 웹 프록시는 클라이언트에 설치되고 클라이언트의 통제를 받는다. 즉, 클라이언트가 웹 서버와 웹 브라우저 간에 전달되는 모든 HTTP 패킷을 웹 프록시를 통해 확인하면서 수정할 수 있다.

3-2. 구글 해킹을 통한 정보 수집
site: 특정 도메인으로 지정한 사이트에서 검색하려는 문자열이 포함된 사이트를 찾는다.
Filetype: 특정 파일 유형에 지정한 사이트에서 검색하려는 문자가 들어 있는 사이트를 찾는다.
Link: 링크로 검색하는 문자가 들어있는 사이트를 찾는다.
Cache: 특정 검색어에 해당하는 캐시된 페이지를 보여준다.
Intitle: 페이지 제목에 검색하는 문자가 들어있는 사이트를 찾는다.
Inurl: 페이지 url 에 검색하는 문자가 들어있는 사이트를 찾는다.

3-3. 웹의 주요 취약점
명령 삽입 취약점
클라이언트 요청을 처리하기 위해 전송받는 인수에 특정 명령을 실행하는 코드를 포한하여 웹 서버에 전송하고 실행한다.
웹 서비스가 예외적인 문자열을 적절히 필터링 하지 못하는 경우에 발생한다.
명령 삽입 공격의 대표적인 형태는 SQL 삽입 공격이다.

인증 및 세션 관리 취약점
취약한 패스워드 설정: 취약한 인증의 가장 대표적인 문제점은 패스워드 설정으로, 웹을 비롯해 패스워드를 사용하는 모든 운영체제와 응용 프로그램에 공통으로 해당한다.
사용자 데이터를 이용한 인증: 데이터 신뢰도에 대한 증명 권한을 클라이언트에 넘기면 클라이언트가 권한을 악용할 수 있다.

Xss 취약점
공격자가 작성한 스크립트가 다른 사용자에게 전달 되는 것이다.
다른 사용자의 웹 브라우저 안에서 적절한 검증 없이 실행되기 때문에 사용자의 세션을 탈취하거나 웹 사이트를 변조하고 악의적인 사이트로 이동할 수 있다.

보안 설정 오류
디렉터리 리스팅: 웹 브라우저에서 웹 서버의 특정 디렉터리를 열면 그 디렉터리에 있는 파일과 목록이 모두 나열되는 것을 말한다.
백업 및 임시 파일 존재: 공격자는 개발자가 남겨둔 백업 파일이나 임시 파일을 통해 중요한 정보를 획득할 수 있다.
미흡한 주석 관리: 주석에는 여러 가지 정보가 기록되므로 주의가 필요하다.

공격 방어 취약점
웹 애플리케이션에서 공격의 탐지, 로깅, 응답 및 공격 시도 차단을 수행해야 한다.

취약한 API
보안에 취약한 API 사용은 보안 문제를 초래할 수 있으므로 충분히 검토해야 한다.

4. 웹 취약점 보안
- 특수 문자 필터링
Xss 취약점 공격: <, >, &, ?, / 등
SQL 삽입 공격: =, ; ,* 등
- 서버 통제 작용
- 지속적인 세션 관리