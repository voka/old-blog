---
title: "위상정렬(Topological Sort)"
categories:
  - Algorithm
toc: true
toc_sticky: true
tags:
  - C++
  - python
  - Algorithm
  - Topological Sort
---

## <span style="color:lightgreen">위상정렬(Topological Sort)</span>

위상정렬은 순서가 정해진 작업을 수행할 시, 그 순서를 결정해주는 알고리즘입니다. 
동시에 진행할 수 있는 일도 있기 때문에 여러가지 답이 존재합니다. 그리고 <span style="color:lightblue">사이클이 발생할 시  시작점을 찾을 수 없기 때문에</span> 방향이 있지만 사이클이 발생하지 않는 그래프일때 적용이 가능합니다.


### 위상정렬의 특징
1. 해당 그래프가 사이클이 발생하는지
3. 발생하지 않는다면 위상정렬의 결과는 어떤지


### 큐를 사용한 위상정렬 방법
1. 진입차수(선행조건의 수)가 0인 노드를 큐에 삽입합니다.
2. 큐에서 원소를 꺼내 연결된 간선을 제거해 나머지 노드의 진입차수를 감소시킵니다.
3. 큐에 감소된 진입차수가 0인 노드를 삽입합니다. 
4. 2,3번을 모든 노드를 방문 할때까지 진행합니다.
5. 모든노드를 방문하기 전에 큐가 빈다는 것은 해당 그래프에 사이클이 존재한다는 말입니다.
-  위 진행과정에서 <span style="color:orange">큐에서 노드를 꺼내어 둔 순서</span>가 바로 위상정렬로 결정된 순서입니다.

## 백준 예제

아래는 C++로 작성된 백준 2252 줄세우기 코드입니다. 


<script src="https://gist.github.com/voka/bba8fec818e1dcf8c30995ef08112c66.js"></script>


python 코드입니다.


<script src="https://gist.github.com/voka/30aa161ac2bc76847031f6fef974434b.js"></script>