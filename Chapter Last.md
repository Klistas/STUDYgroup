# 인공지능, 빅데이터
---
### 인공지능
---
- LISP (리스트 처리기) 프로그래밍 언어는 고수준 프로그래밍 언어에 새로운 개념을 도입함.
  - 단일 연결 리스트를 데이터 타입으로 도입.
  - 프로그램을 명령어의 리스트로 간주 -> 프로그램이 자기 자신을 바꿀 수 있어, 머신러닝 시스템을 만들 때 효과적임.
  - 리습 프로그램은 코드를 만들 수 있기 때문에, 새로운 알고리즘을 만들거나, 기존 알고리즘을 수정하는 것이 가능함.
- 초기의 AI 시스템을 하드웨어는 따라가지 못했음.
- 리습을 위해 최적화된 리습 기계가 만들어짐.
- 80년대 전문가 시스템의 등장으로 발전이 가속화됨.
  - 전문가 시스템 : 의료 전문가 같은 사람들에게 질문을 하며 데이터베이스 내부를 검색하도록 도움.
---
### 빅데이터
---
- 데이터가 모이는 속도는 항상 데이터를 분석하는 능력보다 많다.
- 빅데이터란, 크고 복잡한 데이터에서 유용한 데이터를 분석하여 수집하고, 저장,관리하는 것을 말한다.
- 익명화된 데이터를 수집하고 분석하여, 악용하는 일도 발생할 수 있어 주의를 요함.
---
# 실무 상식과 조언
---
## 소프트웨어 개발의 발자취
---
### 간추린 역사
- 멀틱스(Multics) 운영체제 : 1960년대 벨전화 연구소와 제너럭 일렉트릭, MIT가 협력해 개발한 운영체제
- 유닉스(UNIX) 운영체제 : 멀틱스 프로젝트를 수행할 때 가졌던 파일 시스템에 대한 아이디어를 바탕으로 더 작은 컴퓨터에서 만들어진 새 운영체제
    - 소프트웨어에 있어 최소주의와 모듈화라는 철학을 구현했다.
    - 최초의 Portable(여러 종류의 컴퓨터에서 실행할 수 있는)운영체제가 됐다.
- ITS(Incompatible Timesharing System) : MIT에서 개발한 운영체제
    - 이맥스 텍스트 편집기 : 소프트웨어 개발자들에게 가장 크게 기여한 것.
- BSD(버클리 소프트웨어 배포판) : 버클리학생들의 자체적인 유닉스 버전
    - BBN(인터넷의 토대)의 네트워크 스택이 통합되었다.
    - 소켓 인터페이스가 이 과정에서 만들어졌다.
- Sun Microsystems(썬 마이크로시스템즈) : 대학을 졸업한 사람들이 BSD 버전인 유닉스 버전을 기반으로 창업한 회사로, 상업적인 시스템을 만들어 판매했다.
- MS(MicroSoft) : 빌 게이츠가 만든 운영체제
    - 경쟁하는 혁신을 억압하는 데 초점을 맞추는 경우가 종종 있었다.
- PC : 1980년대 중반부터 유명해졌다.
    - 초기 PC에 메모리 관리 장치가 없었기 때문에, 유닉스를 돌리기 적합하지 않았다.
    - 대학에서는 PC에서 저렴한 마이크로소프트가 실행되기 때문에 교육에 활용했다.
    - 소스코드를 볼 수 없었기 때문에 그 당시, 교육의 질이 떨어졌다.
- FOSS(자유로운 오픈소스 소프트웨어) : 자유롭게 사용가능하고 법적으로 방해받을 걱정이 없는 유닉스 버전을 만드는 것.
- 카피레프트(Copyleft)라이선스 : 다른 사람들이 자신의 소프트웨어를 보호하기 위해 사용하는 저작권의 변종.
    - 근본적으로 카피레프트는 다른 사람이 소프트웨어를 무료로, 자유롭게 사용하고 변경하게 허용하는 것이다.
        - 단, 카피레프트 소프트웨어를 변경한 사람은 변경한 소프트웨어를 똑같은 카피레프트 라이선스하에 다른 사람들에게 제공해야 한다.
- Linux(리눅스) : 1991년 리누스 토발즈가 개발했다.
    - 개발이유 : GNU가 제공하는 운영체제가 없었다.
- Cygnus Support(시그너스 서포트) : 오픈소스 소프트웨어를 상업적으로 지원하기 위한 것
---
### 오픈소스 소프트웨어
- 장점
    - 더 많은 사람이 코드를 살펴보기 때문에 안전성이나 신뢰성이 더 높아진다.
    - 프로그래머가 모든 것을 완전히 새로 만들지 않고도 다른 사람들이 작업해둔 것을 바탕으로 작업할 수 있다.
- 단점
    - 코드를 제대로 작성하지 못하는 학생들의 프로젝트에 있는 코드가 대다수였다.
    - 상당수가 마무리가 잘 되지 않았다.
---
### 크리에이티브 커먼즈
- 시각적, 예술적인 라이선스로, 카피레프트와 비슷한 라이선스.
---
### 이식성의 발전
- 이식성있는 코드는 처금 개발된환경 뿐만 아니라 여러 다양한 환경에서 실행될 수 있다.
- 1980년대에 생긴 새로운 컴퓨터 벤더들은 유닉스를 자신의 제품에 포팅했다.
- 하지만 이제는 사용자가 직접 도구를 다른 시스템에 포팅해야 한다.
    - 해결방법
        - POSIX등의 표준이 만들어져서 사용자환경과 API에 약간의 일관성이 생겼다.
        - GNU 프로젝트는 automake, autoconf, libtool 등이 들어 있는 빌드도구 집합을 개발했다.
---
### 패키지관리
- 패키지 관리 도구 : 프로그램을 의존관계 목록이 포함된 패키지로 묶게 해준다.
    - apt, yum, dnf 등의 관리 도구는 소프트웨어를 다운로드해 설치해준다.
        - 대상 시스템이 설치한 프로그램의 의존관계를 만족하는지 검사해서 필요한 의존관계를 다운로드하고 설치해준다.
    - 여러 프로그램이 동일한 의존관계에 대해 각기 다른 버전을 요구할 때는 문제가 발생하는 경향이 있다.
    - 패키지 관리 프로그램은 서로 호환되지 않기 때문에, 프로그램이 각기 다른 시스템에서 설치될 수 있게 준비하려면 작업량이 크게 늘어난다.
---
### 컨테이너
- 컨테이너 : 패키지 관리 문제를 해결하는 방법
    - 아이디어 : 애플리케이션과 모든 의존관계를 컨테이너 한꺼번에 담는 것.
    - 컨테이너는 데이터 파일등의 모든 내용물이 들어 있는 환경에서 실행해준다
        - 단, 시스템의 나머지와 격리된 상태에서 실행해준다.
    - 장점
        - 애플리케이션을 실행하기 위해 필요한 모든 의존관계를 하나의 패키지로 묶을 수 있어서 소프트웨어 디플로이를 단순화해준다.
        - 보안이 좋다는 경우가 있지만 다른 버그로 공격할 수도 있다.
    - 단점
            - 실질적으로 컨테이너가 공유 라이브러리 사용을 없애버린다.
            - 이로 인해 메모리가 낮아질 수 있다.
            - 애플리케이션 자체보다 더 크다
- 스냅(snap) : 컨테이너화된 애플리케이션
- 컨테이너 리눅스 : 리눅스를 컨테이너에 실행하기 위해 가볍게 만들려고 한 것.
---
### 자바
- 썬 마이크로시스템즈에서 개발되었다.
- 장점
    - 모든 대상 기계에 대해 코드를 재컴파일하는 대신, 대상 기계에서 실행될 자바 인터프리터만 누군가 재컴파일 해두면 자바 코드를 재컴파일할 필요가 없다.
    - 교육에 자바가 쓰인 이유 : 자바가 Garbage collection을 통해 메모리를 관리한다.
    - 초보자에게 복잡한 메모리 관리를 가르치지 않아도 된다.
- 단점
    - 코드가 복잡하고 파편화되어있어 프로그램이 실행되기 어려울 떄가 있다.
    - 어떤 목표달성보다 클래스 계층 유지에 더 우선순위를 두는 경향이 있다.
- 하이버네이트(Hibernate)
    - 장점
        - 자바 클래스와 하위 클래스로 데이터 은닉을 하려는 목표를 달성하려고 한다.
        - HQL이라는 추상화를 일반적으로 SQL 기반 데이터베이스 API위에 제공하는 것이다.
---
### Node.js
- 자바스크립트가 브라우저 밖에서 실행되게 해주는 아주 최근에 나온 환경이다.
- 클라이언트와 서버 쪽 애플리케이션을 하나의 프로그래밍 언어로 작성할 수 있다.
- 단점
    - 노드가 자신만의 패키지 관리자를 만드는데, 이 관리자는 모든 사람에게 필요하지만, 호환되지 않는 방법으로 만들었기 때문에 유지보수하기가 더 어려워졌다.
    - 의존성이 꼬인 노드패키지가 매우많고, 상당수는 심각한 작업에 적당하지 않다.
---
### 클라우드 컴퓨팅
- 네트워크를 통해 다른 누군가의 컴퓨터를 쓴다는 뜻이다.
---
### 가상 머신
- 하드웨어 환경과 운영체제가 실행되기 위한 명령어 집합을 제공하는 시스템
- 하이퍼바이저 : 가상 머신을 운영하는 시스템
---
### 이동식 장치
- 컴퓨팅 파워와 기능을 제공하는 장치이다.
---
## 프로그래밍 환경
---
### 추정하는 방법 배우기
- 작업을 시작하기전, 그 작업이 얼마나 걸릴지 값을 추정하고 기록하고, 추적한다.
- '상황 일지'를 작성한다.
---
### 프로젝트 스케줄링
- 프로젝트의 모든 요소를 목록으로 만들고, 적당한 단위로 나눈다.
---
### 직장 내 문화 다루기
- 문제가 생기면 문제를 다시 재구성해보는 것이 중요하다.
---
### 가치 제안
---
- 프로그래머에게는 코드를 작성하는 능력만이 전부는 아님.
- 프로젝트에 참가할 때는 과업에 가치를 더하는, 즉 생산성 증대를 위해서 무엇을 할 수 있는지 생각해야함.
- 재사용 가능한 코드작성, 유지보수가 용이한 코드 작성등을 통하여 가치를 더하는 방법을 연구해야함.
- 소프트웨어 패키지를 만들 때, 기존의 것을 새로 만들어서 하는 방법이 꼭 가치를 더하는 일만은 아니다.
- 최소 놀람의 규칙을 가이드라인 삼아라.
  - 최소 놈람의 규칙 : 사용자 인터페이스나 소프트웨어가 가능한 한 사람들의 예상과 다른 결과를 내놓지 말아야한다는 규칙.
---
### 스타일을 지켜라
---
- 프로그램이 존재하는 환경을 이해해야함.
- 오픈소스 프로젝트 등에 기여하여, 타인과의 상생 발전을 도모.
- 깔끔한 코드 작성, 설명 문서의 작성등이 있어야 타인들이 내 코드를 이해하고, 도와줄 수 있음.
- 내가 이해한 대로 남들이 이해하지 않으므로, 좋은 문서의 작성은 더욱 더 중요하다.
---
### 기존 프로젝트를 사용하라
---
- 비슷한 일을 하지만 완전히 같지는 않은 프로그램들을 작성하는 것을 피해야함.
- 완성되지 않은 자신의, 혹은 타인의 프로젝트를 끝내기 위해 노력해야함.
- 자신의 프로젝트를 끝내지 못했다면, 적어도 누군가 이어받기 쉽도록 형태를 만들어야함.
- 이것들은 모두 프로그래밍 생태계에 가치를 추가하는 일이기 때문.


