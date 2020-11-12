### python获取当前循环次数



 enumerate是python 2.3中新增的内置函数，它的英文说明为：

 enumerate( iterable)

```
Return an enumerate object. iterable must be a sequence, an iterator,or some other object which supports iteration. The next() method ofthe iterator returned by enumerate() returns a tuple containing acount (from zero) and the corresponding value obtained from iteratingover iterable. enumerate() is useful for obtaining an indexed series:(0, seq[0]), (1, seq[1]), (2, seq[2]), .... New in version 2.3.它特别适合用于一个for循环时，当我们同时需要计数和元素时可以使用这个函数。举个简单的例子，有一个字符串数组，需要一行一行打印出来，同时每行前面加上计数，从1开始。
```

 s = ['abc', 'This is a test', 'Hello, Python']

 for i, line in enumerate(s):

 print i+1, line