### python统计英文词频



##### 输入输出

由于就跑这一次，就不一行一行输入了。

##### 英文分词（切分字符串）

正则表达式匹配

~~~python
def cut(text):
    pattern = r'[\s,\.?!:\(\)"]+'
    return re.split(pattern, text)
~~~

`\s`可以匹配一个空格（也包括Tab等空白符），所以`\s+`表示至少有一个空格，例如匹配`' '`，`' '`等；

##### 统计个数

建一个dict

```shell
key中记录词
value记录出现的次数
```

遍历记录单词的list

如果dict里面没记录就新赋值一个dict[key] = 1

##### 排序

根据value值排序

```python
result_sorted = sorted(result.items(), key=lambda x:x[1], reverse=True)
```

sorted没个字典项，以x[1]为关键词，x[0]表示key。

逆序，频率高的放前面。

这样排序出来是元组list，遍历list，再对其中每个元组遍历输出。

##### 代码：

```python
import re
import sys

def cut(text):
    pattern = r'[\s,\.?!:\(\)"]+'
    return re.split(pattern, text)

  
if __name__ == '__main__':
    filename = sys.argv[1]

    inf = open(filename, "r")
    text = inf.read()
    inf.close()
    
    words = cut(text)
    
    result = {}
    for word in words:
        if word in result:
            result[word] += 1
        else:
            result[word] = 1


    result_sorted = sorted(result.items(), key=lambda x:x[1], reverse=True)

    print(len(result_sorted))
    of = open("word_fre.txt", "w+")
    for tul in result_sorted:
        for one in tul:
            of.write(str(one) + "\t")
        of.write("\n")
    of.close()

```

