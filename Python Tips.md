---
layout: single
title:  "Python Tips"
---

## Use Maximum and Minimum Integer
```py
  max_int = sys.maxsize
  min_int = -sys.maxsize
```
## Incrementing Count in Dictionary
```py
  for i in dic:
    count = dic.get(i, 0)
    dic[i] = count + 1
    # or
    dic[i] = dic[i] + 1 if i in dic else 1
```
## Using Lists as Queues
Using queue by list is slow because of the properties of list, which is fast at the end but slow at the beginning operations, as every elements has to be shifted one by one.
```py
  from collections import deque
  q = deque([1, 2, 3, 4])
  q.append(1) # deque([1])
  q.append(2) # deque([1, 2])
  q.popleft() # return 1
```
## Initialize nested container
```py
  out_list = [[0] * len(width) for _ in range(len(height))] # 2d list
```
## Getting ASCII code
```py
  A = ord("A") # 65
  a = ord("a") # 97
  zero = ord("0") # 48
```
