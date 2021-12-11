# 정보보호개론 10주차 과제

## 암호화
- 암호문: 비밀을 유지하기 위해 당사자만 알 수 있도록 꾸민 약속 기호이다.
- 평문: 누구나 알 수 있게 쓴 일반적인 글이다.

## 기본 암호화 방식
- 전치법 : 단순히 메세지에 들어있는 문자의 위치는 바꾸는 방법이다.
- 후치법: 메시지의 글자를 다른 글자로 대체하여 암호문을 작성하는 방법이다.

## 단일 치환 암호화 방식
- 알파벳 한 글자를 다른 한 글자로 대체하는 방식으로 암호화를 수행한다.
- 단일 치환을 사용한 암호화 방법에는 시저 암호화, 모노 알파베틱 암호화가 있다.

## 다중 치환 암호화 방식
- 단일 치환 방법과 달리, 암호화 키와 매핑하여 알파벳 하나를 여러 가지 다른 알파벳으로 대체해 함호화하는 방법이다.
- 다중 치환을 사용한 암호화 방법에는 비즈네르 암호화, 플레이페어 암호화가 있다.

## 대칭 암호화 방식
- 암호화 키와 복호화 키가 일치하는 방식이다.
- DES 알고리즘: 1977년 1월 NIST가 암호화 표준으로 지정했다. 64비트의 블록 암호화 알고리즘이며 56비트 크기의 키로 암호화한다.
트리플 DES 알고리즘: DES 암호화 키 2개를 이용하여 두 번의 암호화와 한 번의 복호화 또는 두 번의 복호화와 한 번의 암호화를 수행한다.
- AES 알고리즘: 128비트 암호화 블록, 다양한 키의 길이(128/192/256비트)를 갖춘 알고리즘이다. 2000년 10월, 벨기에의 빈센트 레이먼과 요안 다에먼이 개발한 Rijindael 알고리즘이 AES 알고리즘으로 선정되었다.
- SEED 알고리즘: 1999년 2월, 한국인터넷진흥원과 국내 암호 전문가들이 순수 국내 기술로 개발한 128비트 블록의 암호화 알고리즘이다.
- ARIA 알고리즘: 경량 환경 및 하드웨으의 효율성 향상을 위해 개발된 128비트 블록의 암호화 알고리즴이다. 2004년, 국가표준기본법에 의거하여 국가표준으로 지정되었다.
- 양자 암호: 1984년 찰스 베넷과 질 브라샤르가 BB84라는 프로토콜을 통해 제안했다. 양자역학의 복제 불가능성 원리와 측정 후 붕괴라는 특이한 현상을 이용하는 것으로, 단일 광자를 정확하게 측정할 수 있는 기회가 단 한 번으로 제한된다. 이러한 특성 덕분에, 양자 암호 채널을 통해 전달되는 정보가 도청되면 양자 상태가 변경되고 이러한 임의 변경이 데이터 전달에 오류를 일으켜 곧바로 도청을 알아챌 수 있다.
- IDEA 알고리즘: 128비트의 키를 사용하여 64비트의 평문을 8라운드로 돌려 64비트 암호문을 만든다. 모든 연산이 16비트 단위로 이루어지도록 하여 16비트 프로세서에서 구현하기 용이하며 주로 키 교환에 쓰인다.
- RCS 알고리즘: 입출력, 키, 라운드 수가 가변인 블록 알고리즘이다. 32비트, 64비트 128비트 키가 사용되며 속도는 DES의 약 10배이다.
- Skipjack 알고리즘: 미국 국가안보국에서 개발한 클리퍼 칩에 내장된 블록 알고리즘이다. 전화기 등의 음성을 암호화하는 데 주로 사용되며 64비트의 입출력, 80비트의 키를 이용하여 총 32라운드의 암호화 과정을 거친다.
- LEA 알고리즘: 고속 환경 및 모바일 기기 등의 경량 환경에서 기밀성을 제공하기 위해 국내에서 개발한 암호화 알고리즘이다. 128비트 데이터 블록으로 128비트, 192비트, 256비트 비밀 키를 사용할 수 있다.

## 비대칭 암호화 방식
- 암호화 키가 복호화 키가 한 쌍을 이룬다.
- 비대칭 암호화 방식의 발견: 휫필드 디퍼와 마틴 헬먼이 비대칭 암호화 방식을 통한 키 교환 아이디어를 고안했다.
- RSA 알고리즘: 중요 정보를 소수 2개로 표현한 후 두 소수의 곱을 힌트와 함께 전송하여 암호로 사용한다. 충분히 큰 두 소수의 곱에서 두 소수를 찾기 어려운 점을 이용하였다. 오늘날 산업 표준으로 사용하고 있으며 여기에 사용되는 소수는 250자리이다.

### 비대칭 암호화의 기능
- 기밀성 확보를 위한 암호화: 수신자의 공개 키로 암호화하여 송신한다.
- 부인 방지 확보를 위한 암호화: 발신자의 개인 키로 암호화하여 송신한다.

## 해시
### 해시의 특징
- 정보를 숨기기 위한 암호와 달리 해시는 정보의 위조, 변조를 확인하기 위한 것으로, 보안에서 해시를 사용하는 목적은 무결성 확보에 있다.
- 평문의 길이가 달라도 해시 결과 값의 길이는 같다.
- 평문의 내용이 조금만 달라도 해시 값이 완전히 달라진다.

## 해시의 종류
- MD5 알고리즘: 로널드 리베스트가 공개 키 기반 구조를 만들기 위해 RSA와 함께 개발한 것으로 32비트 컴퓨터에 최적화되었다.
- SHA: 160비트의 값을 생성하는 해시 함수로 데이터를 512비트의 블록으로 입력한다.
