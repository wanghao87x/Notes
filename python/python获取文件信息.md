### python获取文件信息

**获取文件大小**

```python
import os
f = os,path.getsize(path)
print f/float(1024*1024)
```



**获取创建时间**

```python
import os
f = os.path.getctime(path)
```



**获取修改时间**

```python
import os
f = os.path.getmtime(path)
```

