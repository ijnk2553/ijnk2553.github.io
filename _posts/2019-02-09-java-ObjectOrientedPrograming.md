---
layout: post
title:  "객체지향프로그래밍 001"
date:   2019-02-09 20:56:35 +0900
categories: jekyll update
---
# 객체지향 프로그래밍의 목적

 1. 생산성 향상
   * 한번에 보다 많은 양의 개발이 가능
 2. 편리한 유지보수
 3. 재사용성

 **객체지향 프로그래밍**은 프로그래밍의 기본단위인 `클래스`와 `객체`를 다루는 `방법론`이다.

---
  
  


# 객체란 무엇인가

>연필 `객체`은 필기를 위한 사물, 커피 `객체`는 사람들이 마시기위한 목적으로 재배 가공된 사물, 커피를 마시는 행위를 하는 사람 `객체`
>
>각 객체들은 목적과 행위를 가짐
>
>연필 `객체`로 커피주문서를 작성 -> 고객 `객체`과 종업원 `객체`이 주문서 `객체`와 돈 `객체`을 주고받음 -> 고객 `객체`이 커피 `객체`를 받아옴
>
>객체들이 유기적으로 동작할때 커피주문이라는 시스템이 완성



**객채**는 `데이터` 혹은 `기능`을 `보유`하고 있어, 그 `목적`을 `수행`하는 것이다.



---



## 클래스
  * 객체를 만들기 위한 기능 명세서/ 설계서

## 객체
 * 클래스를 이용하여 만들어낸 결과물

하나의 `클래스`는 여러 개의 `객체`를 `생성`할 수 있다.

`클래스`와 `객체`는 메모리에 `생성`되었는지 여부에 의해 구분한다.

## 클래스 선언 방법
> 【 제어자 】  class  【 클래스명 】  {    ...    }

```java
package jp.co.gcstest;

public class HelloWorld {

}
```

## 객체 생성 방법

> 【 클래스명 】  【 객체명(변수명) 】 = new 【 클래스의 생성자 】 ;

```java
package jp.co.gcstest;

public class HelloWorldObjectTest {

	public static void main(String[] args) {
		HelloWorld helloWorld = new HelloWorld(); //HellWorld 클래스의 helloWorld 객체가 메모리에 생성됨
	}

}
```

---


## 인스턴스화 / 추상화
> * **인스턴스화** : 클래스로부터 새로운 객체를 생성 `메모리에 할당` 하는 과정 
> * **추상화** : 개발자가 만들고자 하는 객체의 기능과 속성을 `논리적으로` 뽑아내어 클래스로 `설계`하는 과정 
  
---


# 클래스의 구성요소

![class_organization](https://user-images.githubusercontent.com/47468250/52521757-6c5e3600-2cbf-11e9-892a-087517fc404d.png)

> * __메서드__ 는 `객체의 기능`을 수행한다.
> * __속성(변수)__ 는 `객체의 데이터`를 의미한다.
> * __생성자__ 는 메서드의 한종류로 클래스의 `생성 방법을 정의`한다.

---

## 메서드
  * 명령 구문들의 묶음

### 메서드 선언 방법
> 【 접근제어자 】  【 반환데이터형 】 【 메서드명 】 ( 【 매개변수데이터형 `parameter_type` 】 【 매개변수명 `parameter_name` 】 ) { ... }
>
>
> 반환데이터값이 필요없는 경우 __void__ 를 사용
>
>【 접근제어자 】  void 【 메서드명 】 ( 【 매개변수데이터형 `parameter_type` 】 【 매개변수명 `parameter_name` 】 ) { ... }
>
```java
package jp.co.gcstest;

public class HelloWorld {

	/**
	 * 매개변수가 10인지 아닌지 체크
	 * @param param 체크대상이 되는 매개변수
	 * @return 10일경우 : true, 10이외의 경우 false
	 */
	public boolean checkTen(int param) {
		if(param == 10) {
			return true;
		}
		return false;
	}
	
	/**
	 * 매개변수를 출력
	 * @param param 출력대상이 되는 매개변수
	 */
	public void outputParam(int param) {
		System.out.print(param);
	}
}
```


### 메서드 사용방법
> 【 클래스명 】  【 객체명 】 = new 【 클래스의 생성자 】 ;
>
> 【 데이터형 】  【 변수① 】 = 【 객체명 】.메서드명 ( 【 매개변수 】 )
> * 변수①의 데이터형은 메서드의 반환데이터 형과 일치 해야한다.

```java
package jp.co.gcstest;

public class HelloWorldObjectTest {

	public static void main(String[] args) {
		
		boolean returnValue;
		int paramNine = 9;
		
		HelloWorld helloWorld = new HelloWorld();
		
		returnValue = helloWorld.checkTen(10); //returnValue의 데이터형은 checkTen메서드의 반환데이터형과 일치해야
		returnValue = helloWorld.checkTen(paramNine);
		helloWorld.outputParam(paramNine);//보이드 메서드
	}

}

```