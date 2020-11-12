### Python遍历文件夹

Os.walk()

函数：

```python
os.walk(top[, topdown=True[, onerror=None[, followlinks=False]]])1
```

- top – 根目录下的每一个文件夹(包含它自己), 产生3-元组 (dirpath, dirnames,
  filenames)【文件夹路径, 文件夹名字, 文件名】。
- topdown –可选，为True或者没有指定, 一个目录的的3-元组将比它的任何子文件夹的3-元组先产生
  (目录自上而下)。如果topdown为 False, 一个目录的3-元组将比它的任何子文件夹的3-元组后产生 (目录自下而上)。
- onerror – 可选，是一个函数; 它调用时有一个参数, 一个OSError实例。报告这错误后，继续walk,或者抛出exception终止walk。
- followlinks – 设置为 true，则通过软链接访问目录。

##### python获取文件绝对路径

```python
os.path.abspath(__file__)
```

