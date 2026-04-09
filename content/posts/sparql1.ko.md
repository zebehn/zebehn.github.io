---
title: "SPARQL (1): 맛보기"
date: 2008-08-07
draft: true
unpublished: true
tags: ["semantic web", "SPARQL"]
categories: ["시맨틱웹,웹2.0"]
---

<!--more-->

SPARQL을 공부하게 되었다. 아니 해야 한다. 하나씩 SPARQL에 대해 알아가는 것들을 블로그에 정리해보려 한다. 굳ㅋ!


### SPARQL이란?


SPARQL(**S**imple **P**rotocol **a**nd **R**DF **Q**uery **L**anguage)
은 W3C에서 만든 RDF 질의 언어이다. 관계형 DB에 SQL이 있다면 RDF엔 SPARQL이 있다. 관계형 DB에 저장된 데이터로부터 원하는 정보를 꺼내오기 위해 SQL을 활용하듯이, 웹에 공개된 각종
RDF 데이터들로부터 우리가 원하는 데이터를 꺼내오기 위해 SPARQL을 사용한다.


### SPARQL의 첫 맛


간단한 예를 통해 SPARQL의 첫 맛을 느껴보자. 먼저 아래와 같이 두개의 트리플(triple)로 구성된 RDF
데이터가 있다고 하자. RDF 데이터는 트리플로 구성된다. 하나의 트리플은 세 개의 데이터 요소로 구성된다. 세 개의 데이터 중 하나는 Subject, 또 하나는 Predicate, 마지막은 Object로 불린다.


```

 "SPARQL Tutorial" .
 "철수"@ko .
```


위에서 첫번째 트리플을 보자. 이 트리플의 Subject는 http://example.org/book/book1, Predicate은 http://purl.org/dc/elements/1.1/title, Object는 "SPARQL Tutorial"이다. 이 트리플의 의미를 직설적으로 풀어 써보면 다음과 같다.


*http://example.org/book/book1이라는 아이디를 가진 어떤 것(!)은 http://purl.org/dc/elements/1.1/title이라는 속성을 갖는데 이 속성의 값은 "SPARQL Tutorial"이다.*


RDF에서 URI로 적은 것들은 모두 실재하는 어떤 것이나 아니면 가상의 어떤 것을 가리킨다. RDF 트리플을 이용하면 위와 같이 간단한 형식을 통해 URI로 가리켜진 어떤 것의 속성을 묘사할 수 있다. 위 트리플의 의미를 좀 더 인간적으로 해석해 보면 다음과 같다.


*http://example.org/book/book1이라는 아이디를 가진 책의 제목(http://purl.org/dc/elements/1.1/title)은 "SPARQL Tutorial"이다.*


위 트리플만으로 이러한 의역은 불가능하다. URI에 포함된 book과 title이라는 단어에 의지한 억지 해석이라 할 수 있다. 기계는 위 트리플로 이와 같은 의미를 절대 알아낼 수 없다. 여하간, 이와같은 의역을 마음에 두고 다음으로 넘어가 보자.


우리가 원하는 데이터가 `http://example.org/book/book1`라는 아이디를 가진 책의 제목이라고 하면, 다음과 같은 SPARQL 질의문을 사용하면 된다.


```
SELECT ?title
WHERE
{
 ?title .
}

```


위 질의문을 SPARQL 처리 엔진에 입력하면 다음과 같은 결과가 나온다.




 title


 "SPARQL Tutorial"


이 테이블의 의미는 `title`의 값, 즉 `http://example.org/book/book1`의 제목이 "SPARQL Tutorial"이라는 것이다.


다시 위로 올라가서 질의문의 의미를 살펴보면 다음과 같다.


먼저, WHERE 이후 괄호 안에 적힌 내용을 보자. WHERE 이후에는 우리가 원하는 데이터가 만족해야 하는 조건을 적는다. 조건은 트리플 패턴의 형태로 적는다. 위 질의문의 트리플 패턴을 말로 풀어보면 이렇다.


*"Subject가 http://example.org/book/book1이고, Predicate이 http://purl.org/dc/elements/1.1/title인 모든 트리플"*


위 트리플 패턴의 Object 위치에 있는 `?title`은 변수이다. (물음표(?)가 붙은 이름은 변수다.) 따라서, 위 패턴을 만족하는 모든 트리플들의 Object가 변수 ?title의 값이 될 수 있다.


질의 대상인 RDF 데이터를 보면, 두개의 트리플 중 한 개가 위 트리플 패턴에 맞아떨어진다. 그 트리플의 Object가 "SPARQL Tutorial"이므로, 변수 `?title`의 값이 "SPARQL Tutorial"이라는 결과가 질의문의 답이 된 것이다.


### 맺으며...


SQL을 조금이라도 접해본 사람은 SPARQL을 이해하기 쉬울 듯 하다. SPARQL의 구조와 기능이 SQL과 매우 유사하기
때문이다. 이제 SPARQL이 뭔지 간단히 이해했고, 다음엔 좀 더 형식적으로 SPARQL의 구성을 살펴보겠다.게시글 관리
