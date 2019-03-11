---
layout: single
title:  "객체 지향 프로그래밍 003"
date:   2019-02-24 19:35:35 +0900
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

# 추상화
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

> **추상화**
> 필요한 객체: 고객 정보 표형 객체, 마일리지 정보 표현 객체, 객체들을 처리(생성, 수정, 삭제)하는 객체
> 1. CustomerManager:고객 정보 처리 객체
> 2. CustomerValue: 고객 정보 객체
> 3. MileageValue: 마일리지 정보 객체

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

