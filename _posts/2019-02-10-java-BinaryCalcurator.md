---
layout: single
title:  "2진수 계산 출력"
date:   2019-02-09 20:56:35 +0900
categories:
  - JAVA
tags:
  - content
  - css
  - edge case
  - lists
  - markup
---

## 2진수 계산 문제 풀이

* 문제내용

>10진수를 입력 받아 2진수로 변환하는 프로그램을 작성하시오			
>
>			
><10진수 → 2진수>			
>입력 예 : 26			
>출력 예 : 11010	

---

## 진수란

* __10진수__ : 0~9 `10가지` 숫자로 표현
* __2진수__  : 0~1 `2가지` 숫자로 표현

# 진수계산방법

* Ex1) 128을 10진수로 계산 하는 경우

![calcurator_10](https://user-images.githubusercontent.com/47468250/52527649-9e978400-2d0f-11e9-90ca-9ee29ced332d.png)


* Ex2) 10진수 26을 2진수로 계산 하는 경우

![calcurator_2](https://user-images.githubusercontent.com/47468250/52527678-edddb480-2d0f-11e9-9044-1d67fe6862bb.png)

* ## 몫이 0일 될때까지 몫을 진수로 `계속` 나누어 몫이 0이되면 나머지를 `역순`으로 출력

> * 계속 처리 : 반복문!
>     - 반복문의 종료 조건 : 몫이 0이 됨
> * 역순 출력 : 문자열의 앞에 문자열을 추가한 후 출력.

---

# 2진수 계산 풀이 간단 설계

```
    1. 10진수 값을 입력 받아서 inupt변수에 세팅한다.
    2. 1에서 입력 받은 input변수값을 몫변수에 세팅한 후 다음 처리를 반복한다.
         2-1. 몫변수를 진수값으로 나머지연산을 한 값을 나머지변수에 세팅한다.
         2-2. 몫변수를 진수값으로 나눈 값을 몫변수에 세팅한다.
         2-3. output문자열의 앞에 나머지변수값을 추가한다.
         2-4. 몫변수값이 0이면 처리를 종료한다.
    3. 2에서 계산한 output문자열의 값을 출력한다.
```


# 2진수 계산 JAVA소스

```java
package jp.co.gcstest;

import java.util.Scanner;

public class BinaryCalcurator {

	public static void main(String[] args) {
		int inputValue;
		int moc;
		int jinsu = 2;
		int nameaji;
		String outputValue = "";
		
		//1. 10진수 값을 입력 받아서 inupt변수에 세팅한다.
		Scanner sc = new Scanner(System.in);
		System.out.println("2진수로 변환할 10진수 값을 입력하세요.");
		inputValue = sc.nextInt();
		
		//2. 1에서 입력 받은 input변수값을 몫변수에 세팅한 후 다음 처리를 반복한다.
		moc = inputValue;
		while(moc > 0) { //2-4. 몫변수값이 0이면 처리를 종료한다.
			//2-1. 몫변수를 진수값으로 나머지연산을 한 값을 나머지변수에 세팅한다.
			nameaji = moc % jinsu;
			//2-2. 몫변수를 진수값으로 나눈 값을 몫변수에 세팅한다.
			moc = moc / jinsu;
			//2-3. output문자열의 앞에 나머지변수값을 추가한다.
			outputValue = nameaji + outputValue;
		}
		
		//3. 2에서 계산한 output문자열의 값을 출력한다.
		System.out.println(outputValue);
	}

}
```