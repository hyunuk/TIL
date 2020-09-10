---
layout: single
title:  "Python Standard IO"
---

Sometimes, you'll face problems that are not like a standard Leetcode style, which is with parameters and returns.
Problem solving websites such as Hackerrank or acm-style provides problems with standard input/output.
This post is a small tips for the Python standard input and output.
## Standard Output
### 1. print Hello world with line change
```py
  print("Hello world")
```
### 2. print Hello world without line change
```py
  print("Hello world", end="")
```
## Standard Input
```py
  # input
  1 2 3
```
### A. using input with one variable
```py
  a = input()
  print(a) # 1 2 3. a is a **string** that reads the one whole line.
```
### B. using input with multiple variables
```py
  a, b, c = input().split()
  print(a) # 1
  print(b) # 2
  print(type(c)) # <class 'str'>
  # making error if input is not splitted by 3
```
### C. changing type of input
```py
  a, b, c = map(int, input().split())
  print(a+b+c)
```
### D. Putting numbers into a list
```py
  a = list(map(int, input().split()))
  print(a)  # [1, 2, 3]
```
### E. If you cannot figure out the size of input
```py
  ret = list()
    while True:
      temp = list(map(int, input().split()))
      if not temp:
        break
      ret.append(temp)
    print(ret)
```
### F. Using sys.stdin.read() instead of input()

input() is slow especially when it deals with the large amount of data.
