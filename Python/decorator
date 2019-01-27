#decorator
[廖雪峰教程](https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/0014318435599930270c0381a3b44db991cd6d858064ac0000)
> 装饰器本质上就是一个返回函数的高阶函数
##
~~~
def now():
     print('2015-3-25')
~~~
现在我们想要增强now()的功能，但是又不想更改now()函数的定义，**这种在代码运行期间动态增加功能的方式**，称为**decorator**
~~~
def log(func):#log就是一个decorator，能够接受一个函数，返回一个函数
    def wrapper(*args, **kw):
        print('call %s():' % func.__name__)
        return func(*args, **kw)
    return wrapper
~~~
现将log添加在`now()`前面
~~~
@log
def now():
    print('2015-3-25')
~~~
这里的`@log`相当于`now = log(now)`
输出为
~~~
call now():
2015-3-25
~~~
当装饰器本身需要参数输入需要三层嵌套
同时需要修改函数名字，否则有些设计签名的程序可能会出错