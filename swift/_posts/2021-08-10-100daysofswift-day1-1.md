---
layout: post
title: Swift 기초 | 변수
description: >
    변수에 대해서 알아보자.
tags: [Swift, iOS]
comments: true
related_posts:
  - swift/_posts/2021-08-10-100daysofswift-day1-2.md
---


> "The secret to getting ahead is getting started" - Mark Twain

Xcode를 실행하여 "Get Started with a Playground"를 선택하면 Swift 코드를 작성하고 즉시 결과를 볼 수 있는 샌드박스인 Playground가 만들어진다.

## 변수
Playground는 다음과 같이 변수를 정의하는 코드 한 줄로 시작한다.

~~~swift
var str = "Hello, playground"
~~~

이는 `str`이라는 새 변수를 생성하고, "Hello, playground"라는 값을 지정한다. Playground의 우측에서 "Hello, playground"라는 결과값을 확인할 수 있는데, 이는 값이 지정되었음을 Xcode에서 보여주는 것이다.

`str`은 변수이기 때문에 값을 바꿀 수 있다.
~~~swift
str = "Goodbye"
~~~

두 번째에서는 변수가 이미 생성된 상태이기 때문에 `var`이라는 키워드를 작성할 필요 없이 변수의 값을 바꾸면 된다.

### Swift에 변수는 왜 필요할까?
변수는 프로그램에서 임시의 정보를 저장할 수 있도록 해주며, 대부분의 Swift 프로그램에서 중요한 역할을 수행한다. 궁극적으로 프로그램은 어떤 방식으로든 데이터를 변형한다. 사용자로부터 투두리스트 항목을 입력받고, 완료된 항목을 체크한다던지, 디바이스 시간을 읽어 시계에 보여준다던지 등 여러 가지 형태의 데이터를 "어떻게든 변환"하여 사용자에게 보여준다.

데이터를 메모리 상에 저장 할 때 -- 사용자가 입력한 내용이나 인터넷에서 다운로드 받은 내용을 저장할 때 -- 변수가 사용된다.

`var`을 사용해서 변수를 생성하고 나면, 다시 `var`을 사용할 필요 없이 아무 때나 변수의 값을 변경할 수 있다.

~~~swift
var favoriteShow = "Orange is the New Black"
favoriteShow = "The Good Place"
favoriteShow = "Doctor Who"
~~~

`var`을 "새로운 변수를 생성한다"라고 읽으면 도움이 될 수 있다. 즉, 코드의 첫 번째 줄을 '`favoriteShow`라는 새로운 변수를 생성하고, Orange is the New Black이라는 값을 지정한다'라고 읽을 수 있다. 2, 3번째 줄은 `var`이 없기 때문에 새로운 변수를 생성하는 것이 아니라 이미 존재하는 값을 변경하는 것이다.

3줄 모두에 `var`이 있었다고 상상해보자. 모든 줄에 `var favoriteShow`를 사용한 것이다. 이는 '`favoriteShow`라는 새로운 변수를 생성한다'를 세 번 한 것과 같으므로, 첫 번째 줄 이후에는 명백히 틀린 말이 된다. Swift는 이런 에러에 대한 플래그를 세울 것이고, 각 변수가 각각 다른 일믕르 사용하기 전까진 코드를 실행할 수 없도록 할 것이다.

이는 굉장히 까다로워 보일 수 있지만, 사실상 도움이 된다. Swift는 개발자가 이미 존재하는 변수를 수정하고 싶은 것인지, 새로운 변수를 만드려고 하는 것인지 확실하게 하기를 원한다.
