### python多进程multiprocessing

multiprocessing是python的多进程管理包，其中大部分API与threading多线程模块类相似，但是换到了多进程的场景。

通过使用进程而非线程有效绕过了全局解释器锁。

> global interpreter lock -- 全局解释器锁
>
> [CPython](https://docs.python.org/zh-cn/3/glossary.html#term-cpython) 解释器所采用的一种机制，它确保同一时刻只有一个线程在执行 Python [bytecode](https://docs.python.org/zh-cn/3/glossary.html#term-bytecode)。此机制通过设置对象模型（包括 [`dict`](https://docs.python.org/zh-cn/3/library/stdtypes.html#dict) 等重要内置类型）针对并发访问的隐式安全简化了 CPython 实现。给整个解释器加锁使得解释器多线程运行更方便，其代价则是牺牲了在多处理器上的并行性。

所以multiprocessing能更充分的利用多处理器。

#### 进程池

可以创建一个进程池，它将使用 [`Pool`](https://docs.python.org/zh-cn/3/library/multiprocessing.html#multiprocessing.pool.Pool) 类执行提交给它的任务。

```python
*class* multiprocessing.pool.Pool([*processes*[, *initializer*[, *initargs*[, *maxtasksperchild*[, *context*]]]]])
```

processes参数表示进程数量，默认为[`os.cpu_count()`](https://docs.python.org/zh-cn/3/library/os.html#os.cpu_count) （即系统处理器数量）

##### map()

```python
map(func, iterable[, chunksize=None])1
```

Pool类中的map方法，与内置的map函数用法行为基本一致，它会使进程阻塞直到返回结果。
注意，虽然第二个参数是一个迭代器，但在实际使用中，必须在整个队列都就绪后，程序才会运行子进程。



