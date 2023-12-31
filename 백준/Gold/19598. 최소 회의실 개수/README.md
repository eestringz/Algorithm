# [Gold V] 최소 회의실 개수 - 19598 

[문제 링크](https://www.acmicpc.net/problem/19598) 

### 성능 요약

메모리: 135932 KB, 시간: 540 ms

### 분류

자료 구조, 그리디 알고리즘, 우선순위 큐, 정렬, 스위핑

### 문제 설명

<p>서준이는 아빠로부터 N개의 회의를 모두 진행할 수 있는 최소 회의실 개수를 구하라는 미션을 받았다. 각 회의는 시작 시간과 끝나는 시간이 주어지고 한 회의실에서 동시에 두 개 이상의 회의가 진행될 수 없다. 단, 회의는 한번 시작되면 중간에 중단될 수 없으며 한 회의가 끝나는 것과 동시에 다음 회의가 시작될 수 있다. 회의의 시작 시간은 끝나는 시간보다 항상 작다. N이 너무 커서 괴로워 하는 우리 서준이를 도와주자.</p>

### 입력 

 <p>첫째 줄에 배열의 크기 N(1 ≤ N ≤ 100,000)이 주어진다. 둘째 줄부터 N+1 줄까지 공백을 사이에 두고 회의의 시작시간과 끝나는 시간이 주어진다. 시작 시간과 끝나는 시간은 2<sup>31</sup>−1보다 작거나 같은 자연수 또는 0이다.</p>

### 출력 

 <p>첫째 줄에 최소 회의실 개수를 출력한다.</p>

### :pushpin: 풀이

처음에 종료시간을 기준으로 정렬한 '백준 1931 - 회의실' 문제처럼 접근하다가 틀렸다.

<p>
 그 이유는 '문제 1931' 는 "회의실을 사용할 수 있는 회의의 최대 개수"를 구해야 한다. 이것은 최대한 많은 회의를 겹치지 않고, 회의의 종료 시간을 기준으로 정렬하면, 가장 빨리 끝나는 회의부터 차례대로 처리할 수 있으므로 최대한 많은 회의를 할 수 있게 되었다.
</p>
<p>
 하지만 이 문제에서는 "최소 회의실 개수"를 구해야 한다. 이것은 동시에 진행되는 회의의 최소 개수를 의미하므로 시작 시간이 빠른 순서대로 회의를 처리하면 됩니다. 만약 하나의 회의가 끝나는 시간과 다음 회의가 시작하는 시간이 겹치지 않는다면 같은 회의실에서 계속 진행할 수 있으므로 최소 회의실 개수를 구할 수 있다.
</p>

