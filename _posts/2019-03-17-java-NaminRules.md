---
layout: single
title:  "가독성을 높이기 위한 명명 규칙"
date:   2019-02-09 20:56:35 +0900
categories: 
  - JAVA
---
## 명명규칙 (Naming Convention)

 1. 생산성과 가독성 향상
 2. 헝가리언 표기법, 파스칼 표기법, 카멜 표기법

---
  
# 명명 규칙1: 클래스명

* 클래스명은 반드시 <font color="red">대문자로 시작할 것</font>
* <font color="red">단어의 첫글자는 대문자</font>로 쓴다
* 해당클래스가 어떤 <font color="blue">목적</font>으로 만들어졌는지 유추할 수 있는 이름

``` java

//클래스의 첫글자를 대문자 표기
public class Profile{}

//User와 Profile이라는 단어의 조합으로 단어의 첫글자(U,P)를 대문자 표기
public class UserProfile{}

//User와 Profile이라는 단어의 조합으로 단어의 첫글자(U,P)를 대문자 표기
//유저정보를 관리하는 클래스임을 유추가능 
public class UserProfileManager{}

```

# 명명 규칙2: 메서드명

* 메서드명은 반드시 <font color="red">소문자로 시작할 것</font>
* 메서드의 첫글자를 제외한 <font color="red">단어의 첫글자는 대문자</font>로 쓴다
* 메서드는 기능을 담당하므로 <font color="red">동사</font>로 시작
* 해당메서드가 어떤 <font color="blue">목적</font>으로 만들어졌는지 유추할 수 있는 이름

# 명명 규칙3: 속성명

* 속성명은 반드시 <font color="red">소문자로 시작할 것</font>
* 속성의 첫글자를 제외한 <font color="red">단어의 첫글자는 대문자</font>로 쓴다
* 메서드는 기능을 담당하므로 <font color="red">명사</font>로 시작

# 명명 규칙4: 상수명

* <font color="red">모든글자를 대문자</font>로 표현할 것
* 단어와 단어 사이는  <font color="red">언더바 [_]</font>로 구분

``` java

//속성
private Sting firstName;
private UserProfile userProflie = new UserProfile();

//상수
private String NAME = "lee";

//메서드
//Remove, Empty, Space이라는 단어의 조합으로 메서드의 첫글자(r)를 소문자 표기 나머지 단어의 첫글자(E,S)를 대문자 표기
// 빈공간을 제거하는 기능을 할 것으로 추정 가능
public String removeEmptySpace(){}

```




