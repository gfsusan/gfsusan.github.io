---
layout:     post
title:      My First Blog Entry
description: >
  처음 Hydejack 테마를 사용하면서 설정한 것, 기억할 내용들
categories: [blog]
related_posts:
  none
---

# My First Blog Entry!

처음 github pages 통해서 열었을 때, blank 화면이 떴다. 이 문제를 해결하기 위해서 약 3시간의 삽질을 진행해야 했다... 긴 시간 끝에 이 문제를 해결한 방법을 기록하려고 한다.

첫 번째로는 `_config.yml` 파일 안에서
``` yml
# Theme
# ---------------------------------------------------------------------------------------

theme: jekyll-theme-hydejack
remote_theme: hydecorp/hydejack@v9.0.0-rc.6
```
해당 부분 중 `remote_theme: hydecorp/hydejack@v9.0.0-rc.6` 부분이 주석처리 되어 있었다. 우선 주석처리 되어 있는 이 부분을 주석 해제해야 했다.

이후에도 똑같이 빈 화면이 나타나는 부분은 터미널에서 `bundle install`을 실행하고 `bundle exec jekyll run`을 실행한 후 업데이트 된 `Gemfile.lock`을 원격 리포지터리에 `push`한 한 후에야 제대로 사이트가 나타나는 것을 확인할 수 있었다.

## 2번 헤더

이것도 내용이다.  
깔깔
