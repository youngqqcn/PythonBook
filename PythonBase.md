# 基本语法

## 第一个Python程序 "Hello World"

```Python
#!coding:utf8

print 'hello World'    # 单引号
print "hello world"   # 双引号
print('hello world')   # 使用print() 函数
print(u'你好,世界!')    # 打印中文
print(u"你好,世界!")   

```

## 基本语法

- Python是使用空白符(4个空格键)缩进进行语句控制的


### 数据类型

```python
>>> s = 'hello world'
>>> type(s)
<type 'str'>
>>>
>>> s = 12
>>> type(s)
<type 'int'>
>>>
>>> s = 12.3
>>> type(s)
<type 'float'>
>>>
>>> s = True
>>> type(s)
<type 'bool'>
>>>
>>>
>>> def foo():
	           print('foo()')
>>> type(foo)
<type 'function'>
>>>
```



### 函数

```python

def foo(arg1, arg2, arg3='hello'):
    '''
    :arg1: 第一个参数
    :arg2: 第2个参数
    : arg3: 有默认参数
    '''
    return arg3 + 'wolrd'  #返回值
```


### if语句
```Python


def TestIF(inArg):
    '''
    :param inArg:  入参
    :return: 无
    '''
    if isinstance(inArg, str):
        print "str"
    elif isinstance(inArg, list):
        print('list')
    elif type(dict) == type(inArg):
        print('dict')
    else:
        print("{0}".format(type(inArg)))
    pass
```


### for语句

```Python

def TestFor(n):
    '''
    :param n:  一个整数
    求  n!
    '''
    #print(reduce(lambda x, y: x * y, range(1, n + 1)))

    result = 1
    for i in range(0, n+1):
        result *= i
    print(result)
```


### while语句


```python
def TestWhile(n):
    '''
    :param n:
    :return:  1+2+3+...+n
    '''

    i = 0
    sum = 0
    while  i <= n:
        sum += i
    return sum
```
