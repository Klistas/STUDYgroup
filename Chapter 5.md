# 컴퓨터아키텍쳐

---

## 기본적인 구조요소들
- 폰노이만 구조 : 명령어와 데이터를 동시에 가져올수 없기 떄문에 조금 더 느림. 
- 하버드 구조 : 명령어와 데이터를 동시에 가져올 수 있어서 빠르지만 버스가 더 필요함.
    
## 프로세서 코어
- 멀티 프로세서 시스템은 단일 CPU보다 훨씬더 좋은 성능을 얻어 내는 방법.
- 멀티 코어 프로세서 : 코어가 여러개 들어있는 프로세서고, 요즘엔 일반적으로 쓰임.
    
## 마이크로프로세서와 마이크로컴퓨터
- 마이크로 프로세서 : 메모리와 I/O가 프로세서코어와 같이 있지 않음.
- 마이크로 컴퓨터 : 모든 요소를 한 칩 안에 패키징.
- 단일 칩 시스템 : 조금더 복잡한 마이크로 컴퓨터 IO대신 조금 더 복잡한 장치가 들어 있다.

---

## 함수
- 코드를 재사용하기 위해 필요.
- 코드를 작성해두고 필요 할 때마다 호출하여 사용.
- 명령어 집합으로 함수를 호출 할 수 있음.

---

## 스택
- 재귀 : 함수가 자기 자신을 호출하는 경우
- 깊이 우선 순회 : 트리 아래로 내려갈수 있으면 항상 아래로 내려가고, 더 이상 내려갈 화살표가 없는 경우에만 옆에 있는 화살표로 넘어가는 방식.
- 너비 우선 순회 : 옆에 있는 화살표를 먼저 방문하고 그 후 아래쪽으로 가는 화살표를 방문하는 방식.
- 스택 : 데이터가 쌓여있고 나중에 들어온것이 먼저 나가는 LIFO방식이다.
- 푸시 : 스택에 데이터를 넣는 것.
- 팝 : 메모리를 제거하는 법.
- 스택 오버플로 : 공간이 없는 스택에 푸시하는 것.
- 스택 언더플로 : 빈 스택에서 메모리를 가져오는 경우.
- 스택 프레임 : 함수가 호출될때 마다 스택에 저장되는 데이터 모음.

## 인터럽트
- 멀티 태스킹을 위해 일을 중단하고 또는 진행하여 우선순위를 재배치하는 것.
- 인터럽트를 위해 고려해야할 요소.
     1. 응답시간
     2. 현재 상태  

---

## 상대 주소 지정
- 시분할 : 사용자 프로그램의 실행시간을 조절하는 스캐줄링 기법.
- 인덱스 레지스터 : 저장되어 있는 값을 명령어에 들어있는 주소와 더해서 유효 주소를 계산한다.
- 상대 주소 지정 : 명령어의 주소를 기존으로 하는 주소와의 거리로 상대적인 주소 해석.

## 메모리 관리 장치
- 백그라운드에서 멀티테스킹 하기위해 메모리를 관리 해줌.
- 가상주소 : 프로그램을 작성하기위해 사용.
- 물리주소 : 가상주소를 메모리관리장치를 거쳐 메모리에 저장하기위해 물리주소로 변환.
    - 페이지 폴트 : 프로그램이 물리적 메모리에 연관되지 않은 주소에 접근하면 예외가 발생함 예외가 발생하면,
       운영체제는 실행중인 프로그램을 중단시키지 않고, 메모리관리장치가 추가 메모리를 관리하기위해서 프로그램을 계속 실행함.

## 가상 메모리
- 메모리가 여유가 없이 지나치게 많은 요구에 의해 오염될 경우,
   발생되는 오류(해당 메모리의 주소 호출 불가, 잘못된 메모리 참조 등)를 방지하기 위한 기술.
    - 요구불 페이징 : 현재 필요하지 않은 메모리 페이지를 디스크로 옮겨(스왑 아웃) 필요할때 불러들이는(스왑 인) 방법.
        - 장점 : 메모리가 부족해도 프로그램을 실행시킬수 있다.
        - 단점 : 시스템 성능이 크게 저하한다.
- 최소 최근 사용 알고리즘 : 최근에 가장 자주 사용된 페이지는 물리 메모리에 남겨두고 최근에 가장 덜 사용한 페이지를 스왑 아웃하는 방식.

---

## 시스템 공간과 사용자 공간
- 사용자 프로그램과 시스템 프로그램이 서로 간섭을 하면 예상대로 작동하지 못하기 때문에 하드웨어를 통해 분리한다.
- 장점
     1. 사용자 프로그램으로 부터 운영체제를 보호하고, 사용자 프로그램을 다른 사용자 프로그램으로부터 보호한다.
     2. 사용자 프로그램이 MMU 등의 몇몇 요소에 손을 댈수 없기 때문에 운영체제가 프로그램에 대한 자원 할당을 전적으로 제어할 수 있다.

## 메모리 계층과 성능
- 메모리 계층 구조 : 메모리를 필요에 따라 나누어 CPU가 메모리에 더 빨리 접근하게 만들어 준다.
- 캐시 : 속도가 빠른 장치와 느린 장치에서 속도 차이에 따른 병목 현상을 줄이기 위한 메모리.
     - 캐시 실패 : 캐시에서 읽어야하는 데이터가 없을 때 메모리에서 읽는 경우.
     - 캐시 적중 : CPU가 캐시에서 원하는 내용을 찾은 경우.

## 메모리 상의 데이터 배치
- 정적 데이터 : 프로그램을 작성할때 얼마나 많은 메모리가 필요한지 알고있는 데이터.
- 동적 데이터 : 프로그램을 실행하기 전에는 크기를 알수 없는 데이터.
- 힙 : 동적데이터가 정적데이터가 차지하는 영역 바로 위에 쌓이는 영역.
- 스택은 아래로 쌓이고 힙은 위로 쌓이고 때문에 서로 충돌하지 않게 하는 것이 중요하다.

---

## 프로그램 실행 
- 라이브러리 : 관련된 함수를 한데 모은 영역.
- 링크 : 각 프로그램을 링크하기 편한 형식에 링커라는 프로그램을 사용해 여러 조각을 하나로 연결해 실행하는 방법.
- 진입점 : 프로그램의 첫번째 명령어가 위치하는 주소.
- 런타임 라이브러리 : 프로그램을 이루는 모든부분이 하나로 합쳐져서 실행파일을 이루는 것.
