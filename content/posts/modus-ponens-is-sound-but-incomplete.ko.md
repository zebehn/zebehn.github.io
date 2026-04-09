---
title: "Modus Ponens is sound but incomplete."
date: 2007-07-02
draft: true
unpublished: true
tags: ["Artificial Intelligence", "logic"]
categories: ["카테고리 없음"]
---

<!--more-->

Russell의 'Artificial Intelligence: A Modern Approach'에 나온 예제다. Modus Ponens는 First-Order Logic 문장들에 대해 Sound하지만 Incomplete한 추론을 한다.


```
P → Q
⌉P → R
Q → S
R → S
```


Complete한 추론 규칙이라면 S를 유도해내야 한다. P 또는 ⌉P 중 하나는 반드시 참일 것이기 때문이다. 하지만, Modus Ponens는 못한다. -_-게시글 관리
