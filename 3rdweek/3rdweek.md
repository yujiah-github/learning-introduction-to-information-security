## 정보보호개론 3주차 - 3장 요약 과제

1. 네트워크의 이해
1-1 OSI 7계층의 이해
OSI 7계층은 ISO(국제표준화기구)가 다양한 네트워크 간의 호환을 위해 만든 표준 네트워크 모델이다. 

1-(1) 물리 계층(1계층)
1계층인 물리 계층은 시스템 간의 연결을 의미하는 것으로 가장 쉽게 이해할 수 있다. 물리 계층은 간단하지만 네트워크에서 매우 중요하다. 실제 장치를 연결하기 위한 전기적, 물리적 세부 사항을 정의한 계층으로 랜선 등이 포함됨.

1-(2) 데이터 링크 계층(2계층)
2계층인 데이터 링크 계층은 두 포인트 간의 신뢰성 있는 전송을 보장하기 위한 계층으로, CRC 기반의 오류 제어 및 흐름 제어가 필요하다. 네트워크 위의 개체 간에 데이터를 전달하며, 물리 계층에서 발생할 수 있는 오류를 찾아내고 수정하는 데 필요한 기능적, 절차적 수단을 제공한다. 두 지점 간의 신뢰성 있는 전송을 보장하기 위한 계층이며, 16진수 12개로 구성된 MAC 주소를 사용한다.

1-(3) 네트워크 계층(3계층)
3계층인 네트워크 계층은 여러 개의 노드를 거칠 때마다 경로를 찾아주는 역할을 한다. 이 계층은 다양한 길이의 데이터를 네트워크를 통해 전달하며 그 과정에서 라우팅, 흐름 제어, 세그먼테이션, 오류 제어 등을 수행한다. 네트워크 계층에서 동작하는 라우터가 스위치도 있는데, 스위치의 경우 보통 L3 스위치라고 부른다.

1-(4) 전송 계층(4계층)
4계층인 전송 계층은 양 끝 단의 사용자들이 신뢰성 있는 데이터를 주고받을 수 있게 하여 상위 계층이 데이터 전달의 유효성이나 효율성을 신경 쓰지 않게 해준다. 전송 계층은 시퀀스 넘버 기반의 오류 제어 방식을 사용하여 특정 연결을 유효성을 제어하며, 일부 프로토콜은 상태 개념이 있고 연결 지향형이다. 이러한 특성은 전송 계층에서 패킷 전송이 유효한지 확인하고 전송에 실패한 패킷은 다시 전송한다는 것을 의미한다.

TCP는 패킷을 주고받기 전에 미리 연결을 맺어 가상 경로를 설정하는 연결 지향형 프로토콜로, TCP에는 연결을 설정하는 과정과 연결을 종료하는 과정이 존재한다. 이 중 연결 설정 과정은 ‘3-웨이 핸드셰이킹’ 이라고 한다.

1-(5) 세션 계층(5계층)
5계층인 세션 계층은 양 끝 단의 응용 프로세스가 통신을 관리하는 방법을 제공한다. 세션 계층은 동시 송수신 방식, 반이중 방식, 전이중 방식의 통신과 함께 체크 포인트, 유휴, 종료, 다시 시작의 과정을 수행한다. 또한 TCP/IP 세션을 만들고 없애는 책임을 진다. 전송 계층이 끝단 간의 논리적인 설정을 담당한다면 세션 계층은 이런 연결에 정보 교환을 효과적으로 할 수 있도록 추가 서비스를 한다.

1-(6) 표현 계층(6계층)
6계층인 표현 계층은 코드 간의 번역을 담당한다. 사용자 시스템에서 데이터 구조를 하나의 통일된 형식으로. 표현하여 응용 프로그램 계층의 데이터 형식 차이로 인한 부담을 덜어주는 것이다. 

1-(7) 응용 프로그램 계층(7계층)
7계층인 응용 프로그램 계층은 사용자나 응용 프로그램 사이에 데이터 교환이 가능하게 하며, 응용 프로세스와 직접 관계하여 일반적인 응용 서비스를 수행한다.  

2.서비스 거부 공격 : DoS와 DDoS
서비스 거부 공격은 다른 해킹에 비해 비교적 간단한 것으로 일종의 훼방이라고 볼 수 있다. 반면에, 분산 서비스 거부 공격은 공격자가 한 지점에서 서비스 거부 공격을 수행하는 것을 넘어 광범위한 네트워크를 이용하여 다수의 공격 지점에서 동시에 한 곳을 공격하는 형태의 서비스 거부 공격이다.

2-(1) 서비스 거부 공격
취약점 공격형과 자원 고갈 공격형으로 구분할 수 있다. 취약점 공격형은 특정 형태의 오류가 네트워크 패킷을 처리 오직에 문제가 있을 때 공격 대상이 그 문제점을 이용하여 오작동의 유발하는 형태이다. 자원 고갈 공격형은 네트워크 대역폭이나 시스템의 CPU, 세션 등의 자원을 소모시키는 형태다.

2-(2) 보잉크/봉크/티어드롭 공격
보잉크, 봉크, 티어드롭 공격은 프로토코릐 오류 제어 로직을 악용하여 시스템 자원을 고갈시키는 방식이다. TCP 프로토콜은 데이터 전달의 유효성이나 효율성을 높이기 위해 시퀀스 넘버 기반의 오류 제어 방식을 사용하여 특정 연결의 유효성을 제어한다.

2-(3) 랜드 공격
랜드 공격은 시스템을 나쁜 상태에 빠뜨리는 것으로 방법도 아주 간단하다. 패킷을 전송할 때 출발지 IP 주소와 값을 똑같이 만들어서 공격 대상에게 보내는 것이다. 이 때 조작된 목적지 IP 주소는 공격 대상의 IP 주소여야 한다.

2-(4) 죽음의 핑 공격
죽음의 핑 공격은 NetBIOS 해킹과 함께 시스템을 파괴하는 데 가장 흔히 쓰인 초기의 DoS 방법이다. 이메일로 10MB 파일을 보내면 10MB 크기의 데이터 패킷 하나가 통째로 가는 것이 아니라 수천 개의 패킷으로 나뉘어 전송되는 것처럼 네트워크에서도 전송하기 적당한 크기로 패킷을 잘라서 보내는데, 이런 특성을 이용한 공격이다.

2-(5) SYN 플러딩 공격
SYN 플러딩 공격은 동시 사용자 수 제한을 이용하는 것으로, 존재하지 않는 클라이언트가 서버별로 한정된 접속 가능 공간에 접속한 것 처럼 속여 다른 사용자가 서비스를 제공받지 못하게 한다.

2-(6) HTTP GET 플러딩 공격
HTTP GET 플러딩 공격은 공격 대상 시스템에 TCP-3 웨이 핸드세이킹 과정으로 정상적으로 접속한 뒤, HTTP의 GET 메서드를 통해 특정 페이지를 무한대로 실행하는 공격이다.

2-(7) HTTP CC 공격
HTTP 1.1 버전의 CC 헤더 옵션은 자주 변경되는 데이터에 새로운 HTTP 요청 및 응답을 요구하기 위해 캐시 기능을 사용하지 않도록 할 수 있다. 서비스 거부 공격에 이를 응용하려면 ‘Cache-Control’ 옵션을 사용해야 한다.

2-(8) 동적 HTTP 리퀘스트 플러딩 공격
HTTP GET 플러딩 공격이나 HTTP CC 공격은 대개 지정된 웹 페이지를 지속적으로 요청하는 서비스 거부 공격이다. 그러나 이 두 가지 공격은 웹 방화벽에서 특징적인 HTTP 요청 패턴을 확인하여 방어할 수 있다. 동전 HTTP 리퀘스트 플러딩은 이러한 차단 기법을 우회하기 위해 지속적으로 요청 페이지를 변경하여 웹 페이지를 요청하는 기법이다.

2-(9) 슬로 HTTP 헤더 DoS 공격
슬로 HTTP 헤더 DoS 공격은 서버로 전달할 HTTP 메시지의 헤더 정보를 비정상적으로 조작하여 웹 서버가 헤더 정보를 완전히 수신할 때 까지  연결을 유지하도록 하는 공격이다. 그 결과 시스템 자원을 소비시켜 다른 클라이언트의 정상적인 서비스를 방해한다.

2-(10) 슬로 HTTP POST 공격
슬로 HTTP POST 공격은 2010년 11월 미국 워싱턴에서 개최된 2010 OWASP에서 소개된 것으로, 웹 서버와의 커넥션을 최대한 오래 유지하여 웹 서버가 정상적인 사용자의 접속을 받아들일 수 없게 하는 공격 방식이다.

2-(11) 스머프 공격
스머프 공격은 ICMP 패킷과 네트워크에 존재하는 임의의 시스템을 이용하여 패킷을 확장함으로써 서비스 거부 공격을 수행하는 것으로, 네트워크를 공격할 때 많이 사용된다. 스머프 공격을 더 정확하게 이해하려면 다이렉트 브로드캐스트를 알아야 한다.

2-(11) 메일 폭탄 공격
메일 폭탄은 스팸 메일과 같은 종류이다. 메일 서버는 각 사용장에게 일정한 양의 디스크 공간을 할당하는데 메일이 폭주하여 디스크 공간을 가득 채우면 정작 받아야 할 메일을 받을 수 없기 때문이다.

2-2. 분산 서비스 거부 공격(DDoS)
분산 서비스 거부 공격은 미네소타 대학에서 처음 발생하여 야후 등의 서버 서비스를 중지시켰다. 피해가 상당히 심각했으나 아직까지 확실한 대책이 없으며 공격자의 위치와 구체적인 발원지를 파악하는 것도 거의 불가능하다.
분산 서비스 거부 공격에 사용되는 명칭과 구조는 다음과 같다.

공격자 : 공격을 주도하는 해커의 컴퓨터
마스터 : 공격자에게 직접 명령을 받는 시스템. 여러 대의 에이전트를 관리한다.
핸들러 프로그램 : 마스터 시스템의 역할을 수행하는 프로그램
에이전트 : 공격 대상에 직접 공격을 가하는 시스템
데몬 프로그램 : 에이전트 시스템 역할을 수행하는 프로그램

3. 스니핑 공격
‘sniff’는 ‘코를 킁킁 거리다’ 라는 뜻으로, 스니핑은 코를 킁킁 거리면서 음식을 찾는 동물처럼 데이터 속에서 정보를 찾는 것이라고 생각하면 쉽게 이해할 수 있다.

3-1 스니핑 공격의 원리
기본적으로 네트워크에 접속하는 모든 시스템은 설정된 IP 주소와 고유한 맥 주소를 가지고 있다. 통신을 할 때 네트워크 카드는 이 두가지 정보로 자신의 랜 카드에 들어오는 프로토콜 형식에 따른 전기적 신호의 헤더 부분, 즉 패킷의 IP 주소와 MAC 주소를 인식하고 자신의 버퍼에 저장할 지를 결정한다.

3-2. 스니핑 공격의 종류
3-2-(1)	스위치 재밍 공격
OSI 7계층을 설명할 떄 스위치에 포트와 맥 주소를 저장한 테이블이 있다고 한 것을 기억할 것이다. 스위치 재밍은 스위치가 맥 주소 테이블을 기반으로 패킷을 포트에 스위칭 기능을 마비시키는 공격을 말한다. 이러한 스위치 재밍 공격을 MACOF 공격이라고도 한다.

3-2-(2) SPAN 포트 태핑 공격
SPAN은 스위치의 포트 미러링 기능을 이용한다. 포트 미러링이란 각 포트에 전송되는 데이터를 미러링하는 포트에도 똑같이 보내는 것으로, 침입 탐지 시스템을 설치하거나 네트워크 모니터링을 할 때 또는 로그 시스템을 설치할 때 많이 사용한다.

3-3. 스니핑 공격의 탐지
스니핑 공격은 스니퍼를 설치한  이후에는 네트워크에 별다른 이상 현상을 일으키지 않기 때문에 사용자가 이를 인지하기 어려워 능동적인 탐지를 통해서만 잡아낼 수 있다. 

3-3-(1) ping을 이용한 스니퍼 탐지
대부분의 스니퍼는 일반 TCP/IP 에서 동작하기 떄문에 request 를 받으면 response를 전달한다. 이를 이용하여 의심이 가는 호스트에 ping을 보내면 스니퍼를 탐지할 수 있는데, 이때 네트워크에 존재하지 않는 맥 주소를 위장해서 보낸다.

3-3-(2)ARP를 이용한 스니퍼 탐지
ping을 이용하는 것과 유사한 방법으로, 위조된 ARP request를 보냈을 때 ARP response가 오면 프러미스큐어스 모드로 설정되어 있는 것이다.

3-3-(3) DNS를 이용한 스니퍼 탐지
일반적으로 스니핑 프로그램은 사용자의 편의를 위해 스니핑한 시스템의 IP 주소에 DNS에 대한 이름 해석 과정인 Reverse-DNS lookup을 수행한다.

3-3-(4) 유인을 이용한 스니퍼 탐지
스니핑 공격을 하는 공격자의 주요 목적은 아이디와 패스워드 획득이다. 보안 관리자는 이 점을 이용하여 가짜 아이디와 패스워드를 네트워크 계속 뿌리고, 공격자가 이 아이디와 패스워드를 접속을 시도할 때 스니퍼를 탐지한다.

3-3-(5) ARP watch를 이용한 스니퍼 탐지
ARP watch는 맥 주소와 IP 주소의 매칭 값을 초기에 저장하고 ARP 트래픽을 모니터링 하여 이를 변하게 하는 패킷이 탐지되면 관리자에게 메일로 알려주는 틀이다.

4. 스푸핑 공격
‘Spoofing’의 사전적 의미는 ‘속이는 것’이다. 네트워크에서 스푸핑 공격의 대상은 맥 주소, 아이피 주소, 포트 등 네트워크 통신과 관련된 모든 것이 될 수 있다.

4-(1) ARP 스푸핑 공격
ARP 스푸핑은 맥 주소를 속이는 것이다. 공격자의 맥 주소를 로컬에서 통신하고 있는 서버와 클라이언트의 아이피 주소에 대한 데이터 링크 계층의 맥 주소로 속여, 클라이언트에서 서버로 가는 패킷이나 서버에서 클라이언트로 가는 패킷이 공격자에게 향하게 함으로써 랜의 통신 흐름을 왜곡한다.

4-(2) IP 스푸핑 공격
아이피 스푸핑은 쉽게 말해 아이피 주소를 속이는 것으로, 다른 사용자의 아이피를 강탈하여 어떤 권한을 획득한다. 공격자는 신뢰 관계를 맺고 있는 서버와 클라이언트를 확인한 후 클라이언트에 서비스 거부 공격을 하여 연결을 끊는다. 그리고 클라이언트의 아이피 주소를 확보하여 실제 클라이언트처럼 패스워드 없이 서버에 접근한다.

4-(3) ICMP 리다이렉트 공격
ICMP 리다이렉트는 네트워크 계층에서 스니핑 시스템을 네트워크에 존재하는 또 다른 라우터라고 알림으로써 패킷의 흐름을 바꾸는 공격이다.

4-(4) DNS 스푸핑 공격
DNS 스푸핑은 실제 DNS 서버보다 빨리 공격 대상에게 DNS reponse 패킷을 보내어 공격 대상이 잘못된 IP 주소로 웹 접속을 하도록 유도하는 공격이다. 웹 스푸핑과 비슷한 의미로 해석된다.

5. 세션 하이재킹 공격
세션 하이재킹은 말 그대로 ‘세션 가로채기’를 뜻한다. 세션은 ‘사용자와 컴퓨터 또는 두 컴퓨터 간의 활성화된 상태’이므로 세션 하이재킹은 두 시스템 간의 연결이 활성화된 상태, 즉 로그인된 상태를 가로채는 것을 말한다. 가장 쉬운 세션 하이재킹은 누군가 작업을 하다가 잠시 자리를 비웠을 때 몰래 PC 를 사용하여 원하는 작업을 하는 것이다.

TCP 세션 하이재킹은 다음과 같은 단계로 진행이 된다.
(1) 클라이언트와 서버 사이의 패킷을 통제한다. ARP 스푸핑 등을 통해 클라이언트와 서버 사이의 통신 패킷이 전부 공격자를 지나가게 한다.
(2 )서버에 클라이언트 주소로 연결을 재설정하기 위한 RSTreset 패킷을 보낸다. 서버는 패킷을 받아 클라이언트의 시퀀스 넘버가 재설정된 것으로 판단하고 다시 TCP 3-웨이 핸드세이킹을 수행한다.
(3) 공격자는 클라이언트 대신 연결되어 있던 TCP 연결을 그대로 물려받는다.

6. 무선 네트워크 공격과 보안
무선 랜은 유선 랜의 네트워크를 확장하려는 목적으로 사용된다. 따라서 무선 랜을 사용하려면 내부의 유선 네트워크에 AP 장비를 설치해야 한다. 확장된 무선 네트워크는 AP를 설치한 위치에 따라서 통신 영역이 결정되며, 보안이 설정되어 있지 않으면 공격자가 통신 영역 안에서 내부 사용자와 같은 권한으로 공격을 실행할 수 있다.

6-(1) AP 보안
AP 보안을 위한 첫 번째 사항은 물리적인 보안이다. 무선 랜은 공개된 장소에서 접근이 가능하다는 이유로 물리적인 보안을 가볍게 여기는 경우가 많다. 스위치나 라우터는 기업의 네트워크 안정성을 결정짓는 중요한 장비이기 때문에 반드시 물리적인 보안 통제로 적절히 관리하게 마련이다. AP도 스위치의 한 종류이므로 적절한 물리적인 통제가 필요하다.

두 가지 접근 방법은 SSID의 브로드캐스팅 여부에 따라 나뉜다. 무선 랜에서 AP의 존재를 숨기고 싶으면 SSID 브로드캐스팅을 막고 사용자가 SSID를 입력해야 AP에 접속할 수 있게 한다.

6-(2) 무선 랜 통신의 암호화
무선 랜은 통신 과정에서 데이터 유출을 막는 것 뿐 아니라 네트워크에 대한 인증을 위해서도 암호화를 수행한다. 
6-(2)-(1) WEP
WEP는 무선 랜 통신을 암호화 하기 위해 802.11b 프로토콜로부터 적용되었다. 1987년에 만들어진 RC 4 암호화 알고리즘을 기본으로 사용한다. WEP는 64비트와 128비트를 사용할 수 있는데 64비트는 40비트, 128비트는 104비트의 RC 4키를 사용한다.

6-(2)-(2) WPA - PSK
802.11i 보안 표준의 일부분으로 WEP 방식 보안의 문제점을 해결하기 위해 만들어졌다. 802.11i에는 WPA-1 과 WPA-2 규격이 포함되어 있다. 

6-(2)-(3) EAP와 802.1x 암호화
WPA/WPA2-PSK가 기존 WEP의 암호화, 복호화 키 관리 방식을 중점적으로 보완한 것인데 비해 WPA-엔터프라이즈는 사용자 인증 영역까지 보완한 방식이다. WPA-EAP 로도 불리는 WPA-엔터프라이즈 방식은 인증 및 암호화를 강화하기 위해 다양한 보안 표준과 알고리즘을 채택했다.