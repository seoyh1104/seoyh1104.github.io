---
title: "[정보처리기사] 네트워크 구조"
layout: single
categories: Certificate
tag: [정보처리기사]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
use_math: true
---

# 네트워크 구조

## 애드 혹 네트워크(Ad-hoc Network) ★
- `2021년 2회 기출`
- 애드 혹 네트워크는 **노드(Node)들에 의해 자율적으로 구성되는 기반 구조가 없는 네트워크**이다.
- 네트워크의 구성 및 유지를 위해 기지국이나 액세스 포인트와 같은 기반 네트워크 장치를 필요로 하지 않는다.
- 애드 혹(Ad-hoc) 노드들은 무선 인터페이스를 사용하여 서로 통신하고, 멀티 홉 라우팅 기능에 의해 무선 인터페이스가 가지는 통신 거리상의 제약을 극복하며, 노드들의 이동이 자유롭기 때문에 네트워크 토폴로지가 동적으로 변화되는 특징이 있다.
- 애드 혹 네트워크는 완전 독립형이 될 수도 있고, 인터넷 게이트웨이를 거쳐 인터넷과 같은 기반 네트워크와 연동될 수 있다.
- 애드 혹 네트워크 활용 분야는 긴급 구조, 긴급회의, 전챙터에서의 군사 네트워크가 있다.

## 네트워크 설치 구조(토폴로지) 종류
- **버트링성**

1. 버스형 구조  
**하나의 네트워크 회선**에 여러 대의 노드가 멀티 포인트로 연결된 구조 형태이다.  
- | 장점                 | 단점                                          |
  | :------------------ | :-------------------------------------------- |
  | 구조가 간단하기 때문에 설치가 용이, 비용이 저렴<br>네트워크 회선에 노드 추가 및 삭제가 용이 | 노드를 무분별하게 추가할 경우 네트워크 성능 저하<br>네트워크   회선의 특정 부분 고장 시 전체 네트워크에 영향을 끼침 |

2. 트리형 구조  
각 노드가 **계층적으로 연결**되어 있는 구성 형태로 나뭇가지가 사방으로 뻗어 있는 것과 유사한 모양의 구조 형태이다.
- | 장점                 | 단점                                          |
  | :------------------ | :-------------------------------------------- |
  | 허브만 준비되어 있다면 많은 단말 노드를 쉽게 연결이 가능 | 모든 네트워크가 허브를 통해서 이루어지므로 스타형처럼 허브가 고장이 나면 연결된 단말 노드의 네트워크가 제한됨 |

3. 링형 구조  
**모든 노드가 하나의 링에 순차적으로 연결**되는 형태이다.
- | 장점                 | 단점                                          |
  | :------------------ | :-------------------------------------------- |
  | 네트워크 회선에 단말 노드를 추가하거나 삭제하는 등의 네트워크 재구성이 용이 | 링의 어느 한 부분에 장애가 발생하면 전체 네트워크에 영향 |

4. 성형 구조
각 단말 노드가 **허브**라는 네트워크 장비에 **점 대 점**으로 연결되어 있는 구성 형태이다.
- | 장점                 | 단점                                          |
  | :------------------ | :-------------------------------------------- |
  | 소규모의 네트워크 설치 및 재구성이 간편 | 중앙 허브가 고장이 나면 전체 네트워크에 영향 |

## 다중화기(MultiPlexer)
다중화기는 하나의 회선을 통해 일정한 시간이나 주파수로 나누어서 전송하게 하는 장비이다.
- 주파수 분할 다중화(FDM; Frequency Division Muftiplexing)
  - 하나의 주파수 대역폭을 다수의 작은 대역폭으로 분할하여 전송하는 방식
- 시간 분할 다중화(TDM; Time Division MultipIedng)
  - 회선의 대역폭을 일정 시간으로 분할하여 전송하는 방식
- 코드 분할 다중화(CDM; Code Division Multiplexing)
  - 정해진 주파수 대역에 다수의 사용자가 서로 다른 코드를 사용함으로쩌 동일한 주파수로 동시에 다수가 접속해서 전송하는 방식