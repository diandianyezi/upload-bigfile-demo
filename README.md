实现思路：
 
 - 对文件切片：即将一个请求拆分成多个请求，每个请求的时间就会缩短，且如果某个请求失败，只需要重新发送这一次请求即可，无需从头开始
 - 通知服务器合并切片
 - 控制多个请求的并发量
 - 断点续传，当多个请求中有请求发送失败，得对失败的请求做处理，让它们重新发送

参考：
https://juejin.cn/post/7053658552472174605