---
layout: post
title: Swift 기초 | 문자열 삽입 (String Interpolation)
description: >
   문자열 삽입(String Interpolation)에 대해서 알아보자.
tags: [Swift]
comments: true
related_posts:
  - ios/_posts/2021-08-10-100daysofswift-day1-4.md
  - ios/_posts/2021-08-10-100daysofswift-day1-6.md
---

현재까지 코드에 문자열 값을 직접적으로 입력하는 것을 보았다. 그러나 Swift는 추가적으로 문자열에 변수를 삽입함으로써 문자열을 더 유용하게 사용할 수 있는 **문자열 삽입(String Interpolation)** 기능을 제공한다.

임의의 데이터 타입을 문자열에 삽입할 수 있다. 그저 `\` 뒤에 괄호에 감싼 변수를 입력하면 된다.

~~~swift
var score = 85
var str = "Your score was \(score)"
~~~

Playground 결과란을 보면 `str` 변수의 값을 "Your score was 85"로 저장한 것을 확인할 수 있다.

이는 몇 변이고 문자열을 사용해서 문자열을 만들 수 있다.

~~~swift
var results = "The test results are here: \(str)"
~~~

나중에 보면 알겠지만, 문자열 삽입 기능은 변수를 삽입하는것 뿐만아니라 그 안에서 코드를 실행할 수도 있다.


## 문자열 삽입 기능은 왜 제공하는 것일까?

사용자에게 정보를 보여줄 때, 메시지든, 텍스트든, 버튼이든 문자열을 사용할 수 밖에 없을 것이다.

당연히 사용자에게 여러 가지 관련 데이터를 보여주어야 하기 때문에 정적인 문자열만을 가지고는 한계가 있을 것이다. 이 때문에 Swift는 런타임에 생성된 커스텀 데이터를 주입할 수 있도록 문자열 삽입 기능을 제공하는 것이다.

~~~swift
var city = "Seoul"
var message = "Welcome to \(city)!"
~~~

물론 앞선 예시에서는 도시 이름을 바로 문자열에 입력할 수도 있었을 것이다. 하지만 실제 앱에서는 실세계의 유저데이터를 보여주어야 하기 때문에 이를 동적으로 삽입하는 것이 굉장히 중요하다.

Swift에서는 그 어떤 타입의 데이터도 문자열 삽입을 이용해서 문자열에 끼워 넣을 수 있다. 결과물이 항상 유용한 것으 아니겠지만 Swift의 기본 데이터 타입인 문자열, 정수, 불 등을 사용하면 적절한 결과물을 얻어낼 수 있다.
