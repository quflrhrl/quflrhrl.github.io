---
title: "조건문( if문 & switch문 )"
categories:
  - Java
tags:
  - Java
  - if
  - switch
---


> 우선 Java에서는 프로그램의 흐름을 제어해야 할 때가 있다. 이때 사용하는 실행문으로 '**제어문**'이 사용되는데, 제어문에는 조건문, 반복문, 분기문 등이 포함된다. 이 중에서 조건문에 대해 먼저 알아보자!
> 

---

**조건문**은 말 그대로 조건식을 제시하고, 그 결과에 따라 true와 false값으로 프로그램의 흐름을 나누어 주는 역할을 하는 데, Java에서 사용하는 대표적인 조건문은 if문과 switch문이 있다.

- **if , switch 의 뜻**
    - I**f** (만약)…이면 (가정적 조건을 나타냄)
    - **switch** 전환,변경

---

# - if 문 -

If 문은 모든 조건식을 확인하고 다시 순차적으로 true / false 값을 확인하여 true(참)인 조건식의 문장, 명령을 실행한다. 때문에 여러 조건식 중 한 조건식에 오류 발생이 되더라도 모든 조건식을 확인한 뒤 오류가 발생이 된 조건식이 아닌 처음 작성된 조건식에서 오류가 발생이 된다.

### [ if 문의 형태 ]

- 단일 if 문
- 이중 if 문 ( if…else )
- 다중 if 문 ( if…else if…else )
- 중첩 if 문

---

## ● 단일 if 문

```java
if (조건식) { 
   // a
 }
```

 단일 if 문의 조건식이 true이면 ‘a’코드를 실행하고, false의 경우 ‘a’코드를 실행하지 않고 종료한다.

예제)

![단일if.GIF](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d84f1305-8a9f-44af-b4b6-7215ec8edcc0/%EB%8B%A8%EC%9D%BCif.gif)

 int 타입인 num에 10이 할당되었고, 조건식은 num이 양수인지 확인한다. 따라서 해당 예제는 조건식이 true이므로 "num은 양수입니다." 라는 결과가 출력된다.

 만약 num에 0이 할당된다면 조건식이 false가 되어 코드가 실행되지 않고 종료된다.

---

## ● 이중 if 문 ( if…else )

```java
if (조건식) { 
   // a
 } else {
   // b
 }
```

 이중 if 문의 조건식이 true이면 ‘a’코드를 실행하고, false의 경우 ‘b’코드를 실행하여 true와 false의 각각 다른 명령을 실행한다.

예제)

![이중if.GIF](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9a10dfe9-68b2-4bd0-88fc-4cd40ad5a97f/%EC%9D%B4%EC%A4%91if.gif)

 int 타입인 num에 9가 할당되었고, 조건식은 num이 10보다 큰지 확인한다. 해당 예제에서는 조건식이 false이므로 "num은 10보다 작다." 라는 결과가 출력된다.

 만약 num에 11이 할당된다면 조건식에서 true로 "num은 10보다 크다."라는 결과를 출력한다.

---

## ● 다중 if 문 ( if…else if…else )

```java
if (a조건식) { 
   // a
 } else if (b조건식) {
   // b
 } else {
   // c
 }
```

 다중 if 문의 a조건식이 true이면 ‘a’코드를 실행하고, else if 문의 b조건식이 true이면 ‘b’코드를 실행 하며 순차적으로 조건식에 true인 문의 코드를 실행시킨다.

이때 모든 조건에 false일 경우 else 문의 ‘c’코드를 실행한다.

예제)

![다중if.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ad3f0c7c-84fd-4a9f-af9d-6e5aae65ac98/%EB%8B%A4%EC%A4%91if.png)

 int 타입인 num에 7이 할당되었고, a 조건식에서 num이 9보다 큰지 확인한 뒤, a 조건식이 false일 경우 b 조건식인 num이 6보다 큰지 확인한다. 해당 예제는 a 조건식에서 false, b 조건식에서 true 이므로 "num은 9보다 작고 6보다 크다." 라는 결과가 출력된다.

 만약 num에 10이 할당된다면 a 조건식이 true로 "num은 9보다 크다."는 결과를 출력하고, num에 5가 할당된다면 a, b 조건식 모두 false이므로 "num은 6보다 작거나 같다."는 결과를 출력한다.

---

## ● 중첩 if 문

```java
if (a조건식) { 
 if (b조건식) {
   // b
  } else {
   // c
  }
 } else {
   // d
 }
```

 중첩 if 문의 a조건식과 b조건식 모두 true이면 ‘b’코드를 실행하고, a조건식이 true이나 b조건식이 false이면 else문의 ‘c’코드를 실행한다.

이 때 a조건식이 false이면 else문의 ‘d’코드를 실행한다. 

예제)

![중첩if.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7fc10f0e-41ba-4e1e-9100-858a167b191f/%EC%A4%91%EC%B2%A9if.png)

 int 타입인 num1은 5, num2는 8, num3은 10이 각각 할당됬다. a 조건식에서 num2가 num1보다 큰지 확인한 뒤, a 조건식이 true일 경우 b 조건식인 num2가 num3보다 큰지 확인한다. 해당 예제의 경우 a 조건식과 b 조건식 모두 true이므로 "num2는 num1보다 크고 num3보다 작다"라는 결과가 출력된다.

 만약 num2에 11이 할당된다면, a 조건식에서는 true가 되지만 b 조건식에서는 false가 되어 "num2는 num1과 num3보다 큽니다."라는 결과가 출력된다. 반면에 num2에 4가 할당된다면, a와 b 조건식 모두 false가 되어 "num2는 num1보다 작습니다."라는 결과가 출력된다.

---

# - switch 문 -

 switch 문은 모든 조건식을 확인하지 않아 true인 조건식의 명령을 실행 후 break 문에 의해 이후 조건식을 실행하지 않고 종료하여 if 문 보다는 빠르다는 장점이 있다.

그러나 break 문을 생략하면 입력값과 관계없이 순차적으로 값이 호출되어 주의하여야 하고, if 문과는 다르게 <, ≤, >, ≥ 와 같은 부등식을 사용한 조건식의 진위를 판별할 수 없어 어떤 값을 가진 대상과 일치 여부만 판별할 수 있어 조건식에 따라 사용 불가할 수도 있다.

```java
switch (조건식) {
 case A:
   // a
  break;
 case B:
   // b
  break;
 default:
   // c
}
```

 switch 문의 조건식에 대한 값이 true일 경우 동일한 값을 가진 case가 A면 ‘a’코드를, B면 ‘b’코드를 실행하고 break 문으로 종료가 되며, false이면 default 문의 ‘c’코드를 실행한다. 이때 default 문의 경우 생략 가능하다.

- **break 문**
    
    switch문, 반복문에 주로 반복을 종료하기 위한 방식으로 사용
    

예제)

![단일if.GIF](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e6b55e24-87a0-47da-8123-89573f7b11d2/%EB%8B%A8%EC%9D%BCif.gif)

 int 타입인 num에 2가 할당이 되었고, 조건식은 num일 경우 해당이 된다. 해당 예제에서 조건식에 true이므로 case를 확인한다. 이때 num과 같은 값을 가진 case 2의 “num의 값은 ‘2’이다.” 라는 결과가 출력 되고 break 문으로 인해 case 3은 확인하지 않고 종료가 된다.

 만약 조건식이 num이 아닌 num1일 경우 false로 default 문의 값인 “num의 값은 false이다.”는 결과를 출력한다.

---

> 이번 블로그 포스팅에서는 조건문인 if 문 & switch 문을 정리해 보았다. 그동안은 if 문을 아주 간략하게 기억하고 있었다는 것을 알게 되었고,  switch 문의 경우 if 문과 비교 시 속도가 빠른 장점과 조건식에 따라 간단한 코드로 동작이 가능한 장점, 또한 조건식이 복잡한 경우 case를 일일이 명시해야 하는 번거로움이 있을 수 있다는 것을 알게 되었다. 포스팅하며 그동안 겉핥기식으로 배운 것들을 더욱 세세하게 알아간다는 것이 블로그를 쓰는 장점이라는 것을 새삼 깨달았다.
>
