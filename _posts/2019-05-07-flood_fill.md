---
title: 플러드 필 알고리즘
layout: post
date: '2019-05-07 17:24:00'
tags:
- algorithm
---

>*플러드 필 알고리즘으로 그래프의 연결요소의 개수를 구할 수 있다.*

---

### 개념
그래프의 연결요소가 몇 개인지 파악하는 알고리즘이다.

2차원 맵 선형탐색 중, 연결요소 번호가 정해지지 않은 곳에서 그래프 탐색한다.

그림판의 채우기 도구 

---
### 문제 [(백준 2667번 : 단지번호 붙이기)](https://www.acmicpc.net/problem/2667)

<그림 1>과 같이 정사각형 모양의 지도가 있다. 

1은 집이 있는 곳을, 0은 집이 없는 곳을 나타낸다. 

철수는 이 지도를 가지고 연결된 집들의 모임인 단지를 정의하고, 단지에 번호를 붙이려 한다. 

여기서 연결되었다는 것은 어떤 집이 좌우, 혹은 아래위로 다른 집이 있는 경우를 말한다. 

대각선상에 집이 있는 경우는 연결된 것이 아니다. 

<그림 2>는 <그림 1>을 단지별로 번호를 붙인 것이다. 

지도를 입력하여 단지수를 출력하고, 각 단지에 속하는 집의 수를 오름차순으로 정렬하여 출력하는 프로그램을 작성하시오.

---
### 풀이<br>
집이 있고, 단지번호가 붙여지지 않은 위치에서 네 방향으로 탐색 알고리즘 적용

```python
n = int(input())
home =[] # 집의 위치를 저장한 리스트
danji = [[0 for _ in range(0,n)] for _ in range(0,n)] # 단지번호를 저장한 리스트
for i in range(0,n):
    home.append(list(map(int,list(input())))) # 집 위치 입력

cnt = 0 # 단지번호를 위한 변수

def DFS(i,j,cnt): # 깊이우선탐색 재귀
    danji[i][j] = cnt
    if((j-1>=0) and (home[i][j-1] == 1) and danji[i][j-1] == 0): # 왼쪽 탐색
        DFS(i,j-1,cnt)
    if((i-1>=0) and (home[i-1][j] == 1) and danji[i-1][j] == 0): # 위 탐색
        DFS(i-1,j,cnt)
    if((j+1<n) and (home[i][j+1] == 1) and danji[i][j+1] == 0): # 오른쪽 탐색
        DFS(i,j+1,cnt)
    if((i+1<n) and (home[i+1][j] == 1) and danji[i+1][j] == 0): # 아래 탐색
        DFS(i+1,j,cnt)
    return

for i in range(0,n):
    for j in range(0,n):
        if((home[i][j] == 1) and (danji[i][j] == 0)): # 집이 있는데 단지번호 안붙여져 있으면
            cnt+=1 # 단지번호 증가
            DFS(i,j,cnt) # 깊이우선탐색
```