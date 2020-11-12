### Linux命令grep查找文件内容

grep 命令用于查找文件里符合条件的字符串

简单的：

```shell
% grep "string" filename(dirname)
```

可选参数有：

```shell
-e "regex" 正则匹配
-i "string" 不分大小写
-c "string" 查看行数
-v "string" 不匹配项
```

