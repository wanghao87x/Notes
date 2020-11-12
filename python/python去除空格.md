### 一、去除空格

strip()

```python
"···xyz···".strip()            # returns "xyz"  
"···xyz···".lstrip()           # returns "xyz···"  
"···xyz···".rstrip()           # returns "···xyz"  
"··x·y·z··".replace(' ', '')   # returns "xyz" 
1234
```

### 二、替换 `replace("space","")`

用 `replace("\n", "")`，与 `replace("\r", "")`，后边的内容替换掉前边的。

实际问题：

如图：

string中内容

![这里写图片描述](https://img-blog.csdn.net/20180715113106561?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2plcnJ5Z2FvbGluZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

其中，“ · ”代表的为空格，一段话被换行成了几段。

1.使用 `.strip()` 只能够去除字符串首尾的空格，不能够去除中间的空格。如图：

![这里写图片描述](https://img-blog.csdn.net/20180715113056973?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2plcnJ5Z2FvbGluZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

所以需要使用 `.replace(' ', '')` 来替换空格项。`string.replace(' ', '')`。如图：

![这里写图片描述](https://img-blog.csdn.net/20180715113031300?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2plcnJ5Z2FvbGluZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
2.使用 `.replace('\n', '')` 去除换行。如图：并不能达到效果。

![这里写图片描述](https://img-blog.csdn.net/20180715112957749?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2plcnJ5Z2FvbGluZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

原因在于：在python中存在继承了 回车符\r 和 换行符\n 两种标记。

`\r`和`\n` 都是以前的那种打字机传承来的。

`\r` 代表回车，也就是打印头归位，回到某一行的开头。

`\n`代表换行，就是走纸，下一行。

linux只用`\n`换行。

win下用`\r\n`表示换行。

python中同样一句话：`print (u'前面的内容\r只显示后面的内容')`

所以，在去除换行时，需要同时去除两者才行，即使用

```python
.replace('\n', '').replace('\r', '')
1
```

结果如图：