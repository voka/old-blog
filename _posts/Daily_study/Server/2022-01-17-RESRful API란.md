---
title: "RESR(ful) API란?"
categories:
  - Daily Study
toc: true
toc_sticky: true
tags:
  - Study
  - Android
  - web
  - DataBase
  - Server
  - REST API
---

# REST API
## 1. REST 개념
  - REST는 Representational State Transfer의 약자로 **자원(resource)** 의 **표현(representation)** 에 의한 상태 전달을 뜻합니다.
  - 기본적으로 **웹의 기존 기술과 HTTP 프로토콜을 그대로 활용**하기 때문에 웹의 장점을 최대한 활용할 수 있는 아키텍쳐 스타일입니다. 
  - Client와 Server사이의 통신방식 중 하나 

  - ## 구성요소
    > 1. 자원 : 소프트웨어가 관리하는 모든 것 (문서, 그림, 데이터 등)
    > 2. 표현 : 자원을 표현하기 위한 이름 (Month, Students 등)
    > 3. 상태전달 : 데이터의 요청에 따라 자원의 상태를 전달하는 것 (보통 Json or XML 방식으로 데이터를 주고 받는다.)



## 2. SW에서의 REST
  - 어떤 자원에 대해 CRUD(Create, Read, Update, Delete) 연산을 수행하기 위해 URI(<span style="color:lightgreen">Resource</span>)로 GET,POST등의 전달방식(<span style="color:lightgreen">Method</span>)을 사용해 요청을 보냅니다. 
  - 그리고 요청을 위한 자원은 특정한 형태(<span style="color:lightgreen">Representation of Resource</span>)로 표현됩니다. (Json or XML과 같은)
