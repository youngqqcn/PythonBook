# 面向对象


```python
>>> class User:
          '''
          这是一个用户类
          '''

            #构造
        	def __init__(self, inName, inAge, inPassword = '888',  inSex='male'):
        		self.name = inName  #公有成员变量
            self.sex = inSex
        		self.__age = inAge   #私有成员变量
        		self.__passwd = inPassword


        	def GetAge(self): #公有方法
        		return self.__age

        	def __GetPasswd(self): #私有方法
        		return self.__passwd

        	def Login(self, usrName, usrPasswd):  #登录,以查看密码
        		if self.name != usrName:
        			print('user name or passwd error!')
        			exit(1)
        		if self.__passwd == usrPasswd:
        			print('your passwd is : {0}'.format(self.__GetPasswd())) #查看密码


>>> yqq = User('yqq', 11, '12345')
>>> yqq.name
'yqq'
>>> yqq.sex
'male'
>>> yqq.GetAge()
11
>>> yqq.Login('yqq', '123')
>>> yqq.Login('yqq', '12345')
your passwd is : 12345
>>>

```
