---
layout: single
title:  "객체 지향 프로그래밍 003"
date:   2019-02-24 19:35:35 +0900
categories:
     - JAVA
---
## 객체지향프로그램 설계 

* 프로그램의 생산성과 성능의 향상을 위해 객체를 만들고 그 객체들간의 관계를 정의하여 프로그램의 흐름을 제어

> **Object Oriented Programming** : 기능과 데이터를 가진 것들을 만들어, 프로그램을 구성하는 기법 
>
> 객체지향프로그래밍은 데이터나 정보의 표현에 중점을 두고 객체를 만들어 프로그램을 설계하는 것

* 객체 지향 프로그래밍 설계의 4가지 요소
    * 추상화 `Abstraction`
	* 상속 `Inheritance`
	* 캡슐화 `Encapsulation`
	* 다형성 `Polymophism`

---

# 속성의 선언
> 【 데이터 타입 】 【 변수명 】  =  【 데이터 】 ;
>
> 【 클래스명 】 【 변수명 】  = new 【 생성자 】 ();
> * **클래스 영역 내부** 에서 선언되어야 함( **메서드 영역 밖**  )

``` java
package jp.co.gcstest;

public class AttributeTest {
	
	//클래스 영역의 안쪽
	//속성 선언
	int weight = 74;
	String name = new String("cookies");
	//메서드 영역의 바깥쪽 
	public void testMethod() {
		
	}

}
```

---

# 속성의 호출
> 객체를 생성하고 생성된 객체에 점(.)을 붙인 다음 속성명을 호출

``` java
package jp.co.gcstest;

public class AttributeCalling {

	public static void main(String[] args) {
		//객체를 생성
		AttributeTest attributeTest = new AttributeTest();
		//생성한 객체명에 (.)을 붙인 후에 속성을 호출
		attributeTest.weight = 80;
		attributeTest.name = "imma";

	}

}
```

---

# 그림판의 연필 객체
> 기능 : 그리기, 점찍기
>
> 특성 (데이터) : 색깔, 두께


* 연필 객체의 구성
    * 연필객체 설계를 위한 클래스 : Pencil
    * 색깔 데이터 표현을 위한 클래수변수 : color (데이터 타입 : Color)
    * 선의 두께 데이터 표현을 위한 클래스변수 : thickness (데이터 타입 : float)
    * 그리기 기능 구현을 위한 메서드 : drawLine()
    * 점직기 기능 구현을 위한 메서드 : drowDot()

``` java
package jp.co.gcstest;

import java.awt.Color;

public class Pencil {
	Color color;
	float thickness;
	
	public void drawLine() {
		System.out.println("--------------------");
	}
	
	public void drawDot() {
		System.out.println("........");
	}

}
```

---

## package
* 클래스가 어떤 패키지에 포함되어 있는지 명시적으로 표현

> package 【 패키지명 】;

## import
* 다른 클래스나의 메소드나 속성을 참조할 때, 명시적으로 표현

> import 【 패키지명 】.【 클래스명 】;
>
> import 【 패키지명 】.*;

``` java
package jp.co.gcstest;

import java.awt.Color;
```