---
title: "[정보처리기사] 디자인 패턴(Design Pattern)"
layout : single
categories : certificate
toc : true
toc_label: "Table of Contents"
toc_icon: "bars"
toc_sticky: true
author_profile : false
tag : [정보처리기사]
sidebar :
    nav : "docs"
---

## 디자인 패턴(Design Pattern)이란?
- 소프트웨어 프로그램을 개발할때 참조할 수 있는 해결책 또는 예제
- 아키텍처 패턴이 디자인 패턴보다 상위 수준의 설계에 사용됨
- 서브시스템에 속하는 **컴포넌트들과 그 관계**를 설계하기 위한 참조 모델
cf) 아키텍처 패턴은 **전체 시스템의 구조**를 설계하기 위한 참조 모델

## 목적에 따른 디자인 패턴 유형
- **생구행**

### 생성 패턴(Creational Pattern) ★
- **추빌팩프싱**
- **추**상 팩토리(Abstract Factory) : 서로 연관, 의존하는 객체들을 그룹으로 생성해 추상적으로 표현
- **빌**더(Builder) : 객체의 생성 과정과 표현 방법 분리 → 동일한 객체를 생성해도 **서로 다른 결과**
- **팩**토리 메소드(Factory Method) : 객체를 생성하기 위한 인터페이스를 정의하여, 어떤 클래스가 인스턴스화될 것인지는 **서브클래스가 결정**하도록 하는 것(**Virtual-Constructor**패턴)
- **프**로토타입(Prototype) : 원본객체를 **복제**하는 방법으로 객체 생성 비용이 저렴
- **싱**글톤(Singleton) : 하나의 객체를 여러 프로세스가 **동시에 참조할 수 없음**

### 구조 패턴(Structural Pattern) ★
- **어브컴데 퍼플프**
- **어**댑터(Adapter) : **호환성이 없는 클래스** 인터페이스를 이용할 수 있도록 변환해주는 패턴
- **브**리지(Bridge) : **구현부에서 추상층을 분리**하여 독립적으로 확장 및 다양성을 가지는 패턴
- **컴**포지트(Composite) : 여러 객체를 가진 **복합, 단일 객체**를 구분 없이 다룰 때 사용하는 패턴
- **데**코레이터(Decorator) : 상속을 사용하지 않고도 객체의 기능을 **동적으로 확장**해주는 패턴
- **퍼**싸드(Facade) : 서브 클래스들의 **기능을 간편하게** 사용할 수 있도록 하는 패턴 Ex) 리모컨
- **플**라이웨이트(Flyweight) : **공유**해서 사용함으로써 **메모리를 절약**하는 패턴
- **프**록시(Proxy) : **접근이 어려운 객체**를 연결해주는 **인터페이스 역할**을 수행하는 패턴

### 행위 패턴(Behavioral Pattern)
- 생성 패턴과 구조 패턴에 **해당 안되면 행위 패턴**
- 책임 연쇄(Chain of Responsibility) : 한 객체가 처리하지 못하면 **다음 객체로 넘어가는** 패턴
- 커맨드(Command) : 요청에 사용되는 각종 **명령어**들을 추상, 구체 클래스로 분리하여 단순화함
- 인터프리터(Interpreter) : 언어에 **문법 표현을 정의**하는 패턴
- 반복자(Iterator) : **동일한 인터페이스를 사용**하도록 하는 패턴
- 중재자(Mediator) : **서로의 존재를 모르는 상태**에서도 **협력**할 수 있게 하는 패턴
- 메멘토(Memento) : 요청에 따라 객체를 해당 시점의 상태로 **돌릴 수 있는 기능을 제공**하는 패턴
- 옵저버(Observer) : **관찰 대상**의 변화를 **탐지**하는 패턴
- 상태(State) : 객체의 **상태에 따라** 동일한 동작을 다르게 처리해야 할 때 사용하는 패턴
- 전략(Strategy) : 클라이언트에 **영향을 받지 않는 독립적인 알고리즘**을 선택하는 패턴
- 템플릿 메소드(Template Method) : 유사한 서브 클래스를 묶어 **공통된 내용을 상위 클래스에 정의**하는 패턴
- 방문자(Visitor) : 필요할 때마다 해당 클래스에 **방문해서 처리**하는 패턴