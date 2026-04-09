---
title: "Ontology 만들기 101: 아버지 클래스 정의"
date: 2004-08-12
draft: true
unpublished: true
tags: ["Ontology", "owl", "semantic web"]
categories: ["카테고리 없음"]
---

<!--more-->

OWL로 데이터 모델링도 좋고 지식 모델링도 좋고 여하간 뭔가를 표현할라 치면 여러 어려운 문제에 부딛히게 된다. 클래스로 정의할까 인스턴스로 할까, 속성으로 정의할까 클래스로 정의할까 애매한 상황도 많고 아예 OWL로 표현 자체가 불가능해 보이는 개념들도 자주 마주하게 된다.


OWL은 세상을 클래스, 속성, 개체들로 나누고 이들간의 관계를 정의하는 언어이므로 OWL을 사용할 때도 이러한 시각이 필요하겠다. 가장 중요한 것은 표현하고자 하는 개념을 클래스의 관점으로 생각해 보는 노력이 필요하다는 점이다. 가장 간단한 예로 "아버지"라는 개념을 보자. 세상의 모든 사람들 중에 어떤 사람들이 "아버지"일까? 전체 개체들의 집합에서 특정 개념에 속하는 개체들을 특징지울 수 있는 특성을 찾아내는 노력이 클래스 정의에 매우 유용하다. "아버지"의 특성을 생각해 보면 다음과 같은 목록이 만들어진다.


- 아버지는 사람이다.

- 아버지는 남자이다.

- 아버지는 결혼한 사람이다.

- 아버지는 자식을 하나 이상 가진다.


이제 위의 특성들을 OWL로 기술해 보면 다음과 같다.


```
Class(Man)
Class(Woman)
Class(Human complete unionOf(Man, Woman))
Class(MarriedMan partial Man restriction(hasWife minCardinality(1)))
Class(Father partial MarriedMan restriction(hasChild minCardinality(1)))
```


^^;;;


*- 2005년 1월 31일에 Father 정의 갱신. Man, Woman, Human 클래스 정의 추가하고, MarriedMan 클래스를 Human이 아닌 Man 클래스의 하위 클래스로 정의.*게시글 관리
