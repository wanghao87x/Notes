## 1.向普通文本文件写入Unicode字符

> python内置库中的open方法只能读写ascii码，如果想写入Unicode字符，需要使用codecs包

代码示例：

```
# -*- coding: utf-8 -*-
import codecs
content = u'你好'
f = codecs.open('c:/test.txt', 'w', 'utf-8')
f.write(content)
```

我们可以看到codecs包中的open函数可以传入编码参数。