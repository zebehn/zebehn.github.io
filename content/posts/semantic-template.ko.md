---
title: "Semantic Template"
date: 2004-03-09
draft: true
unpublished: true
tags: ["device independence", "semantic web"]
categories: ["카테고리 없음"]
---

<!--more-->

장치독립성(device independence)은 유비쿼터스 환경에 필수적이다. 장치독립성은 하나의 휍 컨텐트를 다양한
장치에서 열람할 수 있도록 해 주는 기술이다. 예를 들어, A라는 사이트를 PC 용 웹 브라우저로 접속하면 플래시 애니메이션과
화려한 이미지 등으로 치장된 화면이 보이고, 핸드폰으로 접속하면 핸드폰에 맞는 작은 이미지 몇 개와 텍스트 위주로 꾸며진 화면이
보인다. 또 동일 사이트를 자동차 운전 중 특수 장치로 접속하면 화면 대신 음성으로 낭독된다. 이와 같은 장치 독립성을 가능하게
하는 기술은 크게 세 가지 부류로 나누어 볼 수 있다. 첫째는 정적 장치독립성(static device
independence)으로서 장치 별로 전용 컨텐트를 저작해 놓는 것이고, 둘째는 동적 장치독립성(dynamic device
independence)으로서 하나의 컨텐트를 저작해 놓고 실시간으로 장치에 맞게 변환하는 것이고, 셋째는 이 두 방법을
병용하는 하이브리드 장치독립성(hybrid device independence)이다.


Semantic Template은 하이브리드 장치독립성 부류에 속하는 기술이다. Semantic Template 기술은 웹
컨텐트의 틀(template)을 기술할 때 시맨틱한 정보를 포함하자는 아이디어다. 웹 페이지의 템플릿을 작성하고 서버측
어플리케이션을 통해 컨텐트를 채워넣는 기술은 이제 보편적인 웹 컨텐트 출판 기술이다. 웹 페이지의 전반적인 틀을 템플릿으로
저작해 놓고 제목, 메뉴바, 내비게이션 바, 본문 등 컨텐트의 종류 별로 정해진 위치에 웹 어플리케이션을 이용하여 컨텐트를
동적으로 삽입한다. 웹 페이지 템플릿은 웹 페이지의 구조를 기술한다.


Semantic Template은 웹 페이지 템플릿의 내용을 확장하여 문서의 구조 정보 뿐 아니라 그 안에 들어갈 컨텐트에
대한 정보까지 포함시키자는 아이디어로 만들어졌다. Semantic Template에 기술되는 정보의 예를 들어보면, "이
구역에는 광고가 위치하는데 이미지 또는 플래시 애니메이션 형식으로 256 색상 이하인 컨텐트만 올 수 있다."는 식이다.
Semantic Template은 CC/PP를 기반으로 한 Delivery Context와 결합되어 장치 사양 및 사용자
선호도에 적합하게 컨텐트를 동적으로 변환하기 위한 기반 지식을 구성하게 된다.


내 생각에 Semantic Template은 장치독립성 기술의 실현에 매우 효과적인 기술이라 생각된다. 아래 논문은 참조 문헌이다.


[1] Minsu Jang et al, [Web Content Adaptation and Transcoding based on CC/PP and Semantic Templates](http://www2003.org/cdrom/papers/poster/p195/p195-jang.html), 2003.게시글 관리
