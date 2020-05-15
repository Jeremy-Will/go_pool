##### easy_go_pool 特性
```
1.动态扩容至指定size
2.size可异步改变：AdjustSize(workNum uint16)
3.可异步关闭也可同步等待任务完成后关闭
适合对任务处理时间短任务量有限的工作进行处理
```
##### go_pool 特性
```
1.动态扩容至指定size
2.size可异步改变：AdjustSize(workNum uint16)
3.当任务量小于需要时会按设置的间隔时间动态缩容
4.可异步关闭也可同步等待任务完成后关闭
适合对任务处理时间较长任务量不确定的工作进行处理
```
##### benchmark 测试
![](https://raw.githubusercontent.com/z-yuanhao/pool/master/images/1.png)
![](https://raw.githubusercontent.com/z-yuanhao/pool/master/images/2.png)
![](https://raw.githubusercontent.com/z-yuanhao/pool/master/images/3.png)
![](https://raw.githubusercontent.com/z-yuanhao/pool/master/images/4.png)
![](https://raw.githubusercontent.com/z-yuanhao/pool/master/images/5.png)