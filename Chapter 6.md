# 입출력과 네트워킹

---

## 저수준 I/O 
- 다이오드 : 전기를 한 방향으로만 흐르도록 제한한다.
- DDRB : 데이터 방향 레지스터로 각 핀을 입력으로 쓸지 출력으로 쓸지 결정한다.
- PORTB : 출력 데이터를 저장하는 래치.
- PINB : 핀의 값을 읽는다.

## 버튼을 눌러라
- 다양한 장치는 어떤 종류던지 버튼이나 스위치가 필요하다.
- 인트럽트 요청 : 버튼을 눌리지 않는 경우 1을 만들어주고 , 버튼을 누르면 0을 만든다. 
- 버튼이 눌리면 금속조각이 잠깐 튕겨지면서 인터럽트가 여러 번 발생할 수 있는데 이런 현상은 바람직하지 않다.
   - 해결방안 1 : 최초의 인터럽트시 타이머를 설정하는 방법
   - 해결방안 2 : 인터럽트가 발생할 때마다 기존타이머를 새타이머로 재설정
    
## 빛이 있으라
- 세븐 시그먼트 디스플레이는 일곱개의 LED가 숫자 8의 형태로 나열되어있고 소수점을 표현하는 LED가 있다
- 8개의 LED를 처리하려면 16개의 접점이 필요한데 이를 효율적으로 하기위해 모든 캐소드를 한꺼번에 연결하고 각 애노드마다 별도의 핀에 배정시켜준다.
- 시각의 잔상효과 : 사람의 눈은 24분의 1초보다 짧은 간격으로 깜박거리는 경우 빛이 켜져있는것으로 인식한다.
 
## 밝기 조절
- 디스플레이가 켜져 있는 평균 시간을 조절함으로서 밝기를 조절할 수 있다.

## 그레이의 2ⁿ가지 그림자
- 그레이코드는 연속되는 코드들간의 하나의 비트만 달라지는 인코딩 방법
 
## 쿼드러처
- 쿼드러처 인코딩 : 그레이 코드의 특성인 한 비트씩 바뀐다는 특성을 이용하여 4가지의 상태로 위치를 판별하는 방법

## 병렬통신
- 여덟 가지 LED 컴포넌트 하나하나마다 별도의 선이 있기 때문에 동시에 모든 컴포넌트를 제어할 수 있다.
- 스트로브 신호
    - 두 개 이상의 장치 사이에서 데이터를 전송하는 시점에 데이터 전송을 알려주기 위한 신호
    
## 직렬통신
- 최소한의 선을 이용해 8개의 신호를 보내는 방법.
- 전송할 데이터는 직렬 프로트콜(여러 규칙으로 이뤄진 통신 규약)을 통해 신호선 하나로 전달되고, 돌아오는 선이 하나 더 필요하다.
- 신호선에 아무 일도 일어나지 않을 때1, 즉 하이 상태로 유지되고, 이를 마크라고 부르며, 로우 상태를 스페이스라고 부른다.
- 시간 분할 멀티플렉싱
    - 시간을 나눈 슬롯을 만들고 슬롯마다 각기 다른 비트를 할당해서 데이터를 한 선에 멀티플렉싱한다.
- 반이중 연결
    - 반이중 통신에서는 송신자와 수신자가 같은 선을 공유한다. 그래서 무선 통신기를 이용할 때 메시지를 송신하고 나면 '오버'라는 단어를 붙인다.
    - 충돌 : 동시에 둘 이상의 송신자가 메시지를 보내려고 시도해서 데이터가 혼신되는 경우

## 파동
- 사인파
    - 다른 모든 파형은 사인파를 조합해 만들 수 있다.
    - 진폭 : 사이파의 높이(0부터 파장의 가장 높은 지점까지의 폭)
    - 주파수(헤르츠) : 매초 같은 방향으로 0을 지나가는 횟수
    - 파장 : 같은 방향으로 0을 지나는 연속된 두 지점 사이의 거리

## 범용 직렬 버스(USB)
- 초기에는 덩치 큰 커넥터들은 선이 4줄뿐인 단일 커넥터였지만, 현재의 USB타입C는 선을 24개까지 사용한다.
- 모든 종단점을 담당하는 컨트롤러가 존재한다.
- 데이터는 패킷으로 나뉘고, 페킷에는 헤더와 페이로드가 들어있다.
- 음향과 비디오를 등시성 전송을 통해 처리할 수 있다.
- 종단점은 자신이 원하는 대역폭을 예약해달라고 요청할 수 있지만, 충분한 대역폭이 없는경우 컨트롤러는 이를 거부할 수 있다.

## 네트워킹
- 근거리 네트워크 : 집이나 사무실같은 좁은 지리적 영역
- 광역 네트워크 : 더 넓은 지리적 영역
- UUCP : 컴퓨터가 다른 컴퓨터에게 데이터를 전송하거나 원격에서 프로그램을 실행할 수 있다.
- 인터넷은 여러 LAN을 하나로 연결해주는 WAN이다.

## 인터넷
- TCP/IP : 전송 제어 프로트콜/인터넷 프로트콜
    - IP는 패킷을 한 곳에서 다른곳으로 옮겨주며, 이 패킷을 데이터그램이라고 부른다.
    - IP를 사용하면 메시지를 언제 받았는지, 제대로 받았는지 알 수 없지만 TCP는 패킷이 제대로 배달됐는지 확실히 알 수 있다.
- IP주소
    - 인터넷상의 각 컴퓨터에는 IP주소라는 유일한 주소가 할당되어있다.
    - 인터넷은 대부분 IPv4, 32비트 주소를 사용한다.
        - 주소는 옥텟표기를 사용해 표현한다.
        - 40억개의 주소를 쓸 수 있지만 충분하지 않기 때문에 128비트 주소를 사용하는 IPv6쪽으로 바뀌고 있다.
    
## 도메인 이름 시스템(DNS)
- IP의 긴 숫자를 외울 필요 없이 example.com과 같은 도메인 이름을 입력해도 원하는 웹 사이트로 갈 수 있다.

## 월드 와이드 웹
- HTTP(하이퍼텍스트 전송 프로트콜) : 현재 가장 많이 사용하는 프로토콜로 웹 페이지 전송을 책임진다.
      - 웹브라우저가 웹서버와 상호작용하는 방법을 정의한다.
      - 웹 브라우저(web browser): 웹 페이지를 볼 때 사용하는 프로그램
      - 웹 서버(web server) : 사용자가 요청한 페이지를 제공한다.
      - URL(Uniform Resource Locator) : 웹 브라우저 주소창에 입력하는 웹 사이트주소에 따라 웹 페이지를 얻을 수 있다. 
            
## 아날로그 처리방법
- 샘플 : 디지털을 아날로그로 표현하려면 데이터의 샘플을 취해야한다.

## 디지털을 아날로그로 변환
- DA변환기 : 디지털을 아날로그로 변환함
- 해상도 : DA가 만들어내는 단계수를 느슨히 표현할 때 쓰임
    - FIFO : 데이터를 일정한 비율로 읽어서 처리하기위한 방법
    - 낮은 워터마크 : FIFO가 거의 빈 상태일 경우 인터럽트 발생
    - 높은 워터마크 : FIFO가 거의 꽉 찬 상태일 경우 인터럽트 발생
  
## 아날로그를 디지털로 변환
- AD변환기 : 아날로그를 디지털로 변환함 -> 입력파형의 샘플을 취할 필요가 있음
- 샘플앤드홀드 : 디지털화한 파형이 아날로그파형을 담기 위해서는 여러가지 샘플을 얻어야하는데 이 회로를 이용해 아날로그신호의 현재값의 안정적으로 잡아냄

## 디지털 오디오
- 일정 간격 시간으로 신호의 진폭이나 높이를 측정
- 푸리에 변환 : 주파수에 따른 진폭을 그래프로 그릴 수 있다.
  - 로우패스 : 낮은 주파수 통과
  - 하이패스 : 높은 주파수 통과
  - 밴드패스 : 정해진 주파수 사이의 주파수를 제외하고 모두 무시한다.
  - 노치 : 특정 주파수만 제외
- 위상차 : 위상시간축위에서 약간씩 신호가 이동함 -> 스테레오 
  - 코덱 : 코더 디코더의 줄임말. 한 코딩 시스템에서 다른 코딩시스템으로 변환

## 디지털 이미지
- 픽셀로 표현 
  - 가산 혼합 색 시스템 : 빨강,녹색,파란색으로 색을 표현하는것
  - 감산 혼합 색 시스템 : 사이언,마젠타,노란색으로 색을 표현하는것
  - 포인트 샘플링 : 각 정사각형의 중심 점의 색을 기록
  - 슈퍼 샘플링 : 한 정사각형 안에서 여러 지점의 색을 얻어서 평균을 냄

## 비디오
- FPS : 프레임/세컨드 로 1초당 프레임을 표현
- 샘플링은 이미지와 별반 다르지않지만 샘플링 아티펙트가 그 자리에 머물러있지않기때문에 깨짐이 발생(슈퍼샘플링으로 해결)
- 움직임 보상 : 움직이지않는 부분은 두고 변경된 부분만 데이터송신 및 저장
- 데이터복구 : 데이터의 완전한 이미지인 키프레임을 추가하는 방식
- 레이어링 : 레이어간의 각기다른 그림을 중첩시켜 비디오 제작

---

## 휴먼 인터페이스 장치

---

### 터미널
- 시분할시스템 : 컴퓨터가 한 번에 하나이상의 작업을 실행하는 것같은 착각을 불러일으키는 멀티테스킹시스템
    - IBM셀렉트릭터미널 : 사용자가 폰트를 바꿀 수 있는 교환가능한 타입볼을 사용한 것

### 그래픽 터미널
- 음극선관이라는 진공관의 변형으로 만들어졌다.
- 그래픽 터미널 디스플레이의 작동 방법 : 정전 평향, 전자 평향 -> 두 방법 모두 비트를 전압으로 변환한다.
- 오늘날 CRT는 액정 디스플레이로 대체된다.

### 백터 그래픽
- 선 또는 백터로 그림을 그리는 방식이다.
- CRT인광물질의 지속성때문에 그림을 표현할 수 있다.
- 원래 CRT는 색을 지원하지 않았기 때문에 흑백이나 그레이스케일 디스플레이다.
- 해상도는 인치당 표시할 수 있는 좌표위치의 갯수이다.

### 래스터 그래픽
- 기존의 텔레비전이 작동하는 방식이다.
- 레스터 스캔은 팩스,레이저 프린터,스캐너등에도 사용한다.

### 키보드와 마우스
- 데이터의 입력을 담당하고 있다.
- X와 Y좌표를 담당하는 두 개의 쿼드러처 인코더를 사용하면 마우스를 만들 수 있다.
 



