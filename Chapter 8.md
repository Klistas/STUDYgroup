 8장 프로그래밍 언어 처리
===


## 어셈블리 언어 (Assembly Language)
- 사람은 알아내기 힘든 기계어를 프로그래머들이 사용하기 쉽게하기 위해 나은 방법이다.
- 비트 조합을 외우지 않고 니모닉(mnemonics)을 통해 명령어를 쓸 수 있다.
- 레이블 : 주소에 이름을 붙일 수 있다.
- 주석 : 다른 사람들이 프로그램을 더 쉽게 읽고 이해하도록 도와줄 수 있다.
- 어셈블러 : 어셈블리 언어로 작성된 코드를 읽어서 동등한 기계어 코드를 생성해주는 프로그램

## 고수준 언어
- 어셈블리 언어보다 더 높은 추상화 단계의 언어
- 컴파일러 : 소스코드를 기계어로 번역해주는 프로그램
- 비구조적언어 : 프로그램이 복잡해지면 스파게티 코드 문제가 생겨 관리를 할 수 없는 언어
    - 포트란 언어 : 최초의 고수준 언어 중 식변환을 해주는 언어
  
## 구조적 프로그래밍
- 스파게티 코드 문제를 해결하기 위해 만든 프로그래밍 방법
- C언어 : 아주 실용적인 언어이며 가장 널리 쓰이는 프로그래밍 언어
    - C++, 자바, PHP, 파이썬, 자바스크립트등이 C언어의 요소를 포함하고 있다.
    
    
## 어휘 분석
- 어휘분석 : 코드를 기호로 부터 단어와 같은 성격의 토큰으로 변환하는 과정
    - 어휘항목 (lexeme): 소스 코드에 존재하는 의미있는 문자열, 식별자, 숫자, 키워드 등을 의미한다.

    - 패턴 (pattern): 토큰이 어휘항목을 서술하는 규칙으로써, 정규문법에 따라 표현된다.

    - 토큰 (token): 토큰이름과 속성값으로 구성되는 데이터쌍으로써, 각 토큰은 토큰의 패턴에 부합하는 어휘항목을 갖는다.


### 상태 기계
- 상태 기계 : 한 번에 오로지 한 개의 상태만 가지게 되며, 현재 상태란 임의의 주어진 시간 상태를 칭한다.


### 정규식
- 정규식 : 언어를 지정하기 위한 언어를 정의하는 것

## 단어에서 문장으로
- 시프트-리듀스 파서 : 시프트는 토큰을 스택에 넣는다는 뜻이고, 리듀스는 스택의 맨 위부터 매치된 토큰들을 다른 어떤 것으로 대치한다는 뜻이다.

    
    
## 누구나 프로그래밍 언어를 만들 수 있는 시대
- 도메인 특화 언어(DSL) : 언어를 어떻게 구체적으로 응용할지 이해할 때 사용되는 언어

## 파스 트리
- 인터프리트(interpret) : 고수준 언어를 실행하는 방법
    - 실제 기계에 사용될 기계어를 만들어내지 않는다. -> 대신 '가상 머신' 에서 실행 된다.
    - 일부 인터프리트 언어는 인터프리터에 의해 직접 실행되기도 한다.
    - 어떤 인터프리트 언어들은 나중에 해석될 수 있도록 중간어로 컴파일 되기도 한다.
- 가상머신 : 소프트웨어로 작성된 기계
- 컴파일 된 코드 : 기계어이기 때문에 더 빠르게 실행된다. 
- 파스 트리(parse tree) : 언어 문법으로 부터 만들어낸 DAG(directed acyclic graph) 데이터 구조
    - 일반적으로 컴파일러나 인터프리트에서 파스 트리를 구성한다.
    - 각 노드에는 code(노드 유형을 표시), leaf의 배열이 있다.
    - leaf
        - code 에 따라 leaf들의 해석이 달라진다.
        - 여러 타입의 정보를 담을 수 있어야 하기 때문에 공용체이다.
        - 멤버이름에는 C언어의 문법을 사용한다.
        - 새로운 노드를 만들 때 함수가 있다면,
            1. leaf의 개수를 첫 번째 인자로 받는다.
            2. code를 두 번째 인자로 받는다.
            3. 세 번째 인자로부터 필요한 만큼 leaf를 받는다.

## 인터프리터
- 파스 트리의 실행 순서
    1. 연결 리스트를 순회한다.
    2. 깊이 우선 순회를 통해 재귀적으로 계산을 한다.
- 파스 트리를 실행하는 방법
    1. 리스트 순회와 계산 코드를 yacc에 붙여넣으면 파스 트리를 즉시 실행할 수 있다.
    2. 파스 트리를 파일에 저장했다가 나중에 읽어서 실행하는 방법이 있다.
        - 자바와 파이썬 같은 언어가 이런 식으로 작동한다.
- 프론트엔드(front-end) : 파스 트리를 만든다.
    - 파스 트리는 어떤 중간언어(intermediate language)로 표현된다.
        - 백엔드(back-end) : 이 언어를 실행할 대상 환경마다 하나씩 존재한다.

## 컴파일러
 - 앞의 인터프리터와 같은 방식.
 - 백엔드 부분에서 코드생성기 추가.

 - 코드생성기 (code generator)
    - 기계어 코드 생성. (어셈블리 코드 생성 -> 어셈블러로 이 어셈블리 코드를 기계어로 번역)

- 컴파일러는 인터프리터보다 훨씬 빠른 코드 생성, But, 완전히 효율적인 방법은 아님. -> 최적화가 필요함.

## 최적화
 - 파스 트리와 코드 생성기 사이에 최적화기 추가
    - 최적화기(optimizer) : 파스 트리를 분석하여, 효율적인 코드 생성을 위해 파스 트리를 변환.
        - 계산 횟수를 줄임
        - 강도 절감(strength reduction) : 연산을 비교해, 더 비용이 적게드는 연산으로 변환.

## 하드웨어를 다룰 때 주의하라.
 - 하드웨어를 조작하는 코드를 최적화시, 오류가 발생할 수 있다.
 - 최적화기에 예외를 설정하거나, 직접적으로 최적화기를 꺼야할 수도 있음.