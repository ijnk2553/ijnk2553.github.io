---
layout: post
title:  "객체 지향 프로그래밍 002"
date:   2019-02-16 19:35:35 +0900
categories: jekyll update
---
## 속성 

* 클래스를 구성하는 데이터들의 특성을 표현

> 메서드 영역밖에서 변수를 선언하고 어디서든 접근이 가능 `클래스변수 `
>
> 메서드 실행부에 선언된 변수 `지역변수 `는 속성이 될 수 없다.

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

