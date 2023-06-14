---
title: "[정보처리기사] 정보처리기사 대비 개념 문제"
excerpt: " 정보처리기사 대비 랜덤 개념 문제"
layout: single
categories: Certificate
tag: [정보처리기사]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
use_math: true
---

# 개념 문제

## Reference
- [koreaexam.com/practical/informationprocessing](https://koreaexam.com/practical/informationprocessing){:target="_blank"}

## 문제

네트워크 상의 트랜잭션에 대한 상태 정보를 포함하는 일종의 토큰으로, 주로 웹서버가 웹브라우저로 전송하여 클라이언트 쪽에 저장하고 나서, 사용자가 해당 사이트를 재방문할 경우 웹브라우저가 웹서버에 재전송하는 형태로 많이 이용된다. 그러나 이는 원하지 않는 보안 상의 취약점을 야기할 수 있으므로 사용자가 이것을 주기적으로 삭제해 주는 것이 바람직하다.

<details>
<summary>정답</summary>
- 쿠키
</details>

---

아래에서 설명하는 아키텍처 용어를 보기에서 찾아 쓰시오.

사물인터넷의 한 가지 응용 시스템인 홈 오토메이션은 허락 없이 출입구 또는 창문이 열리는 상황을 센서가 감지하면 자동으로 알람 경보를 내거나 문자 메시지를 거주자에게 전달한다.

(보기)  
ㄱ. Model-View-Controller, ㄴ. Broker, ㄷ. Layered, ㄹ. Dispatcher, ㅁ. Master-Slave, ㅂ. peer-to-peer ㅅ. pipe and filter ㅇ. repository ㅈ. event-based

<details>
<summary>정답</summary>
- ㅈ. event-based
</details>

---

다음 보기의 디자인 패턴들을 GoF(Gang of Fours) 패턴 분류에 따라 구분하였을 때, 생성 패턴, 구조 패턴, 행위 패턴의 개수를 쓰시오.

(보기)  
○ Abstract Factory ○ Adapter ○ Bridge ○ Builder ○ Composite ○ Decorator ○ Iterator ○ Mediator ○ Observer Prototype ○ Proxy ○ Singleton ○ Strategy ○ Visitor

생성 :  
구조 :  
행위 :  

<details>
<summary>정답</summary>
<p>
- 생성 : 4<br>
- 구조 : 5<br>
- 행위 : 5<br>
</p>

<p>
(해설)<br>
- 생성 : 추빌팩프싱(5) : Abstract Factory(추상 팩토리), Builder(빌더), 팩토리 메소드(Factory Method), Prototype(프로토타입), Singleton(싱글톤)<br>
- 구조 : 어브컴데 퍼플프(7) : 어댑터(Adapter), 브리지(Bridge), 컴포지트(Composite), 데코레이터(Decorator), 퍼싸드(Facade), 플라이웨이트(Flyweight), 프록시(Proxy) <br>
- 행위 : 생성 패턴과 구조 패턴에 해당 안되면 행위 패턴 : 책임 연쇄(Chain of Responsibility), 커맨드(Command), 인터프리터(Interpreter), 반복자(Iterator), 중재자(Mediator), 메멘토(Memento), 옵저버(Observer), 상태(State), 전략(Strategy), 템플릿 메소드(Template Method), 방문자(Visitor)
</p>
</details>

---

아래에서 설명하는 SOLID원칙을 쓰시오.

리팩토링(refactoring)을 통해 기존의 설계를 수정하여 추상 클래스 계층과 구현 클래스 계층을 분리하고 인터페이스 클래스를 통해 구현 클래스를 실체화함으로써, 인터페이스를 클라이언트별로 다양화하였다.

<details>
<summary>정답</summary>
- ISP
</details>

---

[학생] 테이블에서 학번이 100인 레코드의 주소를 '서울'로 갱신하는 SQL문을 작성하시오. (세미콜론은 생략가능함)

<details>
<summary>정답</summary>
- UPDATE 학생 SET 주소 = '서울' WHERE 학번 = 100;
</details>

---

아래에서 설명하는 소프트웨어 공학 모델종류를 쓰시오.

- 매우 짧은 주기로 개발을 진행하는 순차적 소프트웨어 개발 모델로 빠른 속도로 개발한다.
- CASE 도구를 이용하여 개발한다.

<details>
<summary>정답</summary>
- RAD 모델
</details>

---

SOLID원칙중 아래에서 설명하는 객체지향 설계 원칙을 쓰시오.

- 서브타입은 자신의 베이스 클래스로 대체될 수 있어야 한다.
- 파생된 클래스를 만들 때, 베이스 클래스의 기능을 교체하는 것이 아니라 기능을 유지하면서 확장하는 것이어야 한다.

<details>
<summary>정답</summary>
- LSP
</details>

---

ⓐ는 경량 환경 및 하드웨어 구현을 위해 최적화된, Involutional SPN 구조를 갖는 범용 블록 암호 알고리즘입니다. ⓐ가 사용하는 대부분의 연산은 XOR과 같은 단순한 바이트 단위 연산으로 구성되어 있습니다. ⓐ라는 이름은 학계, 연구소, 정부 기관의 첫 글자들을 딴 것으로, ⓐ 개발에 참여한 학·연·관의 공동 노력을 표현하고 있습니다.

ⓐ에 들어갈 알맞은 암호화 알고리즘을 적으시오.

<details>
<summary>정답</summary>
- ARIA
</details>

---

상향식 비용 산정 기법 중 LOC(원시 코드 라인 수) 기법에서 예측치를 구하기 위해 사용하는 항목 3가지를 적으시오.

<details>
<summary>정답</summary>
- 낙관치, 기대치, 비관치
</details>

---

명백한 역할을 가지고 독립적으로 존재할 수 있는 시스템의 부분으로 넓은 의미에서는 재사용되는 모든 단위라고 볼 수 있으며, 인터페이스를 통해서만 접근할 수 있는 것은?

<details>
<summary>정답</summary>
- 컴포넌트(Component)
</details>

---

ㄱ, ㄴ에 들어갈 알맞은 용어를 쓰시오.
(  ㉠  )는 사용자가 입력한 IP 주소를 이용해 물리적 네트워크 주소(MAC Address)를 제공한다. (  ㉡  )는 데이터 전송 과정에서 오류가 발생하면 오류 메시지를 전송한다.

<details>
<summary>정답</summary>
- ㄱ : ARP<br>
- ㄴ : ICMP<br>
</details>

---

ⓐ에 들어갈 용어를 쓰시오. 객제지향 분석 방법론에서 ⓐ 방법은 미시적(Micro) 개발 프로세스와 거시적(Marco) 개발 프로세스를 모두 사용하며 클래스와 객체들을 분석 및 식별하고 클래스의 속성과 연산을 정의

<details>
<summary>정답</summary>
- Booch(부치)
</details>

---

ⓐ에 들어갈 디자인패턴 용어를 쓰시오. ⓐ는 구체적인 클래스에 의존하지 않고, 인터페이스를 통해 서로 연관·의존하는 객체들의 그룹으로 생성하여 추상적으로 표현함

<details>
<summary>정답</summary>
- 추상 팩토리(Abstract Factory)
</details>

---

UNIX 시스템의 구성요소 3가지를 적으시오.

<details>
<summary>정답</summary>
- 커널(Kernel)<br>
- 쉘(Shell)<br>
- 유틸리티 프로그램(또는 유틸리티, 파일 시스템 이라고도 부름)
</details>

---

인터넷 기술을 이용하여 조직 내의 각종 업무를 수행 할 수 있도록 만든 네트워크 환경은 무엇인가?

<details>
<summary>정답</summary>
- 인트라넷
</details>

---

다음 상황에 적합한 소프트웨어 아케틱처 패턴을 쓰시오.

- 데이터 관리 컴포넌트, 인터랙션 제어 컴포넌트, 화면 관리 컴포넌트를 분리
- 하나의 데이터를 다양한 그래프로 보여 줄 수 있는 데스크탑 응용 프로그램 개발
- 데이터베이스 연동 부분과 사용자 웹 화면 제공 부분으로 나눈 웹 기반 응용 프로그램 개발

<details>
<summary>정답</summary>
- MVC
</details>

---

ⓐ에 들어갈 알맞은 단어를 적으시오.

ⓐ은(는) 소프트웨어를 구성하는 요소들 간의 관계를 표현하는 시스템의 구조 또는 구조체이다.

<details>
<summary>정답</summary>
- 소프트웨어 아키텍처
</details>

---

사물통신, 사물인터넷과 같이 대역폭이 제한된 통신환경에 최적화하여 개발된 푸시기술 기반의 경량 메시지 전송 프로토콜
- 메시지 매개자(Broker)를 통해 송신자가 특정 메시지를 방행하고 수신자가 메시지를 구독하는 방식
- IBM이 주도하여 개발

<details>
<summary>정답</summary>
- MQTT
</details>

---

컴퓨터와 컴퓨터 또는 컴퓨터와 인터넷 사이에서 파일을 주고 받을 수 있도록 하는 파일 전송 프로토콜은 무엇인가?

<details>
<summary>정답</summary>
- FTP
</details>

---

메모리상에서 프로그램의 복귀 조수와 변수 사이에 특정 값을 저장해 두었다가 그 값이 변경되었을 경우 오버플로우 상태로 가정하여 프로그램 실행을 중단하는 기술은 무엇인가?

<details>
<summary>정답</summary>
- 스택 가드(Stack Guard)
</details>

---

다음이 설명하는 접근 제어 모델을 보기에서 찾아 쓰시오.

군사용 보안구조의 요구사항을 충족시키기 위해 개발된 최초의 수학적 모델로 알려져 있다. 불법적 파괴나 변조보다는 정보의 기밀성 유지에 초점을 두고 있다. ‘상위레벨 읽기금지 정책(No-Read-Up Policy)’을 통해 인가받은 비밀 등급이 낮은 주체는 높은 보안 등급의 정보를 열람할 수 없다. 또한, 인가받은 비밀 등급 이하의 정보 수정을 금지하는 ‘하위레벨 쓰기금지 정책(No-Write-Down Policy)’을 통해 비밀 정보의 유출을 차단한다.

보기(MAC, DAC, RBAC, Biba, Bell-LaPadula)

<details>
<summary>정답</summary>
- Bell-LaPadula
</details>

---

메모리 영역에 비정상적인 데이터나 비트를 채워 시스템의 정상적인 동작을 방해하는 공격 방식은?

<details>
<summary>정답</summary>
- Buffer overflow
</details>

---

ⓐ은(는) 인터넷 연결과 온라인 개인 정보를 보호하는 서비스인 '가상 사설망'을 의미합니다. 가상 사설망은 데이터를 위해 암호화된 터널을 생성하고 IP 주소를 숨김으로써 온라인 신원을 보호하며 공용 Wi-Fi 핫스팟을 안전하게 사용할 수 있게 해준다.

ⓐ에 들어갈 알맞은 단어를 쓰시오.

<details>
<summary>정답</summary>
- VPN
</details>

---

(RISC) 형식의 중앙처리장치(CPU)가 명령어를 처리하는 개별 단계이다. 처리 순서를 보기를 참조하여 바르게 나열하시오.

ㄱ. 명령어의 종류를 해독하는 단계  
ㄴ. 명령어에서 사용되는 피연산자(operand)를 가져오는 단계  
ㄷ. 명령어를 프로그램 메모리에서 중앙처리장치로 가져오는 단계  
ㄹ. 명령어를 실행하는 단계  
ㅁ. 명령어의 결과를 저장하는 단계  

<details>
<summary>정답</summary>
- ㄷ-ㄱ-ㄴ-ㄹ-ㅁ
</details>

---

ⓐ 에 들어갈 소프트웨어 비용 산정 기법 종류는?

ⓐ모형은 소프트웨어 비용 산정 기법 중 알브레히트가 제안한 것으로 소프트웨어의 기능을 증대시키는 요인별로 가중치를 합산하여 총ⓐ를 구한 후 이를 이용해서 비용을 산정한다.

<details>
<summary>정답</summary>
- 기능 점수(FP)
</details>

---

공개키 암호시스템의 하나로, 암호화뿐만 아니라 전자서명이 가능한 최초의 알고리즘으로 알려져 있다. 전자서명 기능은 인증을 요구하는 전자 상거래 등 광범위한 활용을 가능하게 되었으며 큰 숫자를 소인수분해 하기 어렵다는 것에 기반하여 만들어진 이 암호화 알고리즘은?

<details>
<summary>정답</summary>
- RSA
</details>

---

컴퓨터 시스템의 비정상적인 사용, 오용, 남용 등을 실시간으로 탐지하는 시스템으로 오용 탐지, 이상탐지가 있고 실행 4단계로는

1.데이터 수집(Raw Data Collection)  
2.데이터 가공 및 축약(Data Reduction and Filtering)  
3.침입 분석 및 탐지(Intrusion Analysis and Detection)  
4.보고 및 대응(Reporting and Response)이 있다.  

이 시스템은 무엇인가?

<details>
<summary>정답</summary>
- 침입 탐지 시스템(IDS), Intrusion Detection System(IDS)
</details>

---

개발자가 사용해야 하는 서브시스템의 가장 앞쪽에 위치하면서 서브시스템에 있는 객체들을 사용할 수 있도록 인터페이스 역할을 하는 디자인 패턴은?

<details>
<summary>정답</summary>
- 퍼싸드(Facade) 패턴
</details>

---

EAI구축 유형 중 Hub & Spoke와 Message Bus의 혼합 방식이며 데이터 병목 현상을 최소화할 수 있는 유형은?

<details>
<summary>정답</summary>
- Hybrid
</details>

---

(  )안에 공통적으로 들어갈 단어를 보기에서 찾아 쓰시오.

연산이나 부프로그램이 특정 하나의 자료형에 대해 정의된 것이 아니고, 여러 자료형을 처리할 수 있도록 만들어진 경우의 특성을 (   )(이)라고 한다. 이때 특수 범주형 (   )과(와) 매개변수화 (   )(으)로 나눌 수 있다.

(보기)  
ㄱ. 다형성  
ㄴ. 캡슐화  
ㄷ. 추상화  
ㄹ. 정보은닉  
ㅁ. 상속성  
ㅂ. 원자성  
ㅅ. 독립성  

<details>
<summary>정답</summary>
- 다형성
</details>

---

ⓐ에 들어갈 알맞은 관계대수 연산자를 쓰시오.

ⓐ은(는) 은 X ⊃ Y 두 개의 릴레이션 R(X)와 S(Y)가 있을 때, R의 속성이 S의 속성값을 모두 가진 튜플에서 S가 가진 속성을 제외한 속성만을 구하는 연산이다.

<details>
<summary>정답</summary>
- Division 또는 ÷
</details>

---

ㅁ을 가리키는 용어를 쓰시오.

ㅁ는 사용자의 요구에 따라 변하는 동적인 콘텐츠를 처리하기 위해 사용되는 미들웨어이다. 데이터 접근, 세션 관리, 트랜잭션 관리 등을 위한 라이브러리를 제공하는 것으로 주로 데이터베이스 서버와 연동해서 사용한다.

<details>
<summary>정답</summary>
- 웹 애플리케이션 서버(WAS)
</details>

---

인간과 컴퓨터가 쉽고 편하게 상호작용할 수 있도록 작동시스템을 디자인하고 평가하는 과정을 다루는 학문으로서 이 과정을 둘러싼 중요 현상들에 관한 연구도 포함되며 최종 목표는 시스템을 이용하는데 있어 최적의 사용자 경험(UX)을 만드는 학문을 무엇이라고 하는가?

<details>
<summary>정답</summary>
- HCI (하이퍼 컨버지드 인프라스트럭처, Hyperconverged Infrastructure)
</details>

---

ⓐ에 들어갈 알맞은 단어를 쓰시오.

ⓐ은(는) 소프트웨어 개발에 공통적으로 사용되는 구성 요소와 아키텍처를 일반화하여 손쉽게 구현할 수 있도록 여러가지 기능들을 제공해주는 반제품형태의 소프트웨어 시스템이다.

<details>
<summary>정답</summary>
- 소프트웨어 개발 프레임워크 또는 프레임워크
</details>

---

데이터 전송 전에 연결을 설정하지 않는 비연결형 서비스를 제공하며 고속의 안정성 있는 전송 매체를 사용하여 빠른 속도로 여러 사용자에게 데이터를 전송, 실시간 전송에 유리하며 신뢰성보다는 속도가 중요시되는 네트워크에 사용되는 프로토콜은?

<details>
<summary>정답</summary>
- UDP
</details>

---

다음 공격의 대응 방법에 대한 설명으로 ⓐ, ⓑ 에 들어갈 용어를 쓰시오.

- 다른 네트워크로부터 들어오는 IP broadcast 패킷을 허용하지 않으면 자신의 네트워크가 ( ⓐ ) 공격의 중간 매개지로 쓰이는 것을 막을 수 있다.
- 다른 네트워크로부터 들어오는 패킷 중에 출발지 주소가 내부 IP 주소인 패킷을 차단하면 ( ⓑ ) 공격을 막을 수 있다.

<details>
<summary>정답</summary>
- ⓐ : 스머프<br>
- ⓑ : 랜드
</details>

---

정보보안에서 사람의 심리적인 취약점을 악용하여 비밀 정보를 취득하거나 컴퓨터 접근권한 등을 얻으려고 하는 공격방법을 보기에서 찾아 쓰시오.

(보기)  
스푸핑 공격, 사회공학적 공격, 세션 가로채기 공격, 사전 공격, 무차별 대입 공격

<details>
<summary>정답</summary>
- 사회공학적 공격
</details>

---

UML의 관계에 관해 괄호(ⓐ~ⓒ)에 들어갈 용어를 보기에서 찾아 쓰시오.

(ⓐ) : 2개 이상의 사물이 서로 관련되어 있는 관계 이다.  
- 사물 사이를 실선으로 연결 하여 표현한다.
- 다중도를 선위에 표기한다.

(ⓑ) : 하나의 사물이 다른 사물이 포함되어 있는 관계이다.  
- 전체와 부분되어지며 서로 독립적이다.

(ⓒ) : 포함하는 사물의 변화가 포함되는 사물에게 영향을 미치는 관계이다.  
- ex) 문을 열 수 있는 키는 하나이며, 해당 키로 다른 문은 열 수 없다.

(보기)  
ㄱ. Dependency  
ㄴ. Realization  
ㄷ. Composition  
ㄹ. Associtation  
ㅁ. Aggregation  
ㅂ. Generalization  

<details>
<summary>정답</summary>
- ⓐ : Association (연관 관계)<br>
- ⓑ : Aggregation (집합 관계)<br>
- ⓒ : Composition (포함 관계)<br>
</details>

---

ⓐ에 들어갈 구조패턴의 용어를 쓰시오.

ⓐ는(은) 호환성이 없는 클래스들의 인터페이스를 다른 클래스가 이용할 수 있도록 변환해주는 패턴 (기존의 클래스를 이용하고 싶지만 인터페이스 일치하지 않을 때 이용)

<details>
<summary>정답</summary>
- 어댑터(Adapter)
</details>

---

ⓐ~ⓒ에 들어갈 디자인패턴의 종류를 쓰시오.

ⓐ 패턴은 클래스나 객체들이 서로 상호작용하는 방법이나 책임 분배 방법을 정의하는 패턴이다.  
ⓑ 패턴은 ⓑ가 복잡한 시스템을 개발하기 쉽도록 클래스나 객체들을 조합하여 더 큰 구조로 만드는 패턴이다.  
ⓒ 패턴은 클래스나 객체의 생성과 참조 과정을 정의하는 패턴이다.  

<details>
<summary>정답</summary>
- ⓐ : 행위 (Behavioral)<br>
- ⓑ : 구조 (Structural)<br>
- ⓒ : 생성 (Creational)
</details>

---

기억공간이 15K, 23K, 22K, 21K 순으로 빈 공간이 있을 때 기억장치 배치 전력으로 “First Fit”을 사용하여 17K의 프로그램을 적재할 경우 내부단편화의 크기는 얼마인가?

<details>
<summary>정답</summary>
- 6K
</details>

---

소프트웨어 공학의 3R에서 ⓐ는 시스템의 기술적인 원리를 그 구조분석을 통해 발견하는 과정이고, ⓑ는 기존 시스템을 프로그래밍 표준에 맞추거나 고수준의 언어로 재구성하거나 타 하드웨어에서 사용할 수 있도록 변환하는 작업이고, ⓒ는 이미 개발되어 인정받은 소프트웨어의 전체 혹은 일부분을 다른 소프트웨어 개발이나 유지에 사용하는 것이다.

<details>
<summary>정답</summary>
- ⓐ : 역공학<br>
- ⓑ : 재공학<br>
- ⓒ : 재사용
</details>

---

위조된 매체 접근 제어(MAC) 주소를 지속적으로 네트워크로 흘려보내, 스위치 MAC 주소 테이블의 저장 기능을 혼란시켜 더미 허브(Dummy Hub)처럼 작동하게 하는 공격은?

<details>
<summary>정답</summary>
- Switch Jamming
</details>

---

요구사항 명세서 작성자를 제외한 다른 검토 전문가들이 요구사항 명세서를 확인하면서 결함을 발견하는 요구사항 검증방법의 종류를 적으시오.

<details>
<summary>정답</summary>
- 인스펙션(Inspection)
</details>

---

정보보안 3요소에서 기밀성과 무결성의 차이를 서술하시오.

<details>
<summary>정답</summary>
- 기밀성은 인가된 사용자에게 접근이 가능하고 무결성은 인가된 사용자에 대해서만 수정이 가능하다.<br>
(2022년 2회차 81번 필기 기출)
</details>

---

PMBOK 5단계 프로세스를 1단계~5단계를 보기를 참조하여 순서대로 나열하시오.

(보기)  
ㄱ. 실행, ㄴ. 통제, ㄷ. 계획, ㄹ. 착수, ㅁ. 종료

<details>
<summary>정답</summary>
- 착수-계획-실행-통제-종료
</details>

---

ⓐ에 들어갈 서버 개발 프레임워크의 종류를 쓰시오.

ⓐ는(은) JAVA를 기반으로 만든 프레임워크 이며 전자정부 표준 프레임워크의 기반 기술로 사용되고 있다.

<details>
<summary>정답</summary>
- Spring
</details>

---

다음에 제시된 사용자 인증방법과 의 사용자 인증도구를 바르게 연결하시오.

(보기1)  
ㄱ. 지식 기반 인증, ㄴ. 소지 기반 인증, ㄷ. 생체 기반 인증

(보기2)  
A. OTP 토큰, B. 패스워드, C. 홍채

ㄱ:  
ㄴ:  
ㄷ:  

<details>
<summary>정답</summary>
- ㄱ : B<br>
- ㄴ : A<br>
- ㄷ : C
</details>

---

웹서버의 기능 중 네트워크 트래픽의 포화를 방지하기 위해 응답 속도를 제한하는 기능이 무엇인지 쓰시오.

<details>
<summary>정답</summary>
- 대역폭 제한
</details>

---

ⓐ~ⓒ에 들어갈 알맞은 단어를 적으시오 스토리지에서 ⓐ는 서버와 저장장치를 네트워크 디바이스없이 전용케이블에서 연결하는 방식이 스토리지에서 ⓑ는 서버와 저장장치를 네트워크를 통해 연결하는 방식 스토리지에서 ⓒ는 서버와 저장장치를 ⓐ, ⓑ의 파일 공유 장점을 혼합한방식으로, 연결하는 전용 네트워크를 별도로 구성하는 방식이다.

<details>
<summary>정답</summary>
- ⓐ : DAS(Direct Attachted Storage, 다스, 직접 연결 저장장치)<br>
- ⓑ : NAS(Network Attached Storage, 나스, 네트워크 결합 스토리지)<br>
- ⓒ : SAN(Storage Area Network, 산스, 저장 지역 통신망)
</details>

---

컴퓨터 운영체제의 메모리 관리 방법 가운데 하나로 프로세스와 주기억장치를 고정된 크기의 블록 단위로 나누고, 프로세스 실행 시 필요한 블록만을 보조기억장치에서 주기억장치로 가져오므로 프로세스의 물리적인 저장 공간을 비연속적으로 할당하는 것이 가능하다.

<details>
<summary>정답</summary>
- 페이징(Paging)
</details>

---

보기의 소스코드 품질 도구를 정적 분석도구와 동적 분석도구로 구분지으시오.

(보기)  
ㄱ : pmd  
ㄴ : cppcheck  
ㄷ : SonarQube  
ㄹ : Avalanche  
ㅁ : Valgrind  
ㅂ : checkstyle  

<details>
<summary>정답</summary>
- 정적 분석 도구 : ㄱ, ㄴ, ㄷ, ㅂ<br>
- 동적 분석 도구 : ㄹ, ㅁ
</details>

---