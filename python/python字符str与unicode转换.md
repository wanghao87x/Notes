### python unicode 和 str转化问题

python中的str对象其实就是"8-bit string" ，字节字符串，本质上类似java中的byte[]。 
而python中的unicode对象应该才是等同于java中的String对象，或本质上是java的char[]。 

```python
str: s = "你好"

unicode: u = u"你好“
```

unicode转化为str (encode 编码）：

```python
str = u.encode('gbk')
```

str转化为unicode （decode 解码）：

```python
unicode = s.decode('gbk')
```

