### python pandas中的dataframme对象转换为list

**构造dataframe**

```python
 df = pd.DataFrame(
   {
     'a':[1,3,5,7,4,5,6,4,7,8,9], 
     'b':[3,5,6,2,4,6,7,8,7,8,9]
   }
 )
```

**转为list的方法**

```python
#如果dataframe是单维度就直接转tolist()
#a列转化为list
df['a'].tolist()
#or
df['a'].values.tolist()
#去除重复
df['a'].drop_duplicates().tolist()
```

