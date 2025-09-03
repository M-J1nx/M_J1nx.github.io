---
title:  "[1010] Building bridge"
excerpt: "Solving algorithm problem of Baekjoon"
categories: 
- Algorithm
tags:
- Problem solving
 
toc_label: Contents
toc: true
toc_sticky: true
 
date: 2025-09-03
last_modified_at: 2025-09-03
---

# Content

---

_Problem link : https://www.acmicpc.net/problem/1003_

## Problem

Jaewon tries to build bridge across the river. There’re N sites on the west side of the river and M sites on the east side of it (N≤M). When building the bridge, only one bridge can be built in one sight. Jaewon wants to build many bridges as many as possible, so he tries to build N bridges. Write a program to find the number of cases in which bridges can be built when you say that bridges cannot overlap each other.

## Input

The first line of the input is given the number of test cases T. Then, for each test case, the integer N, M (0 < N ≤ M < 30) is given for the number of sites on the west and east side of the river.

## Output

For each test case, output the number of cases in which a bridge can be built under the given conditions.

# Answer

---

```cpp
#include<iostream>
using namespace std;

int main() {
	int T, N, M;
	cin >> T;
	for (int p = 0; p < T; p++) {
		double top = 1;
		double bottom = 1;
		cin >> N >> M;
		for (int i = M; i > M-N; i--) {
			top *= i;
		}
		for (int j = N; j > 0; j--) {
			bottom *= j;
		}
		printf("%.0lf\n", top/bottom);
	}
}
```

We just need to find the number of cases where N of M are chosen. Since problem said that legs cannot overlap, we don't need to worry about the order.

$nCm = \frac{n!}{m!*(n-m)!}$

+In the answer code, common part is considered like below :

<img width="1459" height="564" alt="image" src="https://github.com/user-attachments/assets/dad11556-0f6a-4487-9dbb-2802bb176d48" />
