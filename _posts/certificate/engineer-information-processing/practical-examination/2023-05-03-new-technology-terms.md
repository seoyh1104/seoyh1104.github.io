---
title: "[정보처리기사] 신기술 용어"
layout: single
categories: Certificate
tag: [정보처리기사]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
use_math: true
---

# 신기술 용어
## 네트워크 관련 신기술 용어
- **SDN**(Software Defined Network)
  - 네트워크를 제어부(Control Plane), 데이터 전달부(Data Plane)로 분리하여 네트워크 관리자가 보다 효율적으로 **네트워크**를 **제어**, **관리**할 수 있는 기술
  - 기존의 라우터, 스위치 등과 같이 하드웨어에 의존하는 네트워크 체계에서 안정성, 속도, 보안 등을 소프트웨어로 제어, 관리하기 위해 개발
- **NFV**(Network Function Virtualization)
  - 범용 하드웨어(세커／스토리지／스위치)에 가상화 기술을 적용하여 **네트워크 기능**을 **가상** 기능으로 모듈화하여 필요한 곳에 제공(스위치, 라우터 등)하는 기술
- **Wi-SUN**(Wireless Smart Utility Network)
  - 스마트 그리드(Smart Grid)와 연계하여 전기, 수도, 가스 등의 공급자와 사용자가 **무선 네트워크**를 이용하여 효율적으로 관리할 수 있도록 활용하는 IEEE 802.15.4 표준 기반의 무선 통신 기술
  - Wi-SUN은 저가격 및 저전력(8mA), 통신사 제공 서비스가 아닌 자체 자가망 구축 형태의 비면허대역(900MHz)을 사용
- **NFC**(Near Field Communication)
  - 13.56MHz 주파수를 사용하고, 424Kbps의 속도로 데이터를 전송하는 RFID의 확장 기술로, **l0cm 이내**에서 저전력, **비접촉식 무선 통신 기술**
  - 고주파(HF)를 이용하는 ISO기EC 18092 표준으로 아주 가까운 거리에서 양방향 통신을 지원 
- **스몰 셀**(Small Cell)
  - 기존의 높은 전송 파워와 넓은 커버리지를 갖는 매크로 셀(Macro Cell)과 달리 낮은 전송 파워와 좁은 커버리지를 가지는 **소형 기지국**
  - 안테나당 10W급 이하의 소출력 기지국 장비나 피코 셀, 펨토 셀 등을 통칭
  - 기존의 매크로 셀과 다양한 스몰 셀(피코 셀, 펨토 셀 등) 및 Wi-Fi 등으로 구성된 네트워크로 사용자 수와 트래픽 수요에 따라 스몰 셀을 배치하여 셀 용량과 커버리지 증대에 활용
- **블루투스**(Bluetooth)
  - **2.4GHz** ISM 주파수 대역을 이용하여 l0cm 이내의 근거리 디바이스 간 통신을 지원하기 위한 무선 접속 규격(IEEE802.15.1)
  - 블루투스 네트워크 구성에는 피코넷(Piconet), 스캐터넷(Scattemet)이 있음
  - 피코넷은 마스터(Master)-슬레이브(Slave) 방식으로 링크를 설정하고, 한 대의 마스터로 7대까지의 슬레이브를 연결하여 네트워크를 구성할 수 있도록 하는 방식
  - 스캐터넷은 피코넷이 여러 개 모여서 계층적이고 규모가 큰 네트워크를 구성할 수 있는 방식
- **BLE**(Bluetooth Low Energy)
  - **저전력** 기반 기기 간 근거리 무선 통신 기능을 제공하는 기술 및 규격
  - 짧은 전송 거리를 극복하고, 1Mbps의 전송속도로 a4GHz 주파수를 사용하는 저비용으로 구성 가능한 블루투스 기술
- **Zing**
  - 기기를 키오스크에 갖다 대면 원하는 데이터를 바로 가져올 수 있는 기술로 10cm 이내 근접 거리에서 기가급 속도로 데이터 전송이 가능한 **초고속 근접 무선통신**(NFC; Near Reid Communication) 기술
  - 3Gbps급의 기기 간 최대 전송속도(무선 구간) 및 직관적 사용자 인터페이스(Touch & Get 방식) 기반의 대용량 데이터 순간 전송 제공
- **BcN**(Broadband convergence Network)
  -  **통신, 방송, 인터넷**이 융합된 품질 보장형 광대역 멀티미디어 서비스를 언제 어디서나 끊김 없이 안전하게 이용할 수 있는 **광대역 통합망**
- **C-V2X**(Celiular-Vehicie-to-Everything)
  - **이동통신**(3GPP 릴리즈 14) 기술 기반의 **V2X 통신기술**로 차량이 유・무선망을 통해 다른 차량 및 도로 등 인프라가 구축된 사물과 정보를 교환할 수 있는 자율주행자동차를 위한 통신기술
- **메시 네트워크**(Mesh Network)
  - 기존 무선 랜의 한계 극복을 위해 등장하였으며, **대규모 디바이스의 네트워크 생성에 최적화**되어 차세대 이동통신, 홈 네트워킹, 공공 안전 등의 특수목적을 위한 새로운 방식의 네트워크 기술
  - 다른 국(Station)을 향하는 호출이 중계에 의하지 않고 **직접 접속되는 그물 모양의 네트워크**
  - 통신량이 많은 비교적 소수의 국 사이에 구성될 경우 경제적이고 간편하지만, 다수의 국 사이에는 회선이 세분화되어 비경제적
  - 대용량을 빠르고 안전하게 전달할 수 있어 행사장이나 군 등에서 많이 활용됨
- **UWB**(Ultra Wide Band)
  - 매우 낮은 전력을 사용하며, 초광대역 주파수 대역으로 디지털 데이터를 전송하는 무선 전송 기술
  - **무선 디지털 펄스**라고도 하며, 0.5mm 정도의 저전력으로 많은 양의 데이터를 1km의 거리까지 전송 가능
- **UsN**(Ubiquitous Sensor Network)
  - **통신 기능이 있는 스마트 RFID 태그 및 센서**를 부착하여, 사물의 인식정보 및 주변의 환경정보(온도, 습도, 오염정보, 균열정보 등)를 탐지하고, 실시간으로 네트워크에 연결하여 정보를 관리하는 기술
- **WBAN**(Wireless Body Area Network)
  - 체내 혹은 인체 주변 3m 이내에서 일어나는 저비용, 저전력, 고속통신이 가능한 **신체 접촉 근거리 무선 네트워크**
- **NDN**(Named Data Networking)
  - **기존의 ip 주소 대신 Data의 이름을 활용**하여 정보(콘텐츠)의 효율적인 검색 및 배포를 목적으로 하는 미래 인터넷 기술
- **네트워크 슬라이싱**(Network Slicing)
  - 하나의 물리적 코어 네트워크를 독립된 다수 가상 네트워크로 분리한 뒤 고객 맞춤형 서비스를 제공하는 5G 핵심 기술
  - SDN과 NFV 기술을 활용하여 하나의 **물리적인 망에 여러 개의 논리적인 망**을 만들어 비용 철감 가능
- **NOMA**(Non-Orthogonal Multiple Access)
  - 동일한 시간, 주파수, 공간 자원상에 두 대 이상의 단말에 대한 데이터를 동시에 전송하여 주파수 효율을 향상시키는 비직교 **다중 접속 기술**
- **MEC**(Mobile Edge Computing/Cloud)
  - 무선 기지국에 분산 클라우드 컴퓨팅 기술을 적용하여 서비스와 캐싱 콘텐츠를 이용자 단말에 가까이 전개함으로쩌 **모바일 코어 망의 혼잡을 완화**하는 기술
- **사물 인터넷**(loT; Internet of Things)
  - 각종 사물에 센서와 통신 기능을 내장하여 **무선 통신을 통해 각종 사물을 인터넷에 연결**하는 기술
- **MQTT**(Message Queuing Telemetry Transport)
  - **loT 장치, 텔레메트리 장치** 등에서 최적화되어 사용할 수 있도록 개발된 프로토콜로, 브로커를 사용한 발행(Publish)／구독(Subscribe) 방식의 경량 메시징을 전송하는 프로토콜
- **COAP**
  - M2M 노드들 사이에서 이벤트에 대한 송수신을 **비동기적으로 전송하는 REST 기반의 프로토콜**이자 제약이 있는(Constrained) 장치들을 위한 특수한 **인터넷 애플리케이션 프로토콜**
- **Zigbee**
  - 근거리 통신을 지원하는 IEEE 802.15.4 표준 중 하나로, 868/915MHz, 2.4GHz 주파수 대역을 이용하는 **저전력, 저속, 저비용의 근거리 무선통신 기술**
- **스마트 그리드**(Smart Grid)
  - **전기 및 정보통신기술을 활용**하여 전력망을 지능화, 고도화함으로써 고품질의 전력서비스를 제공하고 에너지 이용효율을 극대화하는 전력망

## 소프트웨어 관련 신기술 용어
- **인공지능**(Al; Micial Intelligence)
  - 인간의 지적능력을 인공적으로 구현하여 **컴퓨터가 인간의 지능적인 행동과 사고를 모방**할 수 있도록 하는 소프트웨어
- **기계학습**(Machine Learning)
  - 기계학습은 인공지능의 분야 중 하나로, **인간의 학습 능력**과 같은 기능을 컴퓨터에서 실현하고자 하는 기술
  - 환경과의 상호작용에 기반한 경험적인 데이터로부터 **스스로 성능을 향상**시키는 시스템을 연구하는 기술
- **가상 현실**(VR; Virtual Reality)
  - 컴퓨터 등을 사용한 인공적인 기술로 만들어낸 **실제와 유사하지만 실제가 아닌** 어떤 특정한 환경이나 상황 또는 구현하는 기술
- **증강 현실**(AR; Augmented Reality)
  - 가상 현실(VR)의 한 분야로 실제로 존재하는 환경에 가상의 사물이나정보를 합성하여 마치 **원래의 환경에 존재하는 사물처럼 보이도록** 하는 컴퓨터 그래픽 기술
- **혼합 현실**(MR; Mbed Reality)
  - 실세계의 **물리적 환경과 가상환경을 혼합**한 경험을 제공하는 하이브리드 현실
- **블록체인**(Blockchain)
  - 분산데이터베이스의 한 형태로 **분산 노드**의 운영자에 의한 임의조작이 불가능 하도록 고안되어 지속적으로 성장하는 데이터 기록 리스트인 블록을 연결한 모음
- **BaaS**(Blockchain-as-a-Service)
  - **블록체인 개발환경을 클라우드로 서비스**하는 개념으로 블록체인의 기본 인프라를 추상화하여 블록체인 응용 프로그램을 만들 수 있는 클라우드 컴퓨팅 플랫폼
- **CPS**(Cyber-Physical System)
  - **가상 물리 시스템**으로 인간의 개입 없이 대규모 센서,액추에이터를 갖는 물리적인 요소들과 통신 기술, 응용, 시스템 소프트웨어 기술을 활용하여 실시간으로 물리적 요소들을 제어하는 컴퓨팅 요소가 결합된 복합 시스템
- **디지털 트윈**(Digtal Twin)
  - **물리적인 사물과 컴퓨터에 동일하게 표현되는 가상 모델**로 실제 물리적인 자산 대신 소프트웨어로 가상화함으로쩌 실제 자산의 특성에 대한 정확한 정보를 얻을 수 있고, 자산 최적화, 돌발사고 최소화, 생산성 증가 등 설계부터 제조, 서비스에 이르는 모든 과정의 효율성을 향상시킬 수 있는 모델
- **서비스 지향 아키텍처**(SOA; Service Oriented Architecture)
  - 서비스라고 정의되는 분할된 애플리케이션 조각들을 Loosely-coupled하게 연결해 **하나의 완성된 Application을 구현하기 위한 아키텍처**
  - SOA는 비즈니스 층, 표현 층, 프로세스 층으로 구성
- **디지털 변혁**(Digital Transformation)
  - **디지털 기술 기반**으로 기업의 전략, 조직, 프로세스, 비즈니스 모델, 문화, 커뮤니케이션 등을 변화시키는 **경영전략**
- **마이크로서비스 아키텍처**(MSA; Microservices Architecture)
  - 하나의 큰 시스템을 **여러 개의 작은 서비스**로 나누어 변경과 조합이 가능하도록 만든 아키텍처
- **매시업**(Mashup)
  - **웹**으로 제공하고 있는 정보와 **서비스를 융합**하여 새로운 소프트웨어나 서비스, 데이터베이스 등을 만드는 기술
  - 서로 다른 웹 사이트의 콘텐츠를 조합하여 새로운 차원의 콘텐츠나 서비스를 창출하는 웹 사이트 또는 애플리케이션을 의미
- **그레이웨어**(Grayware)
  - 바이러스나 명백한 악성 코드를 포함하지 않는 합법적 프로그램이면서도 사용자를 귀찮게 하거나 위험한 상황에 빠뜨릴 수 있는 프로그램
  - 즉 평범한 소프트웨어인지, 바이러스인지 구분하기 어려운 중간 영역에 존재하는 프로그램
  - 그레이웨어는 스파이웨어, 애드웨어, 장난 프로그램, 원격 액세스 도구 등 **사용자가 원하지 않는 프로그램을 총칭**하는 이름
- **텐서플로**(TensorFlow)
  - **구글**의 구글 브레인 팀이 제작하여 공개한 **기계 학습**(Machine Learning)을 위한 오픈 소스 소프트웨어 라이브러리
- **파스타**(PaaS-TA)
  - 국내 IT 서비스 경쟁력 강화를 목표로 개발되었으며 인프라 제어 및 관리 환경, 실행 환경, 개발 환경, 서비스 환경, 운영 환경으로 구성된 NIA 주도로 개발된 **개방형 클라우드 컴퓨팅 플랫폼**
- **메타버스**(Metaverse)
  - 가상, 초월과 세계, 우주의 합성어로서, **3차원 가상 세계**를 뜻하는 용어
  - 정치, 경제, 사회, 문화의 전반적 측면에서 현실과 비현실 모두 공존할 수 있는 생활형, 게임형 가상 세계

## 인프라 관련 신기술 용어
- **SDDC**(Software Defined Data Center)
  - 모든 하드웨어가 가상화되어 가상 자원의 풀(Pool)을 구성하고, 데이터센터 전체를 운영하는 **소프트웨어가 필요한 기능 및 규모에 따라 동적으로 자원을 할당, 관리**하는 역할을 수행하는 **데이터센터**
- **SDS**(Software Defined Storage)
  - 서버와 전통적인 스토리지 장치에 장착된 물리적 디스크 드라이브를 가상화 기술을 적용하여 **필요한 공간만큼 나눠서 사용할 수 있도록 논리적인 스토리지로 통합한 가상화 기술**
  - 컴퓨팅 소프트웨어로 규정하는 데이터 스토리지 체계이며, 일정 조직 내 여러 스토리지를 하나의 스토리지처럼 관리하고 운용하는 컴퓨터 이용 환경
- **HACMP**(High Availability Cluster Muitiprocessing)
  - 각 시스템 간에 **공유 디스크를 중심으로 클러스터링으로 엮여 다수의 시스템을 동시에 연결**하여 조직, 기업의 기간 업무 서버 등의 안정성을 높이기 위해 사용되는 **고가용성 솔루션**
  - 여러 가지 방식으로 구현되며 2개의 서버를 연결하는 것으로 2개의 시스템이 각각 업무를 수행하도록 구현하는 방식이 널리 사용됨
- **도커**(Docker)
  - **컨테이너 응용 프로그램의 배포를 자동화**하는 오픈소스 엔진
  - 소프트웨어 컨테이너 안에 응용 프로그램들을 배치시키는 일을 자동화해주는 오픈 소스 프로젝트이자 소프트웨어 하이퍼바이저(Hyperiisor)
  - 하나의 호스트 컴퓨터상에서 동시에 다수의 운영체제를 구동시킬 수 있는 HW와 OS 사이의 SW 가상화 플랫폼
- **쿠버네티스**(Kubemetes)
  - **리눅스** 재단에 의해 관리되는 **컨테이너화된 애플리케이션의 자동 배포, 스케일링 등을 제공하는 오픈 소스 기반의 관리 시스템**
- **서버리스 컴퓨팅**(Serverless Computing)
  - MSA, BaaS, FaaS 등의 기술을 활용하여 **서버가 없는 것과 같이 직접 해당 이벤트에 접근**하여 처리하는 컴퓨팅 기술
  - 각 서버를 접속하는 방식보다 연결 및 속도를 개선

## DB 관련 신기술 용어
- **하둡**(Hadoop)
  - 오픈 소스를 기반으로 한 **분산 컴퓨팅 플랫폼**
  - 일반 PC급 컴퓨터들로 가상화된 대형 스토리지를 형성하고 그 안에 보관된 거
  - 대한 데이터 세트를 병렬로 처리할 수 있도록 개발된 자바 소프트웨어 프레임워크로 구글, 야후 등에 적용
- **HDFS**(Hadoop Distributed Ale System)
  - 대용량 파일을 분산된 서버에 저장하고, 그 저장된 데이터를 빠르게 처리할 수 있게 하는 **하둡 파일 시스템**
- **맵 리듀스**(Map Reduce)
  - 구글에서 대용량 데이터를 **분산 병렬 컴퓨팅**에서 처리하기 위한 목적으로 제작하여 2004년 발표한 소프트웨어
  - Java, C++, 그리고 기타 언어에서 적용이 가능하도록 작성
  - 아파치 하둡(Apache Hadoop)으로 대표되는 소프트웨어 프레임워크
- **스쿱**(Sqoop)
  - **커넥터**(Connector)를 사용하여 관계형 데이터베이스 시스템(RDBMS)에서 HDFS로 데이터를 수집하는 기술
- **NoSOL**(Not Only SQL)
  - 전통적인 RDBMS와 다른 DBMS를 지칭하기 위한 용어로 데이터 저장에 **고정된 테이블 스키마가 필요하지 않고 조인(Join) 연산을 사용할 수 없으며, 수평적으로 확장이 가능**한 DBMS
- **다크 데이터**(Dark Data)
  - 수집된 후 저장은 되어 있지만, **분석에 활용되지는 않는 다량의 데이터**
- **데이터 마이닝**(Data Mining)
  - 빅데이터 분석 기술 중 대량의 데이터를 분석하여 데이터 속에 있는 변수 사이의 상호관계를 규명하여 **일정한 패턴을 찾아내는 기법**
- **데이터 웨어하우스**(DW; Data Warehouse)
  - 사용자의 의사 결정에 도움을 주기 위하여, 기간 시스템의 데이터베이스에 축적된 데이터를 **공통 형식으로 변환해서 관리**하는 데이터베이스
- **데이터 마트**(DM; Data Mart)
  - 데이터 웨어하우스(DW) 환경에서 정의된 접근계층으로, **데이터 웨어하우스에서 데이터를 꺼내 사용자에게 제공**하는 역할
  - 데이터 웨어하우스의 부분이며, 대개 특정한 조직 혹은 팀에서 사용하는 것을 목적으로 함
- **메타 데이터**(Meta Data)
  - 데이터에 대한 **구조적인 데이터**로서, 일련의 데이터를 정의하고 설명해 주는 데이터이고, 구축할 정보 자원을 기술하는 데이터
- **디지털 아카이빙**(Digital Archiving)
  - 지속적으로 보존할 가치를 가진 디지털 객체를 장기간 관리하여 이후의 이용을 **보장**할 수 있도록 변환, 압축 저장하여 DB화하는 작업
- **마이 데이터**(MyData)
  - 정보 주체가 기관으로부터 자기 정보를 직접 내려받아 이용하거나 제3자 제공을 허용하는 방식으로 **정보 주체 중심의 데이터 활용체계**
  - 개인이 정보 관리의 주체가 되어 능동적으로 본인의 정보를 관리하고, 본인의 의지에 따라 신용 및 자산관리 등에 정보를 활용하는 일련의 과정
- **스크래파이**(Scrapy)
  - **웹 사이트를 크롤링하여 구조화된 데이터를 수집**하는 **파이썬(Python) 기반**의 애플리케이션 프레임워크