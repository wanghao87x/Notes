### python模块functools.partial函数

##### functools模块

functools应用于高阶函数，参数和返回值是函数

##### fuctools.partial()

创建一个偏函数。创建一个新的函数，这个函数包含你已经指定的参数，如下：简单例子

~~~python
from functools import partial

def add(x, y):
    return x + y

add_y = partial(add, 3)  # add_y 是一个新函数
add_y(4)
stdout>>> 7
~~~

函数在被调用之前得到，就可以使用。