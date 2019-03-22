---
layout: single
title:  "객체 지향 프로그래밍 003"
date:   2019-03-17 09:46:35 +0900Z
comments: true
categories:
     - JAVA
---
## 객체 지향 프로그램 설계 

* 프로그램의 생산성과 성능의 향상을 위해 객체를 만들고 그 객체들간의 관계를 정의하여 프로그램의 흐름을 제어

> **Object Oriented Programming** : 기능과 데이터를 가진 것들을 만들어, 프로그램을 구성하는 기법 
>
>
> **객체 지향 프로그래밍**은 데이터나 정보의 표현에 중점을 두고 객체를 만들어 프로그램을 설계하는 것

* 객체 지향 프로그래밍 설계의 4가지 요소
    * 추상화 `Abstraction`
	* 상속 `Inheritance`
	* 캡슐화 `Encapsulation`
	* 다형성 `Polymophism`

---

# 추상화 (Abstraction)
* 객체를 설계하는 기초 단계

> **추상 :** 여러가지 사물이나 개념에서 `공통`되는 특성이나 속성을 추출해 파악하는 작용
>
> * 객체에 필요한 기능을 파악하고 분류
> * 정의된 `객체의 기능`은 클래스의 `메소드`
> * 정의된 `객체의 데이터`는 클래스의 `속성`


* 추상화 예시 : 고객 관리 프로그램

> **기능 요건**
>
> 1. 고객관리 프로그램은 고객과 마일리지 정보를 저장, 처리한다.
> 2. 고객관리 프로그램에서 제공하는 기능은 데이터 생성, 수정, 저장이다.


 **추상화**
 필요한 객체: 고객 정보 표형 객체, 마일리지 정보 표현 객체, 객체들을 처리(생성, 수정, 삭제)하는 객체
 1. CustomerManager:고객 정보 처리 객체
 2. CustomerValue: 고객 정보 객체
 3. MileageValue: 마일리지 정보 객체


``` java
public class CustomerManager{
	CustomerValue customer;
	MileageValue maileage;

	public void create(){}

	public void delete(){}

	public void update(){}

	public void store(){}
}
```

CustomerManager클래스가 속성 customer와 mileage에 저장된 데이터와 각 기능을 처리하는 메서드들을 이용하여 고객 관리 프로그램을 구현을 추상화

---

# 상속 (Inheritance)

> **상속** : 자신의 모든 것들을 다음 세대에 물려주는 것
>
>두 클래스중 한 클래스가 갖고 있는 속성과 메서드들을 다른 클래스에게 물려주는 것
> **부모** `상위` 클래스 (<font color="Red">Super Class</font>): 물려 주는 역할
> **자식** `하위` 클래스 (<font color="Blue">Sub Class</font>): 상속 받는 역할

상속 기법을 올 바르게 적용 하기 위한 <font color="DeepPink">is-a</font> 법칙

* <font color="blue">Sub class</font> is a <font color="red">Super class</font>

>CowValue, HorseValue, AnimalValue 간의 상관관계
> * CowValue is a AnimalValue <font color="blue">(O)</font>
> * HorseValue is a AnimalValue <font color="blue">(O)</font>
> * CowValue is a HorseValue <font color="red">(X)</font>

상속을 위한 명령어
* **Extends** : 클래스 <font color="red">하나</font>만 상속 가능
* **Implements** : 인터페이스 <font color="red">하나 이상</font> 상속 가능

---

# 캡슐화(Encapsulation)

> **캡슐화** : 캡슐에 넣기, 소중히 보관함
>
>객체 지향적 의미
> * 서로 관련 있는 기능이나 데이터를 한 곳으로 모아서 효율적으로 관리 및 사용할 수 있도록 하는 것
>
> * 꼭 필요한 데이터나 기능만 외부에 노출 시키는 것

효율적인 데이터 관리를 위해서는 <font color="green">서로 연관있는 데이터만이 하나의 객에 선언</font>되어야 할 것
관련있는 것끼리 모아 클래스를 만드는 것이 `캡슐화`

외부에서 클래스를 호출했을 경우, 클래스 내부에 있는 데이터가 어떻게 동작하는지 알 필요 없이 개발자가 원하는 결과값만 얻게 되는것

<font color="purple">무결성 유지 가능</font> : 내부의 중요한 데이터가 노출되지 않기 때문

---

# 다형성(Polymorphism)
> 다양한 형태의 성질을 가지는 것

하나의 기능을 수행하지만 형태를 다양하게 가질 수 있는 기법

예)
 * [String클래스의 여러 함수 들](https://docs.oracle.com/javase/7/docs/api/)
