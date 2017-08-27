# 数据结构

## str 对象

```Python
>>> s = 'hello python'
>>> type(s)
<type 'str'>
>>> len(s)
12
>>> s[6]
'p'
>>> s[6 : ]
'python'
>>> s[2 : 5]
'llo'
>>> s[0 : 4]
'hell'
>>> s[ : ]
'hello python'
>>> s[ : -1]
'hello pytho'
>>> s[ : -4]
'hello py'
>>> s[ :: -1]
'nohtyp olleh'
>>> s
'hello python'
>>> 'pyt' in s
True
>>> 'pty' in s
False
>>> s.find('th')
8
>>> s.replace('py', 'PPPy')
'hello PPPython'
>>> s
'hello python'
>>>

```



## list  列表

相当于链表


| 方法名 | 作用 |
|--------|------|
| append| 追加一个对象 |
| extend | 将其他对象的内容追加进来|

```python
>>> l = [1, 3, 4, 5]
>>> type(l)
<type 'list'>
>>> l[3]
5
>>> l[ : -2]
[1, 3]
>>> l.append('343')
>>> l.append([9, 8, 7])
>>> l
[1, 3, 4, 5, '343', [9, 8, 7]]
>>> l.extend([9, 8, 7])
>>> l
[1, 3, 4, 5, '343', [9, 8, 7], 9, 8, 7]
>>> for item in l:
	           print (item)


1
3
4
5
343
[9, 8, 7]
9
8
7
>>>

```

## dict  字典
键值对

类似STL中map容器

** dict的key必须是不可变对象(如:str, tuple, int, 等)。**

```python
>>> d = {'name': 'Kim', 'age' : 99, 'hobby' : 'football'}
>>> type(d)
<type 'dict'>
>>> d['name']
'Kim'
>>> d
{'hobby': 'football', 'age': 99, 'name': 'Kim'}
>>> len(d)
3
>>> d['Tel'] = 9119119119119111
>>> d
{'hobby': 'football', 'age': 99, 'Tel': 9119119119119111L, 'name': 'Kim'}
>>> d.keys()
['hobby', 'age', 'Tel', 'name']
>>> d.values()
['football', 99, 9119119119119111L, 'Kim']
>>> for key, value in d.items():
	print ('{0}={1}'.format(key, value))


hobby=football
age=99
Tel=9119119119119111
name=Kim
>>>

```


## tuple  元组

tuple是不可变对象, 其内容不可修改, 其他和list一样

```python
>>> t = (1, 3, 4, 'yqq', 434.32, 4, 3, 'yqq')
>>> t.count(4)
2
>>>
>>> t.index(4)
2
>>> t[4]
434.32
>>>
>>> 4 in t
True
>>>  
>>> for item in t:
	print (item)


1
3
4
yqq
434.32
4
3
yqq

```


## set 集合


```python
>>> s1 = set([1, 3, 5, 7, 9])
>>> s2 = set((9, 4, 3, 1))
>>> type(s1)
<type 'set'>
>>> type(s2)
<type 'set'>
>>> s1
set([1, 3, 9, 5, 7])
>>> s2
set([9, 3, 4, 1])
>>> s1 | s2
set([1, 3, 4, 5, 7, 9])
>>> s1 - s2
set([5, 7])
>>> s1 + s2

Traceback (most recent call last):
  File "<pyshell#159>", line 1, in <module>
    s1 + s2
TypeError: unsupported operand type(s) for +: 'set' and 'set'
>>> s1 & s2
set([9, 3, 1])
>>>

```
