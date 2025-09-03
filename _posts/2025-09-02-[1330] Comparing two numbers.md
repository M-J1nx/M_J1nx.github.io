---
title:  "[1330] Comparing two numbers"
excerpt: "Write a program to compare A and B"
categories: 
- Algorithm
tags:
- Problem solving
 
toc_label: Contents
toc: true
toc_sticky: true
 
date: 2025-09-02
last_modified_at: 2025-09-02
---

# Content

---

_Problem link : https://www.acmicpc.net/problem/1330_

## Problem

Given two integers A and B, write a program to compare A and B.

## Input

The first line is given by A and B. A and B are separated by a space.

## Output

Output one of the following three in the first line.

- If A is greater than B, output '`>`.
- If A is less than B, output '<'.
- If A and B are the same, output '=='.

## Limits

- 10,000 ≤ A, B ≤ 10,000

# Answer

---

```cpp
#include<iostream>
using namespace std;

int main() {
	int a, b;
	cin >> a >> b;
	if (a > b) {
		cout << '>';
	}
	else if (a < b) {
		cout << '<';
	}
	else if (a == b) {
		cout << "==";
	}
	return 0;
}
```

The error occurs when I using `‘` in `==`. It was really basic concept, so.. need to caring about details.