# 네트워크 - 면접대비

### Q. OSI 7계층에 대해 설명할 수 있나요?
![7](https://user-images.githubusercontent.com/44339530/114519390-55d70f00-9c7b-11eb-8290-87fbc8bac1d3.png)<br>

- 1 계층(물리 계층)
    - 케이블의 종류나 커넥터 등과 같은 전송에 필요한 <b> 두 장치간의 실제 접속과 관련된 물리적인 특성에 대한 규칙을 정의</b>
    - 데이터를 전기 신호로 바꾸어주는 계층
    - 전송단위: 비트(Bit)
    - 장비: 케이블의 종류(UTP 케이블, 동축 케이블), 허브

- 2 계층(데이터 링크 계층)
    - 물리적으로 연결되어 있는 호스트끼리의 통신을 담당
    - 시스템들 간의 신뢰성을 보장하며 오류 검출과 오류제어 기능을 수행
    - 송신 측과 수신측의 속도차이를 해결하기 위한 흐름 제어 기능을 수행
    - 전송단위: 프레임(Frame)
    - 장비: 브릿지, 스위치
    - 프로토콜: 이더넷

- 3 계층(네트워크 계층)
    - 데이터가 원하는 목적지까지 성공적으로 전달되도록(가장 빠르게) 하는 역할을 담당
    - 전송단위: 패킷(Packet)
    - 장비: 라우터
    - 프로토콜: IP, ICMP, ARP

- 4 계층(전송 계층)
    - 프로세스간의 통신을 담당
    - 포트 번호를 정의하고 오류 및 흐름제어, 다중화를 수행
    - 전송단위: 세그먼트(segment)
    - 장비: TCP, UDP
    - 프로토콜: 게이트, L4스위치

- 5 계층(세션 계층)
    - 응용 프로세스가 통신을 관리하기 위한 방법을 제공
    - 컴퓨터끼리 통신을 하기 위해 세션을 만드는 계층
    - 전송단위: 데이터(Data)
    - 프로토콜: NetBIOS, SSH, TLS

- 6 계층(표현 계층)
    - 데이터의 형식(format)을 정의하는 계층
    - 예를 들어, 동영상 파일, 그림 파일, 문서 파일 등
    - 세션계층에서 받은 데이터를 응용계층으로 보내기 전에 통신에 적당한 형태로 변환(반대로 응용계층에서 세션계층으로 보내기전에도 변환하기도 함)
    - 프로토콜: JPEG, MPEG
- 7 계층(응용 계층)
    - 사용자와 직접 상호작용하는 응용프로그램들이 포함된 계층
    - 대표적으로 전자메일, 파일전송등의 서비스가 있음
    - 프로토콜: DNS, FTP, HTTP
- 출처: https://quro07.tistory.com/4

### Q. HTTP와 HTTPS의 차이에 대해 설명할 수 있나요?
![8](https://user-images.githubusercontent.com/44339530/114519995-eca3cb80-9c7b-11eb-8de3-c844ebe80c6d.png)<br>
- HTTP는 평문 데이터를 전송하는 프로토콜이기 때문에 비밀번호나 주민번호 등을 주고 받으면 제3자에 의해 조회될 수 있습니다. 이러한 문제를 해결하기 위해 HTTP에 암호화가 추가된 프로토콜이 HTTPS입니다. HTTPS는 CA로 부터 자신의 공개키를 갖는 인증서를 발급하여 보내는 메시지를 공개키로 암호화하도록 하고 있습니다. 공개키로 암호화된 데이터는 개인키로만 복호화가 가능하기에 제3자가 원본 데이터를 조회 할 수 없게 됩니다.

#### 출처
- https://mangkyu.tistory.com/91