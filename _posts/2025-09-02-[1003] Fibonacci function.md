---
title:  "[1003] Fibonacci function"
excerpt: "Write a program to find out how many times each 0 and 1 are output when fibonacci(N) is called"
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

_Problem link : https://www.acmicpc.net/problem/1003_

## Problem

The source below is C++ function getting Nth fibonacci number. 

```
int fibonacci(int n) {
	if (n == 0) {
		printf("0");
		return 0;
	} else if (n == 1) {
		printf("1");
		return 1;
	} else {
		return fibonacci(n‐1) + fibonacci(n‐2);
	}
}
```

Write a program to find out how many times each 0 and 1 are output when `fibonacci(N)` is called.

## Input

The number of test cases T is given in the first line.

Each test case consists of a line, given N. N is a natural number less than or equal to 40, or 0.

## Output

For each test case, the number of times 0 is output and the number of times 1 is output are separated by spaces.

# Answer

---

```cpp
#include<iostream>
using namespace std;

long long fiboNum[50] = {0, 1,};

long long fibo(int n) {
	if (n == 0 || n==1) {
		return fiboNum[n];
	}
	else if (fiboNum[n] == 0) {
		fiboNum[n] = fibo(n - 1) + fibo(n - 2);
	}
	return fiboNum[n];
}

int main() {
	int T, N = 0;
	cin >> T;
	for (int i = 0; i < T; i++) {
		cin >> N;
		if (N == 0) {
			cout << "1 0" << endl;
		}
		else {
			cout << fibo(N - 1) << " " << fibo(N) << endl;
		}
	}
}
```

Let’s figure out what is fibonacci number first. 

> *What is a Fibonacci function?* A sequence in which the first and second terms are 1, and all subsequent terms are formed by the sum of the first two terms
Ex. 1, 1, 2, 3, 5, 8, 13, 21 …
> 

Here, the function given in the function is in the form of a recursive function, indicating the number of terms in the index. We only need how many times we call the 0 and 1 indexes, respectively, so we don't need the actual Fibonacci number.

When we summarize the numbers up to 7, we see that the nth number is equal to the number of calls made by the n-1th and n-2th. To make this simple,

![image.png](image.png)

It can be done like this. So let's refer to that and write the code.

```cpp
#include<iostream>
using namespace std;

int countZero = 0;
int countOne = 0;

int fibonacci(int n) {
	if (n == 0) {
		countZero++;
		return 0;
	}
	else if (n == 1) {
		countOne++;
		return 1;
	}
	else {
		return fibonacci(n-1) + fibonacci(n-2);
	}
}

int main() {
	int T, N=0;
	cin >> T;
	for (int i = 0; i < T; i++) {
		cin >> N;
		fibonacci(N);
		cout << countZero << " " << countOne << endl;
		countZero = 0;
		countOne = 0;
	}
}
```

Simply doing this is time-out, which means you can't do the math yourself..

※ For the additional items that used a lot of time.. I thoughtlessly set the array size to 40, but It kept saying it was wrong because N could fit up to 40. Let's pay attention to the array size