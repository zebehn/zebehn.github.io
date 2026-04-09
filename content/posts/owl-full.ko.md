---
title: "OWL Full에 대하여"
date: 2004-02-24
draft: true
unpublished: true
tags: ["Ontology", "owl", "semantic web"]
categories: ["카테고리 없음"]
---

<!--more-->

[[OWL Reference의 8.1절 번역입니다.](http://www.w3.org/TR/2004/REC-owl-ref-20040210/#OWLFull)]


OWL Full을 OWL의 하위 언어라 하기는 뭣하다. 모든 OWL 구문을 포함하고 있을 뿐 아니라 자유로운 RDF 구문
구조를 제약 없이 사용할 수 있도록 허용하고 있기 때문이다. OWL Full에서 owl:Class는 rdfs:Class와
동치이다. 반면 OWL Lite와 OWL DL에서 owl:Class는 rdfs:Class의 진부분집합이다. (즉, 모든 RDF
클래스가 OWL Lite 또는 DL 클래스는 아니다.) 또한, OWL Full에서는 클래스를 개체로 취급할 수 있다. 예를
들면, OWL Full에서는 "Fokker-100"이라는 이름을 (운항 중인 Fokker-100 기종 항공기들의 집합이란
의미로) 클래스 이름으로 사용할 수도 있고 동시에 (AirplaneType 클래스의 인스턴스로서) 개체의 이름으로 사용할 수도
있다.


OWL Full에서 데이터 값은 모두 개체의 영역에 속하는 것으로 간주된다. 실질적으로 OWL Full의 개체 공간에는
모든 자원들이 포함된다. 즉, owl:Thing은 rdfs:Resource와 동치이며, 따라서 데이터 타입 속성(data
type properties)과 개체 속성(object properties)은 서로 떨어진 집합이 아니다. OWL Full에서
owl:ObjectProperty는 rdf:Property와 동치이다. 결론적으로 owl:DatatypeProperty는
owl:ObjectProperty의 부분집합이 된다. (주의: 이는 owl:ObjectProperty와
owl:DatatypeProperty가 둘 다 rdf:Property의 부분집합이라는 사실에 모순되지 않는다.)


OWL의 표현력과 RDF의 유연한 메타모델링 기능을 모두 활용하고자 하는 사람들에게 OWL Full은 유용한 선택이 될
것이다. 그러나, OWL Full의 기능을 사용하면 OWL Lite와 OWL DL이 제공하는 보장된 추론 특성을 잃게 된다.


- 노트 1: OWL Lite나 OWL DL에 의거하여 작성되지 않은 모든 RDF 문서는 OWL Full 문서이다.

- 노트 2: 다시 한번 요약 정리하면, OWL Full에서는 owl:Thing과 rdfs:Resource가 동치이고,
owl:Class와 rdfs:Class가 동치이고, owl:ObjectProperty와 rdf:Property가 동치이다.게시글 관리
