# 数据流解析失败或者存储任务启动失败! ! !

#### 数据流解析拆分

![数据流](https://github.com/yinchuanwang/sharplookQA/blob/master/stream.001.jpeg)

#### 问题诊断
+ 如果节点5失败可能是什么原因？
+ 如果节点11失败可能是什么原因？
+ 如果消息收发都正常，但还是显示启动失败是什么原因？


#### 诊断结果
+ 接收消息失败的可能原因
  + topic配置错误。producer-consumer不登对
  + 连接kafka状态不稳定。
  + 代码处理bug
+ 消息解析失败的原因
  + 版本不匹配，jar包问题
+ 消息正常，但还是显示启动失败
  + 前端总共等待10秒，走完这18步超时了
+ 消息正常，但还是显示启动中
  + 第17步出问题了，ITOA可能hang住了(gc或者其他问题)，重启ITOA

