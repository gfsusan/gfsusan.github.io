---
layout: post
title: Swift 기초 | 여러줄 문자열
description: >
   여러줄 문자열에 대해서 알아보자.
tags: [Swift]
comments: true
related_posts:
  - swift/_posts/2021-08-10-100daysofswift-day1-2.md
  - swift/_posts/2021-08-10-100daysofswift-day1-4.md
---

기본 Swift 문자열은 따옴표("")를 사용하지만, 그 중간에 줄바꿈을 사용할 수 없다.

여러줄 문자열(Multi-line Strings)을 사용하고 싶으면 다음과 같이 세 개의 따옴표로 시작하고 끝나는 문법을 사용할 수 있다.

~~~swift
var str = """
This goes
over multiple
lines
"""
~~~

이와 같은 따옴표를 사용하려면 다음을 꼭 따라야 한다: 시작과 끝 따옴표 트리오(""")는 독립된 라인에 써야 하며, 시작과 끝의 줄바꿈은 최종 문자열에 포함되지 않는다.

만약 실제로 줄바꿈이 필요한 것이 아니라 코드를 보기 쉽게 만드는 용도로 여러줄 문자열을 사용하고 싶다면, 각 줄을 `\`로 끝내면 된다.

~~~swift
var str = """
This goes \
over multiple \
lines
"""
~~~

## 여러줄 문자열은 왜 필요할까?

Swift의 기본 문자열은 따옴표로 시작하고 따옴표로 끝난다. 그리고 그 중간에 줄바꿈이 포함될 수 없다. 예를 들면 다음과 같다.

~~~swift
var quote = "Change the world by being yourself"
~~~

이는 짧은 길이의 텍스트에서는 잘 동작하지만, 저장하고자 하는 텍스트가 길어질 수록 소스코드가 지저분해진다. 이때 여러줄 문자열이 유용하게 사용된다. 삼중 따옴표를 사용하면 문자열을 여러 줄에 걸쳐서 사용할 수 있으며, 코드에서 가독성이 향상된다.

~~~swift
var burns = """
The best laid schemes
O' mice and men
Gang aft agley
"""
~~~

Swift는 앞선 코드의 줄바꿈을 텍스트의 일부로 보기 때문에, 해당 문자열은 실제로 3개의 라인으로 구성된다.
