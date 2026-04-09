---
title: "OWL 추론의 기능"
date: 2006-02-21
draft: true
unpublished: true
tags: ["owl", "owl inference", "semantic web"]
categories: ["카테고리 없음"]
---

<!--more-->

간단한 예를 통해 OWL 추론의 기능을 설명해 보고자 한다. 임의의 OWL 문서에 아래의 두 문장을 기술했다고 하자.


```
:Researcher rdfs:subClassOf :Person.
:Gildong rdf:type :Researcher.

```


rdfs:subClassOf은 클래스 간의 포함 관계를 기술한다. 위의 첫번째 문장은 :Researcher 클래스는
:Person 클래스에 포함된다는 사실을 진술한다. 한 단계 더 들어가면, OWL의 클래스(Class)는
개체(Individual)들의 집합으로 정의된다. 클래스는 클래스 정의(Class Description)에 기술된 바에 따라
임의의 속성을 공유하는 개체들의 집합인 셈이다. 즉, 위의 첫번째 문장은 :Researcher 클래스를 구성하는 모든 개체들은
:Person 클래스를 구성하는 개체이기도 하다는 뜻이 된다. 또는, :Researcher 클래스에 속한 모든 개체들은
:Person 클래스에도 속한다고도 말할 수 있겠다.


rdf:type는 개체의 클래스 소속 여부를 진술한다. 즉, 어떤 개체가 어떤 클래스에 속하는가를 기술한다. 위의 두번째 문장은 :Gildong이 :Researcher 클래스를 구성하는 개체들 중 하나임을 선언한다.


결론적으로,

rdfs:subClassOf와 rdf:type이 내포한 의미에 따라, 위의 두 문장으로부터 다음의 새로운 사실을 유도할 수 있다.


```
:Gildong rdf:type :Person

```


따라서, OWL 문서에 :Person 클래스에 속하는 모든 개체를 명시할 필요가 없다. 상기와 같은 과정을 통해 암묵적으로
:Person 클래스에 속하는 것으로 판명되는 모든 개체들을 끄집어낼 수 있기 때문이다. 이것이 OWL 추론의 기능이다.게시글 관리
