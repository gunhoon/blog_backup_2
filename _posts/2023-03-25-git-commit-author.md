---
layout: post
title: git commit author 변경
date: 2023-03-25 13:50:00 +0900
category: git
tags: git
permalink: /1
---
개발하면서 가끔 한 번씩 사용하는 명령어들이 있다. 자주 사용하는 것이 아니다 보니 기억이 가물가물하여 매번 찾아봐야 한다. 이런 명령어들을 하나씩 포스팅하여 보자.

git에서 이미 commit된 코드의 author를 변경할 수가 있다.

## commit된 author 변경하기

아래와 같이 author를 변경하고, edit 모드로 진입하여 commit message도 수정할 수 있다.

```bash
git commit --amend --author "Author Lee <author@example.com>"
```

no-edit 옵션으로 commit message 수정없이 author만 변경할 수도 있다.

```bash
git commit --amend --no-edit --author "Author Lee <author@example.com>"
```

## commit된 author와 date 변경하기

reset-author 옵션을 사용하여 author를 설정값으로 reset할 수도 있다. 다만, 이것은 date도 현재 날짜와 시간으로 같이 reset된다.

```bash
git commit --amend --no-edit --reset-author
```
