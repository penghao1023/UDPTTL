# UDPTTL
UDP分包发送（丢包重发）

-----------------------------------------------------------------
发送方：依托发送超时时间和内存大小控制发送
1.每次发送，超过5秒没有发送数据或者收到其它控制包就关闭。
2.默认一个进程内部，发送数据量超过100M就不能再发送，只能等待。

---------------------------------------------------------------------
接收方：依托接收超时控制接收
1.每个数据包完整接收超过5秒，则不再接收，认为发送方异常
2.接收方按照发送方端点（IP+Port）放置接收数据，超过10分钟没有数据接收，则移除此端点的存储结构



