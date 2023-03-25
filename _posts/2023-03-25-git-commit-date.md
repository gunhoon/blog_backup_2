---
layout: post
title: git commit date 변경
date: 2023-03-25 17:00:00 +0900
category: git
tags: git
permalink: /2
---
git에서 이미 commit된 코드의 날짜(date)를 변경해 보자. 며칠 지난 commit을 현재 날짜로 수정해서 push할 때 종종 사용한다.

## commit된 author date 변경하기

commit의 author date를 현재 날짜 및 시간으로 변경하기 위해서는 아래와 같은 명령어를 사용한다. 

```bash
# $(date -Iseconds)는 date를 ISO 8601 포맷으로 변경하는 옵션이다.
# 그냥 $(date)는 날짜가 한글 포맷으로 출력될 경우 git이 날짜를 제대로 인식 못하는 문제가 있다. 
git commit --amend --no-edit --date=$(date -Iseconds)
```

reset-author 옵션을 사용하여 author date를 현재 시간으로 리셋할 수도 있다. 이 옵션은 date 뿐만 아니라 author도 reset하여 현재 설정된 author로 같이 변경한다. 

```bash
git commit --amend --no-edit --reset-author
```

## author date를 지정된 날짜로 변경하기

현재 날짜가 아닌 특정 날짜로 author date를 변경할 수도 있다. 일반적으로 알려진 날짜 포맷을 넘겨주면 된다.

```bash
git commit --amend --no-edit --date="Sat Mar 25 17:00:00 2023 +0900"
```

```bash
git commit --amend --no-edit --date="2023-03-25T17:00:00+09:00"
```
