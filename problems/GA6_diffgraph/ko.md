승현이는 정점의 개수가 $N$개인 방향성 그래프 $G$와 음이 아닌 정수들로 구성된 배열 $A[1], A[2], \cdots, A[N-1]$을 가지고 있습니다. 정점들에는 $0$ 이상 $N-1$ 이하의 정수 번호가 붙어 있으며, 각 간선에는 가중치가 존재합니다. 초기에 이 방향성 그래프에는 간선이 하나도 없었기 때문에, 승현이는 허전함을 느꼈습니다. 이에 그는 아래와 같은 방식으로 간선들을 잇기로 했습니다.

* 임의의 두 정점 $u$와 $v$ ($0 \le u, v < N, u \neq v$)에 대하여,
  - 만약 $u > v$이고 $A[u - v]$의 값이 양수라면, $u$에서 $v$로 향하는 가중치가 $A[u - v]$인 간선을 추가합니다.
  - 만약 $u < v$이고 $A[u - v + N]$의 값이 양수라면, $u$에서 $v$로 향하는 가중치가 $A[u - v + N]$인 간선을 추가합니다.
  
승현이는 이렇게 간선을 추가한 뒤에 임의의 정점에서 출발하여 다른 정점에 도착하는 최단 경로의 길이를 구하고자 합니다. 

### 입력 형식

첫 번째 줄에 그래프 $G$의 정점의 수 $N$ ($5 \le N \le 2,000$)이 주어집니다. 두 번째 줄에 $A[1], A[2], \cdots, A[N-1]$ ($0 \le A[1], A[2], \cdots, A[N-1] \le 10,000$)이 공백을 사이로 두고 주어집니다. 세 번째 줄에 질의의 수 $Q$ ($1 \le Q \le 200,000$)가 주어집니다. 이후 $Q$개 줄이 주어지는데, 이 중 $i$번째 줄 ($1 \le i \le Q$)에는 두 개의 정수 $a_{i}$와 $b_{i}$ ($0 \le a_{i}, b_{i} < N$, $a_{i} \neq b_{i}$)가 공백을 사이로 두고 주어집니다.

### 출력 형식

여러분은 각 질의마다 $a_{i}$번 정점에서 출발하여 $b_{i}$번 정점에 도착하는 최단 경로의 길이를 한 줄에 하나씩 입력에서 주어진 순서대로 출력해야 합니다. 단 이러한 최단 경로가 존재하지 않을 경우 $-1$을 출력합니다.

### 서브태스크

#### 서브태스크 1 [3점]

* $N \le 7$, $Q = 1$

#### 서브태스크 2 [4점]

* $N \le 50, Q \le 50$

#### 서브태스크 3 [5점]

* $N \le 300, Q \le 87,600$

#### 서브태스크 4 [6점]

* 추가 제약 조건은 없습니다.

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">5<br/>
3 2 0 0<br/>
4<br/>
1 0<br/>
2 1<br/>
3 0<br/>
0 1</td>
   <td class="code-font">3<br/>
3<br/>
5<br/>
4</td>
  </tr>
  <tr>
   <td class="code-font">6<br/>
0 3 0 0 0<br/>
4<br/>
0 4<br/>
1 2<br/>
2 3<br/>
4 0</td>
   <td class="code-font">3<br/>
-1<br/>
-1<br/>
6</td>
  </tr>
 </tbody>
</table>