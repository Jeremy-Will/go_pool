###### 核心思想：固定数量的goroutine for循环处理一同个channel中的数据
###### 特征
```
1.自动扩容至设置的大小，如果任务量小，即便设置值很大也不会出现浪费
2.可异步调整worker数量，手动扩容或缩容
3.可异步关闭，关闭时会等待正在进行中的任务完成，根据任务耗时可能需要花费一点时间
4.工作池接收任务后会返回一个错误，如果有错请结束发送任务，因为这时有可能工作池已被异步关闭
5.若想正常跑完任务关闭工作池，则请发送任务完毕后再关闭工作池
```