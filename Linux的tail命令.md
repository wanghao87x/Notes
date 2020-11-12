### tail命令语法
```python
tail[-f][-c Number|-n Number|-m Number|-b Number|-k Number][File]
```

**参数解释：**
*-f* 	该参数用于监视File文件增长。
*-c* 	Number 从 Number 字节位置读取指定文件
*-n* 	Number 从 Number 行位置读取指定文件。
*-m* 	Number 从 Number 多字节字符位置读取指定文件，比方你的文件假设包括中文字，假设指定-c参数，可能导致截断，但使用-m则会避免该问题。

<br>
*-b*	Number 从 Number 表示的512字节块位置读取指定文件。
*-k* 	Number 从 Number 表示的1KB块位置读取指定文件。
*File* 	指定操作的目标文件名称

上述命令中，都涉及到number，假设不指定，默认显示10行。Number前面可使用正负号，表示该偏移从顶部还是从尾部开始计算。
tail可运行文件一般在/usr/bin/以下。