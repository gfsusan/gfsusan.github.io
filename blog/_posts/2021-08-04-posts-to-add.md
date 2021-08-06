---
layout: post
title: Posts Contents To Be Added In the Future
description: >
  개발을 진행하면서 맞딱드렸던 문제들, 까먹기 전에 주제라도 기록하자.
categories: [blog]
tags: [Navi, iOS, Swift]
related_posts:
  none
---

# 앞으로 업로드할 개발 내용들 Checklist ✅

개발 하면서 자주 맞딱드리는 문제들이 있다. 이전에 마주한 문제라는 것을 알지만 매번 똑같이 구글링하고 같은 해결 과정을 반복한다. 앞으로는 문제 해결 과정을 나의 블로그에 기록하고자 한다.

## 1. TableHeaderView가 제대로 나타나지 않는 현상
테이블 헤더 뷰를 지정하였더니
 - Large Title 가 작게 나온다.
 - 헤더 뷰가 런칭 시에는 나타나지 않고, 테이블 뷰에 스크롤 이벤트가 발생하면 '반짝✨' 하고 나타난다. ㅂㄷㅂㄷ

### 해결 방법


``` swift
  tableHeaderView = verseView
  verseView.widthAnchor.constraint(equalTo: widthAnchor).isActive = true
  verseView.heightAnchor.constraint(equalToConstant: 100).isActive = true

  // Header View가 바로 나타나지 않는 현상 해결
  if let headerView = self.tableHeaderView {

      // Update the size of the header based on its internal content.
      headerView.layoutIfNeeded()

      // ***Trigger table view to know that header should be updated. -> 신박하다!!!
      let header = self.tableHeaderView
      self.tableHeaderView = header
  }

```

> layoutIfNeeded()`에 대해서 알아봐야 겠다.
