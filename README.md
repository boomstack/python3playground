# python3playground

### 分割字符串
```python
s = "aaaa:bbbb:ccccc:ddddd: dsfsdf:fasdeeeeee"
ans = s.split(':')
```

### deque使用，可担任数组、队列、栈, java能做到的它都能，java不能直接做到的它也能
```python
import collections

q = collections.deque()
# 向右添加元素
q.append(11)
q.append(22)
# 向左添加元素
q.appendleft(33)
q.appendleft(44)
# >>deque([44, 33, 11, 22])
# 可直接像java数组一样访问！！！
t = q[1]
#
q.extend([1, 2, 3])
q.extendleft([3, 4, 5])
# >>deque([5, 4, 3, 44, 33, 11, 22, 1, 2, 3])
num = q.count(1)  # 1出现的次数

# Stack pop出栈 && append压栈
q.pop()
# >>deque([5, 4, 3, 44, 33, 11, 22, 1, 2])

# Queue popleft出队 && append入队
q.popleft()
# >>deque([4, 3, 44, 33, 11, 22, 1, 2])
# 删除指定位置，其他也通用！！！！
del q[1]
# >>deque([4, 44, 33, 11, 22, 1, 2])

# 删除指定元素
q.remove(33)
# >>deque([4, 44, 11, 22, 1, 2])
# 翻转
q.reverse()
# >>deque([2, 1, 22, 11, 44, 4])
print(q)


```

