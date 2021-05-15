# js-algo
자바스크립트 알고리즘 스터디 기록
___
## 알고리즘 출제 유형 빈도
| 유형 | 출제빈도 |
|---|:---:|
| [`구현`](#구현) | `33%` |
| [`BFS/DFS`](#BFS/DFS) | `20.9%` |
| [`그리디`](#그리디) | `19.8%` |
| [`정렬`](#정렬-(-Sort-) | `8.2%` |
| [`동적 프로그래밍`](#동적-프로그래밍-(-dymanic-programming-) | `8.2%` |
| [`이진탐색`](#이진탐색) | `3.8%` |
| `최단 경로` | `3.3%` |
| `그래프 이론` | `2.7%` |

> 출처 : [코딩 테스트에서는 주로 기초 알고리즘에 기반하는 문제가 출제됩니다.
그중에서도 가장 출제 빈도가 높은 문제는 그리디(Greedy), 구현(Implementation), DFS/BFS를 활용한 탐색 문제입니다.](https://realhanbit.co.kr/channel/category/category_view.html?cms_code=CMS7793635735)

## 구현
구현으로 묶이는 유형은 모든 경우의 수를 일일이 계산하는 것(brute force)으로 문제에서 하라는 대로 잘 따라하면 답이 나온다. 생각한 것을 코드로 구현할 수 있는지 보는 문제 유형.
 비효율적인 시간 복잡도를 가지고 있기 때문에 대이터 갯수가 100만개 이하일 때 적절하다. 하지만 쉽게 풀 수 있는 문제를 어렵게 생각하여 생각이 꼬일 수도 있다. 문제를 만나면 먼저 물어보자. 무식하게 풀 수 있을까?

#### 구현 문제에 접근하는 방법
보통 구현 유형은 사소한 입력 조건 등을 명시해주며 문제의 길이가 긴 편이다.
고차원적 사고력을 요구하지 않는 편이라 언어 자체에 익숙하다면 쉽게 풀 수 있다.
 matrix 2차원 공간 행렬 문제.
 완전 탐색과 시뮬레이션 문제로 나누지만 명확하게 구분할 필요는 없다.
둘의 차이는 문제에서 해결 방법을 명시하느냐 아니냐의 차이이고
brute force한 방법으로 푸는 것은 동일하다.

 ##### 정당성 검증 
고려할 사항 : 시간 / 메모리 제한 사항/ 데이터의 갯수

#### + 완전 탐색 (exhaustive search)
        모든 경우의 수를 일일이 탐색.
#### + 시뮬레이션 (simulation)
        문제에서 제시한 알고리즘을 한 단계 씩 차례대로 수행.   
        즉 수행해야 하는 모든 과정이 문제에 이미 나와있다.

---
## BFS/DFS
 대표적인 그래프 탐색 알고리즘   
 
 ![bfsdfs](https://res.cloudinary.com/practicaldev/image/fetch/s---f65OlYQ--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/e2ru41fjhqs4ombbcedf.png "bfs and dbf")
 
### 어떤 경우에 사용해야 하는가
#### 최단 거리를 탐색해야할 때
 e.g : 친구 추천, 네비게이션 최단 거리 안내
### + BFS(Breadth First Search) 너비 우선 탐색
[leetcode BFS \[Easy\]](https://leetcode.com/problemset/algorithms/?topicSlugs=breadth-first-search&difficulty=Easy)

     탐색할 때 너비(형제 노드)를 우선 탐색하는 알고리즘.
      * 두 개의 큐를 사용한다. 큐에 각 노드 정보를 기록해야 한다.
      * 찾고자 하는 노드가 루트 노드에서부터 가까이 있다고 예상될 때 사용.

#### 경로가 존재하는지 판별해야할 때
 e.g : 미로게임
### + DFS(Depth First Search) 깊이 우선 탐색
[leetcode DFS \[Easy\]](https://leetcode.com/problemset/algorithms/?difficulty=Easy&topicSlugs=depth-first-search)

     탐색할 때 깊이(자식 노드)를 우선 탐색하는 알고리즘.
      * 한 개의 큐와 한 개의 스택을 사용한다.
      * BFS보다 속도가 느릴 수 있다.
---
## 그리디
[leetcode : Greedy \[Easy\]](https://leetcode.com/problemset/algorithms/?difficulty=Easy&topicSlugs=greedy)

 탐욕 알고리즘, 각 단계에서 항상 더 큰 쪽으로 선택한다.
 동적 프로그래밍이 필요 이상의 작업을 수행하게 되는 경우를 보완해 고안된 알고리즘

### 어떤 경우에 사용해야 하는가
 최적 부분 구조 / 탐욕 선택 속성
 한 번의 선택이 다음 선택에는 무관한 값이어야 하며 매 순간의 최적해가 문제에 대한 최적해일 때.
 
 * 거스름돈 문제 ( 동전 가격 배수 관계가 성립될 때 [1, 5, 10, 15, 50] )
 * 활동 선택 문제 ( Activity selection problem )
 * 최소 신장 트리 ( Minimum spanning tree ) 
 * 제약 조건이 많은 대부분의 문제
 * 다익스트라 알고리즘
 * 허프만 코드
 * 크러스컬 알고리즘
 
---
## 정렬 ( Sort )
[leetcode : Sort \[Easy\]](https://leetcode.com/problemset/algorithms/?difficulty=Easy&topicSlugs=sort)

데이터를 정렬해야 하는 이유는 [이진탐색](#이진탐색)이 가능하게 만들기 위함.
이 정렬을 어떻게 더 효율적으로 수행할 수 있을지가 핵심.



---
## 동적 계획법 ( Dynamic Programming )
[leetcode : dynamic programming \[Easy\]](https://leetcode.com/problemset/algorithms/?difficulty=Easy&topicSlugs=dynamic-programming)

---
## 이진탐색
[leetcode : binary search \[Easy\]](https://leetcode.com/problemset/algorithms/?difficulty=Easy&topicSlugs=binary-search)

---
## 최단 경로
최단 경로부터는 현재는 너무 어려우므로 이런게 있다는 걸 알고만 있기로...
[상세 설명](https://ratsgo.github.io/data%20structure&algorithm/2017/11/25/shortestpath/) 
 단일 출발 최단경로 ( 단일 노드에서 출발하여 그래프 내의 모든 다른 노드에 도착하는 최단 경로를 찾는 문제 ) 풀이에는 다익스트라, 벨만-포드 알고리즘이 적합하다.
 전체쌍(All-pair) 최단경로 ( 그래프 내 모든 노드 쌍들 사이의 최단 경로를 찾는 문제 ) 풀이에는 플로이드-와샬 알고리즘이 적합하다.

 ### 다익스트라 ( Dijkstra algorithm )
 [상세 설명](https://ratsgo.github.io/data%20structure&algorithm/2017/11/26/dijkstra/)
 너비 우선 탐색 ( BFS )를 기본으로 하는 알고리즘
 
 ### 벨만-포드 ( Bellman-Ford's algorithm )
 [상세 설명](https://ratsgo.github.io/data%20structure&algorithm/2017/11/27/bellmanford/)
 
 ### 플로이드-와샬 
 [상세 설명](https://chanhuiseok.github.io/posts/algo-50/)

---
## 그래프 이론
 위에서 나온 것들이 다 사용되는 듯
 [그래프 이론 기초](http://www.kwangsiklee.com/2017/11/%EA%B7%B8%EB%9E%98%ED%94%84-%EC%9D%B4%EB%A1%A0-%EA%B8%B0%EC%B4%88-%EC%A0%95%EB%A6%AC/)
---
