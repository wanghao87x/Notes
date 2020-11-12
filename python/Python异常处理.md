### Python异常处理

```python
try:

except:

else:
```

异常产生后，如果不处理则会抛出异常，中断程序执行。使用`except`语句捕获异常并处理之后，程序执行except处理的语句，并且继续执行，**不会中断**。



##### 断言assert

+ 语法：assert a==b, "warning"

如果a等于b不成立，则会产生异常AssertionError

+ 处理方式示例：

```python
def saveRes(res):
    # length = res.count('\n')
    try:
        length = res.count('\n')
        assert length == cnt - 1, "数据量和结果数量不一致！"
    except AssertionError as ase:
        print ase
        res = "Error\n" * (cnt-1) + "Error"
    #将翻译结果分段写入文件
    f = codecs.open(outputFile, 'a+', 'utf-8')
    f.write(res)
    f.write('\n')
    f.close()
```

