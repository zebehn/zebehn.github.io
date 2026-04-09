---
title: "Comprehension Principle"
date: 2004-05-18
draft: true
unpublished: true
tags: ["logic"]
categories: ["카테고리 없음"]
---

<!--more-->

Comprehension
principle이란 무엇인가? OWL 추론 관련 일을 하면서 맞이하는 가장 어려운 점은 이상한 나라에서나 나옴직한 용어들과
시도때도 없이 대면해야 한다는 점이다. 이 모든 것이 학교 다닐 때 수업에 집중하지 않은 탓이요, 또 하나는 내 전문 분야가
아니기 때문이다. 나를 많이 괴롭혔던 많은 용어들 중 하나가 바로 Comprehension Principle(이하 CP)이다.
CP가 무엇인가? 한마디로 오리무중이었다. W3C의 시맨틱웹 관련 메일링리스트에서 종종 대면했던 이 용어!! 드디어 오늘 난 웹
검색을 시작했다! 그리고 철학과 논리학 지식의 보고인 스탠포드의 플라톤 철학 백과 사전
사이트(http://plato.stanford.edu)에서 원론적이지만 결정적인 지식을 찾게 되었다.


글에 의하면 CP는 프레게(Frege)에 의해 형식화된 다음과 같은 두 개의 식으로 설명된다. 첫번째 식은 개념(Concept)에 대한, 두번째 식은 관계(Relation)에 대한 CP를 표현한다.


**Comprehension Principle for Concepts**

∃G∀x(Gx ≡ φ(x)),where φ(x) is any formula which has x free and which has no free Gs.

**Comprehension Principle for Relations**

∃R∀x∀y(Rxy ≡ φ(x,y)), where φ(x,y) is any formula with x and y free and which has no free Rs.


이 두 식은 그 모양새로 인해 매우 복잡해 보이지만 말로 설명하면 간단하다. CP를 내가 이해한 대로 말로 풀어보면 다음과 같다.


"임의의 이름으로 명명된 개념이나 관계는 그것을 설명하는 논리식과 동격이다."


예를 들어, '홀수'는 특정 부류의 수들을 개념화한 이름이다. 이 이름은 홀수를 정의하는 논리식, 예를 들어 "2로 나누어
1을 남기는 수"라는 논리식으로 표현된 수들을 지칭한다. CP는 "홀수"라는 개념과 "2로 나누어 1을 남기는 수"가 동치라는
원리이다.게시글 관리
