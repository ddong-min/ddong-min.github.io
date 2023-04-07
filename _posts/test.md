---
layout: post
title: "[Ddong-Min] 백준 2178번 미로탐색 문제풀이"
excerpt: "백준문제풀이 - 미로탐색"

categories:
    - 백준
tags:
    - [백준]

toc: true
toc_sticky: true

data: 2023-04-06
last_modified_at: 2023-04-06
---


### 풀이설명

풀이 아이디어 :

1) 먼저 이 문제는 가중치가 없는 그래프에서의 최단거리를 구하는 문제라고 볼 수 있기 때문에 BFS를 사용해서 문제를 푸는 방법을 생각했습니다.

2) 일반적인 그래프 문제와 달리 queue에 넣어야 하는 값이 x,y좌표로 두개의 정보를 넣어야 했기 때문에 vector를 사용하는 것을 생각했지만 아직 vector사용법이 익숙하지 않아서 queue배열을 2차원 배열로 설정하고 열을 2개씩 설정해서 각각 x값과 y값을 갖도록 설정했습니다.


코드 실행과정 :

1) (1,1)인 시작위치를 기준으로 기준위치의 상하좌우 위치가 방문한 적이 있는 지 그 위치의 값이 1인지 0인지 검사함으로써 조건에 만족하면 그 위치로 이동하게 됩니다. 
2) while문을 활동하여 위의 과정을 미로의 모든 길이 막힐때 까지 반복합니다. 이때 dist배열을 이용해서 미로위의 각위치까지의 최단거리 값을 배열에 담아줍니다.
3) while문이 종료되면 N,M까지의 최단거리(dist[N-1][M-1])값을 출력해줍니다.



cf)후에 vector를 사용한 방법과 메모리와 수행시간을 줄일 수 있는 다양한 풀이를 추가로 올리겠습니다.