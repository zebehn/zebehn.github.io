---
title: "OWL 클래스에 속성 달기"
date: 2004-02-24
draft: true
unpublished: true
tags: ["Ontology", "owl", "semantic web"]
categories: ["카테고리 없음"]
---

<!--more-->

> "OWL Full을 사용하지 않고 OWL의 클래스에 속성을 매달 수 있는가?"


최근 W3C의 webont-comment 메일링리스트에 올라왔던 질문의 요지다.


예를 들어, 용어 사전을 만든다고 치자. 사전은 명사와 동사로 이루어져 있다. 그리고, 각 명사마다 관련된 동사들을 엮어준다고 하자. "과자"와 "먹다"를 연결해 주는 식으로 말이다. 간단하게 다음과 같은 예를 적어볼 수 있을 것이다.


```
:Cookie rdf:type owl:Class.
:Eat rdf:type owl:Class.
:relatedAction rdf:type owl:ObjectProperty.
:Cookie :relatedAction :Eat.
```


위와 같은 OWL 구문을 포함하는 문서는 OWL Lite, DL, Full 중 어디에 속할까?


답은 OWL Full이다. OWL Lite와 OWL DL에서 속성(owl:DatatypeProperty & owl:ObjectProperty)은 개체(individual) 간의 관계만을 기술할 수 있기 때문이다. 위 문장의 :relatedAction 속성은 클래스 간의 관계를 기술함으로써 클래스인 `:Cookie`와 `:Eat`를 개체처럼 다루고 있으므로 OWL Full이다. 따라서, 위와 같은 정보를 OWL Lite나 DL로 표현하려면 다음과 같이 단어를 개체로 표현해야 한다.


```
:Word rdf:type owl:Class.
:Noun rdfs:subClassOf :Word.
:Verb rdfs:subClassOf :Word.
:Cookie rdf:type :Noun.
:Eat rdf:type :Verb.
:relatedAction rdf:type owl:ObjectProperty.
:relatedAction rdf:range :Verb.
:relatedAction rdf:domain :Noun.
:Cookie :relatedAction :Eat.
```게시글 관리
